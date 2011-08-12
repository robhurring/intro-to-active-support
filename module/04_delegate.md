!SLIDE bullets incremental
# Module#delegate

* Reduces boilerplate
* Allows forwarding method calls to associations

!SLIDE code

    @@@ ruby
    class User < ActiveRecord::Base
      has_one :profile
      delegate :name, :address, 
        :to => :profile
    end
    
    user = User.first
    user.build_profile({
     name: 'John Smith', 
     address: '123 Fake St.'
    })
    
    user.name       # => John Smith
    user.address    # => 123 Fake St.

!SLIDE code

    @@@ ruby
    class User < ActiveRecord::Base
      has_one :profile
      delegate :name, :address, 
        :to => :profile, :prefix => true
    end

    user = User.first
    user.build_profile({
     name: 'John Smith', 
     address: '123 Fake St.'
    })
    
    user.profile_name       # => John Smith
    user.profile_address    # => 123 Fake St.

!SLIDE code

    @@@ ruby
    class User < ActiveRecord::Base
      has_one :profile
      delegate :name, :address, 
        :to => :profile, :allow_nil => true
    end

    user = User.first
    # ... no profile created for user ...
    
    user.name           # => nil
    user.address        # => nil

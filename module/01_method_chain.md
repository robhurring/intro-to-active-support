!SLIDE
# Module Extensions
## require 'active_support/core\_ext/module'

!SLIDE bullets incremental
# Module#alias\_method\_chain

* Useful for overriding methods
* Keeps the old method available

!SLIDE code small

    @@@ ruby
    class User
      def hello
        "Hello!"
      end
    end

    user = User.new
    puts user.hello
    # => "Hello!"

    class User
      def hello_with_time
        "#{hello_without_time} - #{Time.now.to_s(:short)}"
      end
      alias_method_chain :hello, :time
    end

    puts user.hello
    # => "Hello! - 10 Aug 00:00"
    

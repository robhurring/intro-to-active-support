!SLIDE bullets incremental smaller
# Module#attr\_accessor\_with_default

* Sometimes you just need a default

!SLIDE code

    @@@ ruby
    class Url
      attr_accessor_with_default :port, 80
    end

    Url.new.port # => 80

    class User
      attr_accessor :name, :surname
      attr_accessor_with_default(:full_name) do
        [name, surname].compact.join(" ")
      end
    end

    u = User.new
    u.name = 'Xavier'
    u.surname = 'Noria'
    u.full_name # => "Xavier Noria"
    

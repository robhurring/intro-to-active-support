!SLIDE bullets incremental smaller
# Object#to_param? and Object#to\_query?

* Useful for creating SEO friendly routes

!SLIDE code small

    @@@ ruby
    class User
      def to_param
        "#{id}-#{name.parameterize}"
      end
    end
    
    link_to @user.name, @user
    # /users/1-john-smith
    
    current_user.to_query('user') 
    # => user=1-john-smith
!SLIDE bullets
# Inflections
## Easily format strings in views

!SLIDE code small

    @@@ ruby
    "table".pluralize     
    # => "tables"
    
    "tables".singularize 
    # => "table"
    
    "admin_user".camelize 
    # => "AdminUser"
    
    "visual_effect".camelize(:lower) 
    # => "visualEffect"
    
    "AdminUser".underscore 
    # => "admin_user"
    
    "alice in wonderland".titleize 
    # => "Alice In Wonderland"
    
    "contact_data".dasherize 
    # => "contact-data"
    
    "comments_count".humanize 
    # => "Comments count"
    
!SLIDE code

    @@@ ruby
    "Admin::UsersController".demodulize 
    # => "UsersController"
    

    "admin/users_controller".camelize 
    # => "Admin::UsersController"
    
    
    "admin/users_controller".classify
    # => "Admin::UsersController"
    # NOTE: this is just a string    
    
    
    "admin/user".constantize
    # => Admin::User
    # NOTE: this is the actual class!
    #   "user".constantize.new

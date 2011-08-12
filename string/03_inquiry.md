!SLIDE bullets incremental
# String#inquiry
## Turn string content into methods

!SLIDE code

    @@@ ruby
    "dev".inquiry.dev? 
    # => true
    
    
    s = ActiveSupport::StringInquirer.new("dev")
    s.dev?
    # => true
    
    
    Rails.env.development?
    # => true
    

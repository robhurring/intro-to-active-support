!SLIDE
# String Extensions
## require 'active_support/core\_ext/string'

!SLIDE bullets incremental
# String#html_safe?

* Useful in views where data comes from the user
* Protects from XSS
* Strings are unsafe by default in Rails 3+

!SLIDE code

    @@@ ruby
    "".html_safe? 
    # => false
    
    
    s = "".html_safe
    s.html_safe?
    # => true
    
    
    # appending an unsafe string 
    # will taint the safe string
    "".html_safe + "<"           # => "&lt;"
    "".html_safe + "<".html_safe # => "<"


    <%= raw @cms.current_template %>
    <%== @cms.current_template %>
    # inserts @cms.current_template as is

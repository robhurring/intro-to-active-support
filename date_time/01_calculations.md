!SLIDE
# Date Extensions
## require 'active_support/core\_ext/date'

!SLIDE bullets incremental
# Named Dates

* next_year
* next_week
* next_month
* beginning_of\_week
* beginning_of\_year

!SLIDE code

    @@@ ruby
    d = Date.new(2010, 5, 8) 
    # => Sat, 08 May 2010
    
    
    d.next_month             
    # => Tue, 08 Jun 2010
    
    
    d.next_year              
    # => Sun, 08 May 2011    

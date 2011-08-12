!SLIDE
# String#to\_date(time)
## Convert strings to Date/Time objects

!SLIDE code

    @@@ ruby
    "2010-07-27".to_date              
    # => Tue, 27 Jul 2010
    
    
    "2010-07-27 23:37:00".to_time     
    # => Tue Jul 27 23:37:00 UTC 2010
    
    
    "2010-07-27 23:37:00".to_datetime 
    # => Tue, 27 Jul 2010 23:37:00 +0000

!SLIDE bullets incremental
# Durations

!SLIDE code

    @@@ ruby
    d = Date.current
    # => Mon, 09 Aug 2010
    
    
    d + 1.year
    # => Tue, 09 Aug 2011
    
    
    d - 3.hours
    # => Sun, 08 Aug 2010 21:00:00 UTC +00:00
    
    
!SLIDE code

    @@@ ruby
    now = DateTime.current
    # => Mon, 09 Aug 2010 23:15:17 +0000
    
    
    now + 1.year
    # => Tue, 09 Aug 2011 23:15:17 +0000
    
    
    now - 1.week
    # => Mon, 02 Aug 2010 23:15:17 +0000
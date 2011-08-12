!SLIDE bullets incremental
# Date#step

!SLIDE code

    @@@ ruby
    today = Date.today
    next_week = today + 1.week
    
    today.step(next_week, 1.day) do |day|
      puts day.to_s :long
    end
        
    # => August 10, 2011
    # => August 11, 2011
    # => August 12, 2011
    # => August 13, 2011
    # => August 14, 2011
    # => August 15, 2011
    # => August 16, 2011
    # => August 17, 2011
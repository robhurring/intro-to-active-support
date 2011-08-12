!SLIDE bullets incremental
# Date#advance

!SLIDE code

    @@@ ruby
    date = Date.new(2010, 6, 6)
    
    
    date.advance(:years => 1, :weeks => 2)  
    # => Mon, 20 Jun 2011

!SLIDE bullets incremental
# Range#overlaps?

!SLIDE code
    @@@ ruby
    (1..10).overlaps?(7..11)  
    # => true
    
    
    (1..10).overlaps?(11..27) 
    # => false
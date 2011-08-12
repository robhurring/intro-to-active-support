!SLIDE bullets incremental
# Enumerable#sum

!SLIDE code

    @@@ ruby
    [1, 2, 3].sum 
    # => 6

    
    (1..100).sum  
    # => 5050

    
    (1..5).sum {|n| n * 2 } 
    # => 30

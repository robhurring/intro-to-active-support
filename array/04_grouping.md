!SLIDE bullets incremental
# Array#in\_groups_of
# Array#in_groups

!SLIDE code

    @@@ ruby
    [1, 2, 3].in_groups_of(2) 
    # => [[1, 2], [3, nil]]
    

    
    [1, 2, 3].in_groups_of(2, 0) 
    # => [[1, 2], [3, 0]]


    
    [1, 2, 3].in_groups_of(2, false) 
    # => [[1, 2], [3]]
    

!SLIDE code

    @@@ ruby
    %w{1 2 3 4}.in_groups(2)
    # => [["1", "2"], ["3", "4"]]
    
    
            
    %w{1 2 3 4 5}.in_groups(2, 0)
    # => [["1", "2", "3"], ["4", "5", 0]]    
    
    
    
    %w{1 2 3 4 5}.in_groups(2, false)
    # => [["1", "2", "3"], ["4", "5"]]
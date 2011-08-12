!SLIDE bullets incremental small
# Enumerable#index_by

* Similar to Enumerable#group_by
* Each key has 1 value
* If keys aren't unique, last value is used

!SLIDE code

    @@@ ruby
    orders.index_by(&:number)
    # => {'2009-032' => #<Order>, 
    #     '2009-008' => #<Order>}

          
    
    # duplicate keys are not grouped!
    (1..5).index_by{ |n| n & 1 }
    # => {1=>5, 0=>4}
    
    
    
    (1..5).group_by{ |n| n & 1 }
    # => {1=>[1, 3, 5], 0=>[2, 4]}
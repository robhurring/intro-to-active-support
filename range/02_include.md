!SLIDE bullets incremental
# Range#include?

!SLIDE code
    @@@ ruby
    (2..3).include?(Math::E) 
    # => true
    
    
    (1..10).include?(3..7)  
    # => true
    
    
    (1..10).include?(0..7)  
    # => false
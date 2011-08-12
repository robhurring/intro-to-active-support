!SLIDE
# Array Extensions
## require 'active_support/core\_ext/array'

!SLIDE bullets incremental
# Array#to_sentence

!SLIDE code

    @@@ ruby
    ['Earth'].to_sentence           
    # => "Earth"
    
    
    ['Earth', 'Wind'].to_sentence      
    # => "Earth and Wind"
    
    
    ['Earth', 'Wind', 'Fire'].to_sentence 
    # => "Earth, Wind, and Fire"


    users.map(&:name).to_sentence
    # "Bob, Dave, Chuck and Bill"
!SLIDE bullets incremental
# String#truncate
## Less is more.

!SLIDE code small

    @@@ ruby
    "Oh dear! Oh dear! I shall be late!".truncate(18)
    # => "Oh dear! Oh dea..."
    
    
    "Oh dear! Oh dear! I shall be late!".truncate(18, 
        :omission => '&hellip;')
    # => "Oh dear! O&hellip;"        
        
    
    "Oh dear! Oh dear! I shall be late!".truncate(18, 
        :separator => ' ')
    # => "Oh dear! Oh..."

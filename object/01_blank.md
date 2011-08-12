!SLIDE
# Core Extensions

!SLIDE
# Objects
## require 'active_support/core\_ext'
### Extensions to _all_ objects

!SLIDE bullets incremental small
# Object#blank? and Object#present?

* Checks for "nil" and "false"
* Strings made up of only whitespace
* Empty arrays and hashes
* Anything that responds to #empty?

!SLIDE code small

    @@@ ruby
    def ensure_session_key!
      raise ArgumentError, 'A key is required' if @key.blank?  
    end
    
    

    def set_conditional_cache_control!
      return if self["Cache-Control"].present?
      #...
    end
    
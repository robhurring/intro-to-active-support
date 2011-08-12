!SLIDE
# Hash Extensions
## require 'active_support/core\_ext/hash'

!SLIDE bullets incremental
# Hash#reverse_merge

* Useful when merging in defaults

!SLIDE code

    @@@ ruby
    class Cache
      Defaults = {ttl: 1.hour}
      
      def store(options = {})
        options.reverse_merge! Defaults
        puts options[:ttl]
      end
    end
    
    Cache.new.store
    # => 3600 (1.hour)
    
    Cache.new.store(ttl: 1.minute)
    # => 60 (1.minute)
    
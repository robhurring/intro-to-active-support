!SLIDE
# Class Extensions
## require 'active_support/core\_ext/class'

!SLIDE bullets incremental
# Class#cattr_accessor

* attr_accessor at the Class level
* Reduces boilerplate

!SLIDE code
    
    @@@ ruby
    class EZLaw
      def self.config=(config)
        @@config = config
      end

      def self.config
        @@config || {}
      end
    end
    
    EZLaw.config = {hello: 'World'}

!SLIDE code

    @@@ ruby
    # Refactors into this
    class EZLaw
      # Generates class methods to access 
      # @@config
      cattr_accessor :config
    end

    EZLaw.config = {hello: 'World'}

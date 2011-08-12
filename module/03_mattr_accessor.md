!SLIDE bullets
# Module#mattr_accessor

* attr_accessor for modules!

!SLIDE code
    
    @@@ ruby
    module EZLaw
      extend self

      def config=(config)
        @config = config
      end

      def config
        @config || {}
      end
    end

    EZLaw.config = {hello: 'World'}

!SLIDE code
    
    @@@ ruby
    # Refactors into this
    module EZLaw
      mattr_accessor :config
    end

    EZLaw.config = {hello: 'World'}

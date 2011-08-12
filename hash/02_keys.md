!SLIDE 
# Hash#except

!SLIDE code

    @@@ ruby
    # serialize all attributes except password
    class User
      def to_json
        attributes.except(:password).to_json
      end
    end
    

    {:a => 1, :b => 2}.except(:a) 
    # => {:b => 2}
    
!SLIDE 
# Hash#with_indifferent\_access

!SLIDE code

    @@@ ruby
    {:a => 1}.with_indifferent_access["a"] 
    # => 1
    
    
    {:a => :a}.stringify_keys
    # => {"a" => :a}
    
    
    {"a" => "a"}.symbolize_keys
    # => {:a => "a"}
    
!SLIDE code

    @@@ ruby
    yml = YAML.load <<-EOY
    ---
    cache: true
    email: you@example.com
    EOY
    
    # enable indifferent access
    yml = yml.with_indifferent_access
    
    
    yml['cache']
    # => true
    
    
    yml[:cache]
    # => true
    

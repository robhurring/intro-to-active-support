!SLIDE bullets incremental
# Class#class_attribute

* attr_accessor at the Class level
* shared with all subclasses
* can be overridden by subclasses

!SLIDE code small

    @@@ ruby
    class A
      class_attribute :x
    end

    class B < A
    end
    
    class C < B
    end

    A.x = :a
    B.x # => :a
    C.x # => :a

    B.x = :b
    A.x # => :a
    C.x # => :b 

    C.x = :c
    A.x # => :a
    B.x # => :b



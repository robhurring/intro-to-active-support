!SLIDE bullets incremental small
# Object#try?

* When you want to run a method on an object that _may_ be nil
* This is easy to abuse ಠ_ಠ

!SLIDE code small

    @@@ ruby
    class Person
      attr_accessor :name
    end

    person = Person.new

    puts person.try(:name) || 'Unknown'
    # => Unknown

    person.name = 'Joe'
    puts person.try(:name) || 'Unknown'
    # => Joe

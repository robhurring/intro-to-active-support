!SLIDE bullets incremental
# Date#change

* :year, :month, :day

# DateTime#change

* :hour, :min, :sec

!SLIDE code

    @@@ ruby
    d = Date.new(2010, 12, 23)
    
    
    d.change(:year => 2011, :month => 11)
    # => Wed, 23 Nov 2011

!SLIDE code

    @@@ ruby
    now = DateTime.current
    # => Tue, 08 Jun 2010 01:56:22 +0000


    now.change(:hour => 0)
    # => Tue, 08 Jun 2010 00:00:00 +0000
    
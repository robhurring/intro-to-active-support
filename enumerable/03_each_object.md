!SLIDE bullets incremental small
# Enumerable#each\_with_object

* similar to #inject
* with a twist.

!SLIDE code

    @@@ ruby
    [1, 2].inject({}) do |h, i| 
        h[i] = i + 1
        h # << easy to forget
    end 
    # => {1 => 1, 2 => 4}


    # note the inverted params
    [1, 2].each_with_object({}) do |i, h| 
        h[i] = i + 1
    end 
    # => {1 => 1, 2 => 4}
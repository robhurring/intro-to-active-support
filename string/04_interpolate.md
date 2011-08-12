!SLIDE bullets small incremental
# String#%
## sprintf with named places

!SLIDE code

    @@@ ruby    
    "I say %{foo}" % {:foo => "wadus"}          
    # => "I say wadus"

    
    "Total is %<total>.02f" % {:total => 43.1}  
    # => Total is 43.10

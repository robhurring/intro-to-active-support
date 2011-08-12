!SLIDE bullets incremental
# Array#wrap

* wraps objects in an array
* calls the #to_ary method if available

!SLIDE code

    @@@ ruby
    @servers = 'db.example.com'
    
    def reboot
      Array.wrap(@servers).each do |server|
        puts "rebooting: #{server}"
      end
    end
    
    reboot
    # => rebooting: db.example.com



    # Gotchas!    
    Array.wrap(:a => :b) # => [{:a => :b}]
    Array(:a => :b)      # => [[:a, :b]]

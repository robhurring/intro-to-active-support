!SLIDE
# Enumerable Extensions
## require 'active_support/core\_ext/enumerable'

!SLIDE bullets incremental
# Enumerable#group_by

!SLIDE code

    @@@ ruby
    users = User.all
    users_by_last_name = users.group_by do |user|
        user.last_name
    end
    # => {'Smith' => [#<User>, #<User>, ...]}



    (1..5).group_by{ |n| n & 1 }
    # => {1=>[1, 3, 5], 0=>[2, 4]}
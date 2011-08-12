!SLIDE bullets incremental small
# Enumerable#many?

* shorthand for size > 1

!SLIDE code

    @@@ ruby
    <% if pages.many? %>
      <%= pagination_links %>
    <% end %>
    
    
    @see_more = videos.many? do |video| 
      video.category == params[:category]
    end
    
    
    # be aware that:
    #   any? matches > 0,
    #   many? matches > 1
    
    [1].any?    # => true
    [1].many?   # => false
    [1,2].many? # => true
# pokemon-go-horse
Add this html code snippet to your web page to add a simple pokemon capture game.

## Includes
It includes jQueryUi and jQuery Throwable.

## Prank (how to use)
Just include the html snippet in your page's html.

It is fun to add this snippet to a webapp with a low probability of being run, like this code we used on our RubyOnRails app
```
  <% if !Rails.env.test? && current_user.manager? %>
    <% if rand <= 0.008 %>
      <%= render(:partial => "shared/pkmn") %> 
    <% end %>
  <% end %>
```

Or, if you want to prank individual users better:
```
  <% if !Rails.env.test? && current_user.manager? && current_user.client_id == 1 %>
    <% username_pkmn_encounter_probability = {
        'patrick' => 0.02,
        'henrique' => 0.05
      }
    %>
    <% if rand <= (username_pkmn_encounter_probability[current_user.username] || 0.008) %>
      <%= render(:partial => "shared/pkmn") %>
    <% end %>
  <% end %>
```

  With a small probability of appearing, the users will start trying to guess what causes the pokemons to appear:
  > "It appeared just after I grabbed a cup of coffee!"
  
  Enjoy & Help Improve!
  
## Credits
Henrique Gubert
Mauricio Moraes 

# Phoenix.LiveView behavior

## <u>Resources</u>
### Docs 
- Phoenix.LiveView behaviour
  https://hexdocs.pm/phoenix_live_view/Phoenix.LiveView.html#c:handle_params/3
  

## Anatomy of a liveview
- mount - Sets up the data for the initial page...
  - arguments -params / session / socket
  - return value - {:ok, socket}
- handle_event - Call back that updates data on the page
  - arguments - msg / meta_data / socket
  - return value - {:noreply, socket}
- render - Renders the LiveView to the browser

## Functional Components
* Allow you to layer logic to keep code clean and reusable
* Attributes
  * :attr - data being passed into the component
  * {} - attributes are interpolated with curly braces
* slots - Allows for rendering custom html inside a component.
  ```
  slot :inner_block
  ```


## Custom Interpolation
  
  - heex templates use {@value} to interpolate value into the template

- [[elixir]]
- [[elixir_phoenix]]
- [[index]]
- [[programming]]
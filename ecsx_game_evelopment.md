# ECSx_Game_Development

- [[index]]
- [[Game_Development]]

A new approach to game development in Elixir.

## Why is Elixir Not Used For Gamedev?

Standard Answers:
* Elixir is bad at math
  * Can be overcome with NIFs or NX
* Elixir is Immutable
  * Requires copying game struct
    * Can break up the data structure to make it more manageable

## Entity-Component-System

### What is Entity-Component-System

* Patter for where entities composed of components of data with systems which operate entities' components
  * Tick Rate - 
  * Component is basically an attribute (Height, Material,Wood, Velocity, ect)
* Entities are not restricted as to the type of components they can have
* Systems - Contributes the behavior to entities
* Tags - A component that provides information about the entity
  * eg IsHuman

### ECSx Generators
* ecsx.setup
* ecsx.gen.component(ComponentName type)
* ecsx.gen.system(SystemName)
* ecsx.gen.tag()

### ECSx.Manager
* Runs all systems
* Owner of all data tables and updates components
* Auto-updates with generators
* setup and startup
  * startup block - runs once
  * setup - Runs every time the manager runs

### Persistance

* Data is saved across reboots
  * HitPoints.add(char_id, @start_hp)
  * HitPoints.add(char_id, @start_hp, persist: true)
* Backup frequency is configurable
  * Defaults to file system
  * can use ecsx_persist_ecto

### Frontend Integration
* Clients have read-only access to Components
  * ECSx.ClientEvent.add(entity_id, event) where event is eg a keydown event
  * [{entity, event}, ...] = ECSx.ClientEvent.get_and_clear()

### ECSx LiveDashboard
* Adds an additional page to the Phoenix LiveDashboard
* Optional Dependency
* Tracks run times for each System
* Allows inspection of Component tables

### What's Next?
* Optimizations
* Turn-based games vs Ticks per second model
* Expand tutorial project

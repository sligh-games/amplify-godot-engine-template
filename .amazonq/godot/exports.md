# GDSCRIPTEXPORTS

1. BASIC EXPORT SYNTAX:
   ```gdscript
   # Basic exports
   @export var health: int = 100
   @export var name: String = "Player"
   @export var speed: float = 300.0
   
   # Resource exports
   @export var sprite: Sprite2D
   @export var material: Material
   ```

2. GROUP AND CATEGORY ORGANIZATION:
   ```gdscript
   # Category organization
   @export_category("Player Stats")
   
   # Group organization
   @export_group("Movement")
   @export var walk_speed: float = 300.0
   @export var run_speed: float = 600.0
   
   # Subgroup organization
   @export_subgroup("Advanced Movement")
   @export var acceleration: float = 10.0
   @export var deceleration: float = 5.0
   ```

3. PATH EXPORTS:
   ```gdscript
   # File paths
   @export_file var config_file
   @export_file("*.json") var json_file
   
   # Directory paths
   @export_dir var assets_folder
   
   # Global paths (tool mode only)
   @export_global_file("*.png") var global_image
   @export_global_dir var global_folder
   ```

4. RANGE LIMITATIONS:
   ```gdscript
   # Integer ranges
   @export_range(0, 100) var health: int
   
   # Float ranges with step
   @export_range(0, 1, 0.1) var opacity: float
   
   # Ranges with special modifiers
   @export_range(0, 100, 1, "or_greater") var level: int
   @export_range(0, 100, 0.1, "or_less", "or_greater") var scale: float
   
   # Exponential range
   @export_range(0, 100000, 0.01, "exp") var exp_value: float
   ```

5. COLOR EXPORTS:
   ```gdscript
   # Full color (with alpha)
   @export var primary_color: Color
   
   # Color without alpha
   @export_color_no_alpha var secondary_color: Color
   ```

6. NODE PATH EXPORTS:
   ```gdscript
   # Direct node reference
   @export var target_node: Node
   
   # Specific node type
   @export var character: CharacterBody2D
   
   # Node path
   @export var path: NodePath
   
   # Filtered node path
   @export_node_path("Button", "TouchScreenButton") var button_path
   ```

7. FLAGS AND ENUMS:
   ```gdscript
   # Bit flags
   @export_flags("Fire", "Water", "Earth", "Wind") var elements = 0
   
   # Explicit flag values
   @export_flags("Move:1", "Attack:2", "Defend:4") var actions = 0
   
   # Built-in flags
   @export_flags_2d_physics var collision_mask
   
   # Enums
   @export_enum("Warrior", "Mage", "Rogue") var character_class: int
   @export_enum("Low:0", "Medium:1", "High:2") var difficulty: int
   ```

8. ARRAY EXPORTS:
   ```gdscript
   # Basic array
   @export var items: Array[String] = []
   
   # Resource array
   @export var scenes: Array[PackedScene] = []
   
   # Typed packed arrays
   @export var positions = PackedVector2Array()
   @export var colors = PackedColorArray()
   ```

9. STORAGE AND CUSTOM EXPORTS:
   ```gdscript
   # Storage only (no editor visibility)
   @export_storage var stored_value: int
   
   # Custom property hints
   @export_custom(PROPERTY_HINT_RANGE, "0,100,1") var custom_range: int
   ```

10. MULTILINE TEXT:
    ```gdscript
    # Multiline text fields
    @export_multiline var description: String
    @export_multiline var script: String = "line 1\nline 2"
    ```

11. TOOL BUTTONS:
    ```gdscript
    # Button in inspector
    @export_tool_button("Reset", "Reset") var reset_action = reset_values
    
    func reset_values() -> void:
        health = 100
        notify_property_list_changed()
    ```

12. SUFFIXES AND UNITS:
    ```gdscript
    # Values with units
    @export_range(0, 100, 1, "suffix:m") var distance: float
    @export_range(0, 360, 0.1, "radians_as_degrees") var rotation: float
    ```
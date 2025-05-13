# GDSCRIPTSTYLE

1. FILE ORGANIZATION MUST FOLLOW THIS ORDER:
   ```gdscript
   # 1. Tool/Icon annotations
   @tool
   @icon("res://path/to/icon.png")
   
   # 2. Class declaration
   class_name ClassName
   extends BaseClass
   
   # 3. Description
   ## Class description and documentation
   
   # 4. Signals
   signal my_signal
   
   # 5. Enums
   enum State {IDLE, WALK, RUN}
   
   # 6. Constants
   const MAX_SPEED = 300
   
   # 7. Exported Variables
   @export var speed = 200
   
   # 8. Public Variables
   var health = 100
   
   # 9. Private Variables
   var _internal_state = 0
   
   # 10. Onready Variables
   @onready var _sprite = $Sprite2D
   ```

2. NAMING CONVENTIONS MUST FOLLOW:
   ```gdscript
   # Files: snake_case
   character_controller.gd
   
   # Classes: PascalCase
   class_name PlayerController
   
   # Functions: snake_case
   func move_character():
   
   # Variables: snake_case
   var player_health
   
   # Constants: SCREAMING_SNAKE_CASE
   const MAX_HEALTH = 100
   
   # Signals: snake_case
   signal health_changed
   ```

3. INDENTATION RULES:
   ```gdscript
   # Use tabs for indentation
   func my_function():
       if condition:
           do_something()
           
   # Multiline statements use double indent
   var result = some_long_function_name(
           parameter1,
           parameter2,
           parameter3
   )
   ```

4. LINE LENGTH AND FORMATTING:
   ```gdscript
   # Maximum line length: 100 characters
   
   # Break long lines
   var very_long_variable_name = (
       first_value +
       second_value +
       third_value
   )
   
   # Use trailing commas in multiline collections
   var items = [
       "item1",
       "item2",
       "item3",
   ]
   ```

5. SPACING RULES:
   ```gdscript
   # Space after keywords
   if condition:
   for item in items:
   
   # Space around operators
   var x = 5 + 3
   
   # Space after commas
   function_call(param1, param2, param3)
   
   # No space inside parentheses
   func my_function(param1, param2):
   ```

6. COMMENTS AND DOCUMENTATION:
   ```gdscript
   ## Documentation comments use double hash
   ## They must be above the item they document
   
   # Regular comments use single hash
   # And must have a space after the hash
   
   #region Region markers have no space
   #endregion
   ```

7. TYPE HINTS SHOULD BE USED AS FOLLOWS:
   ```gdscript
   # Explicit typing
   var health: int = 100
   
   # Return type hints
   func calculate_damage() -> int:
   
   # Type inference when obvious
   var vector := Vector2(1, 0)
   ```

8. SIGNAL CONNECTIONS SHOULD BE:
   ```gdscript
   # In _ready() function
   func _ready() -> void:
       signal_name.connect(_on_signal_name)
   
   # Handler naming
   func _on_signal_name() -> void:
   ```

9. VIRTUAL METHODS ORDER:
   ```gdscript
   func _init() -> void:
   func _enter_tree() -> void:
   func _ready() -> void:
   func _process(delta: float) -> void:
   func _physics_process(delta: float) -> void:
   func _input(event: InputEvent) -> void:
   ```

10. WHITESPACE ORGANIZATION:
    ```gdscript
    # Two blank lines between classes
    class_name ClassA
    
    
    class_name ClassB
    
    # One blank line between methods
    func method_one():
        pass
        
    func method_two():
        pass
    ```

11. ACCESS PATTERNS:
    ```gdscript
    # Public methods first
    func public_method():
        pass
        
    # Private methods last (with underscore)
    func _private_method():
        pass
    ```

12. ERROR HANDLING:
    ```gdscript
    # Use assert for development checks
    assert(condition, "Error message")
    
    # Use if/return for runtime checks
    if not condition:
        push_error("Error message")
        return
    ```

These style guidelines ensure consistency and readability across GDScript codebases. Follow them to maintain professional and maintainable code.
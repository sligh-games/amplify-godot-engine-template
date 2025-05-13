# GDSCRIPTSYNTAX

1. BASIC VARIABLE DECLARATIONS FOLLOW THIS SYNTAX:
   ```gdscript
   # Basic format: var name: type = value
   var score: int = 0
   var health := 100  # Type inference
   var is_active: bool = false
   var item_name: String = "Sword"
   ```

2. ARRAYS AND DICTIONARIES MUST BE DECLARED AS FOLLOWS:
   ```gdscript
   # Arrays
   var items: Array[String] = []  # Typed array
   var scores: Array = [1, 2, 3]  # Untyped array
   
   # Dictionaries
   var inventory: Dictionary = {
       "sword": 1,
       "shield": 2
   }
   ```

3. FUNCTION DECLARATIONS MUST FOLLOW THIS PATTERN:
   ```gdscript
   # Format: func name(param: type) -> return_type:
   func add_score(value: int) -> void:
       pass
       
   func get_health() -> int:
       return health
       
   # Optional parameters
   func spawn_enemy(type: String = "basic", level: int = 1) -> void:
       pass
   ```

4. CLASS DECLARATIONS MUST USE THIS SYNTAX:
   ```gdscript
   # Basic class
   class_name Player extends CharacterBody2D
   
   # Inner class
   class InnerItem:
       var name: String
       func _init(item_name: String) -> void:
           name = item_name
   ```

5. SIGNALS MUST BE DECLARED USING THIS SYNTAX:
   ```gdscript
   # Without parameters
   signal died
   
   # With parameters
   signal health_changed(old_value: int, new_value: int)
   
   # Emitting signals
   died.emit()
   health_changed.emit(old_health, new_health)
   ```

6. MATCH STATEMENTS MUST FOLLOW THIS STRUCTURE:
   ```gdscript
   match state:
       State.IDLE:
           process_idle()
       State.WALK:
           process_walk()
       _:  # Default case
           process_default()
   ```

7. CONTROL FLOW SYNTAX:
   ```gdscript
   # If statements
   if condition:
       statement
   elif other_condition:
       statement
   else:
       statement
       
   # For loops
   for item in items:
       process(item)
       
   # While loops
   while condition:
       process()
   ```

8. PROPERTY GETTERS AND SETTERS:
   ```gdscript
   var health: int:
       get:
           return _health
       set(value):
           _health = value
           health_changed.emit(_health)
   ```

9. EXPORT ANNOTATIONS MUST BE STRUCTURED AS:
   ```gdscript
   @export var speed: float = 100.0
   @export_range(0, 100) var volume: int = 80
   @export_enum("Sword", "Bow", "Staff") var weapon_type: String = "Sword"
   @export var custom_resource: Resource
   ```

10. STATIC TYPING AND ASSERTIONS:
    ```gdscript
    # Type casting
    var node := get_node("Path") as Node2D
    
    # Assertions
    assert(health >= 0, "Health cannot be negative")
    ```

11. COROUTINES AND AWAIT SYNTAX:
    ```gdscript
    # Await signal
    await get_tree().create_timer(1.0).timeout
    
    # Await function
    var result = await some_async_function()
    ```

12. ENUMS MUST BE DECLARED AS:
    ```gdscript
    # Named enum
    enum State {IDLE, WALK, RUN, JUMP}
    
    # Anonymous enum
    enum {WEAPON_SWORD, WEAPON_BOW, WEAPON_STAFF}
    ```

13. LAMBDA FUNCTIONS SYNTAX:
    ```gdscript
    var callback = func(value: int) -> void:
        print(value)
        
    # With name for debugging
    var named_lambda = func process_value(value: int) -> void:
        print(value)
    ```

14. PATTERN MATCHING SYNTAX:
    ```gdscript
    match value:
        1, 2, 3:
            print("Small number")
        var x when x > 100:
            print("Large number: ", x)
        _:
            print("Other number")
    ```

15. CLASS CONSTRUCTOR SYNTAX:
    ```gdscript
    func _init(param1: int, param2: String = "") -> void:
        # Initialize instance
        self.param1 = param1
        self.param2 = param2
    ```
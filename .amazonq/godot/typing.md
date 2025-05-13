# GDSCRIPTTYPING

1. BASIC TYPE DECLARATIONS:
   ```gdscript
   # Variable typing
   var health: int = 100
   var position: Vector2 = Vector2(0, 0)
   var active: bool = true
   
   # Constant typing
   const SPEED: float = 300.0
   const TILE_SIZE: int = 64
   
   # Function parameter and return typing
   func deal_damage(amount: int) -> void:
       health -= amount
   ```

2. TYPE INFERENCE RULES:
   ```gdscript
   # Using := for type inference
   var score := 0  # Inferred as int
   var name := "Player"  # Inferred as String
   var movement := Vector2()  # Inferred as Vector2
   
   # Constants are automatically typed
   const GRAVITY = 9.8  # Float type inferred
   ```

3. ARRAY TYPING:
   ```gdscript
   # Typed arrays
   var items: Array[String] = []
   var scores: Array[int] = [1, 2, 3]
   var nodes: Array[Node] = [$Player, $Enemy]
   
   # Invalid nested typing
   # var matrix: Array[Array[int]]  # Not supported
   ```

4. CLASS AND CUSTOM TYPE USAGE:
   ```gdscript
   # Using preloaded class as type
   const ItemClass = preload("res://item.gd")
   var my_item: ItemClass
   
   # Using global class_name
   class_name Player
   var player: Player
   
   # Inner class typing
   class InnerType:
       var value: int
   var inner: InnerType
   ```

5. TYPE CASTING RULES:
   ```gdscript
   # Safe casting with 'as'
   var node := get_node("Path") as Node2D
   
   # Type checking with 'is'
   if object is CharacterBody2D:
       process_character(object)
   
   # Unsafe cast handling
   var player := body as PlayerController
   if not player:
       return  # Cast failed
   ```

6. COVARIANCE AND CONTRAVARIANCE:
   ```gdscript
   # Parent class
   class_name Entity
   func get_data(param: Node) -> Resource:
       pass
       
   # Child class - contravariant parameter, covariant return
   class_name Player extends Entity
   func get_data(param: Node2D) -> ItemResource:
       pass
   ```

7. SIGNAL TYPING:
   ```gdscript
   # Signal with typed parameters
   signal damage_taken(amount: int, source: Node)
   
   # Typed signal connection
   func _on_hit(damage: int, attacker: Node) -> void:
       health -= damage
   ```

8. SAFE LINE PRACTICES:
   ```gdscript
   # Safe node access with typing
   @onready var sprite: Sprite2D = $Sprite2D
   
   # Safe type checking
   if sprite != null and sprite is Sprite2D:
       sprite.visible = false
   ```

9. ENUM TYPING:
   ```gdscript
   enum State {IDLE, WALK, RUN}
   var current_state: State = State.IDLE
   
   # Custom enum typing
   enum_types {
       TYPE_WEAPON = 0,
       TYPE_ARMOR = 1
   }
   var item_type: enum_types
   ```

10. ERROR PREVENTION:
    ```gdscript
    # Null checks with typing
    func process_item(item: Item) -> void:
        assert(item != null, "Item cannot be null")
        
    # Type validation
    func handle_collision(body: Node) -> void:
        if not (body is Player):
            return
    ```

11. DICTIONARY TYPING:
    ```gdscript
    # Type hints for dictionary values
    var inventory: Dictionary = {
        "weapon": weapon as Weapon,
        "armor": armor as Armor
    }
    ```

12. VOID RETURN TYPE:
    ```gdscript
    # Explicit void returns
    func initialize() -> void:
        health = 100
        position = Vector2.ZERO
    
    # Implicit void (not recommended)
    func initialize():
        health = 100
    ```
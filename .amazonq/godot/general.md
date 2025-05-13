# GDSCRIPTRULES

1. ALL SCRIPTS SHOULD HAVE A CLEAR CLASS PURPOSE AND BE PROPERLY NAMED WITH THE `.gd` EXTENSION.

2. SPECIFY THE FILE PATH WHEN PROVIDING CODE EXAMPLES:
   ```gdscript
   # res://scripts/player/movement.gd
   extends CharacterBody2D
   ```

3. WHEN CREATING NEW SCRIPTS, ALWAYS MENTION THE STEPS:
   ```
   1. Right click in the FileSystem panel
   2. Select "New Script"
   3. Choose the parent class
   4. Set the file path and name
   ```

4. ALL CODE SHOULD BE PROPERLY COMMENTED WITH:
   - Class purpose at the top
   - Function descriptions
   - Complex logic explanations
   ```gdscript
   # Player movement controller
   # Handles basic movement and animations
   extends CharacterBody2D
   
   # Speed of player movement in pixels/second
   @export var speed = 300
   
   func _physics_process(delta):
       # Calculate movement vector based on input
       var direction = Input.get_vector("left", "right", "up", "down")
       velocity = direction * speed
   ```

5. SIGNALS SHOULD BE DECLARED AT THE TOP OF THE FILE:
   ```gdscript
   signal health_changed(old_value, new_value)
   signal died
   ```

6. EXPORTED VARIABLES SHOULD BE GROUPED TOGETHER AFTER SIGNALS:
   ```gdscript
   @export var health: int = 100
   @export var speed: float = 300.0
   @export_range(0, 100) var damage: int = 10
   ```

7. PRIVATE VARIABLES SHOULD USE UNDERSCORE PREFIX:
   ```gdscript
   var _internal_state: Dictionary = {}
   var _cached_value: int = 0
   ```

8. BUILT-IN VIRTUAL FUNCTIONS SHOULD BE IN THIS ORDER:
   ```gdscript
   func _init() -> void:
       pass
       
   func _ready() -> void:
       pass
       
   func _process(delta: float) -> void:
       pass
       
   func _physics_process(delta: float) -> void:
       pass
       
   func _input(event: InputEvent) -> void:
       pass
   ```

9. CUSTOM FUNCTIONS SHOULD BE GROUPED BY FUNCTIONALITY WITH COMMENTS:
   ```gdscript
   # Movement functions
   func move_to_target() -> void:
       pass
       
   # Combat functions
   func apply_damage(amount: int) -> void:
       pass
   ```

10. USE TYPE HINTS WHEN POSSIBLE FOR BETTER CODE CLARITY:
    ```gdscript
    func calculate_damage(base_damage: int, multiplier: float) -> int:
        return int(base_damage * multiplier)
    ```

11. ENUMS SHOULD BE DECLARED AT THE TOP OF THE FILE AFTER SIGNALS:
    ```gdscript
    enum State {IDLE, WALK, RUN, JUMP}
    enum {WEAPON_SWORD, WEAPON_BOW, WEAPON_STAFF}
    ```

12. CONSTANTS SHOULD BE IN UPPERCASE WITH UNDERSCORES:
    ```gdscript
    const MAX_HEALTH: int = 100
    const PLAYER_DEFAULT_NAME: String = "Player"
    ```

13. ALWAYS USE AUTOLOAD NODES THROUGH THEIR SINGLETON NAME:
    ```gdscript
    # If GameManager is autoloaded as "Game"
    Game.current_score += 10
    ```

14. SCENE REFERENCES SHOULD USE PRELOAD:
    ```gdscript
    const BulletScene = preload("res://scenes/bullet.tscn")
    ```

15. NODE REFERENCES SHOULD USE ONREADY AND TYPE HINTS:
    ```gdscript
    @onready var _animation_player: AnimationPlayer = $AnimationPlayer
    @onready var _sprite: Sprite2D = $Sprite2D
    ```
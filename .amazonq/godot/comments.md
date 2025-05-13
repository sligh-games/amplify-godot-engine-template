# GDSCRIPTCOMMENTS

1. BASIC COMMENT TYPES:
   ```gdscript
   # Regular comment
   # Multiple line
   # comment
   
   ## Documentation comment
   ## Appears in editor help
   
   #region Named region
   # Code here
   #endregion
   ```

2. SCRIPT DOCUMENTATION:
   ```gdscript
   ## A brief description of the script
   ##
   ## Detailed description explaining functionality,
   ## usage, and important notes.
   ##
   ## @tutorial: https://example.com/docs
   ## @experimental: Still in development
   extends Node
   ```

3. MEMBER DOCUMENTATION:
   ```gdscript
   ## Signal documentation
   signal health_changed
   
   ## Enum documentation
   enum State {
       IDLE,    ## Idle state description
       WALK,    ## Walk state description
       RUN      ## Run state description
   }
   
   ## Variable documentation
   var health: int
   
   ## Method documentation
   ## @param amount The amount to heal
   ## @return Whether healing was successful
   func heal(amount: int) -> bool:
       pass
   ```

4. DOCUMENTATION TAGS:
   ```gdscript
   ## @deprecated: Use new_function() instead
   func old_function():
       pass
       
   ## @experimental: API may change
   func beta_feature():
       pass
       
   ## @tutorial: https://example.com
   ## @tutorial(Advanced): https://example.com/advanced
   func complex_feature():
       pass
   ```

5. BBCODE FORMATTING:
   ```gdscript
   ## Text can be [b]bold[/b], [i]italic[/i], or [u]underlined[/u]
   ## 
   ## Links to other elements:
   ## - [method some_method]
   ## - [member some_property]
   ## - [signal some_signal]
   ## - [constant SOME_CONSTANT]
   ```

6. CODE EXAMPLES:
   ```gdscript
   ## Usage example:
   ## [codeblock]
   ## var instance = MyClass.new()
   ## instance.setup()
   ## instance.process()
   ## [/codeblock]
   func setup():
       pass
   ```

7. INLINE DOCUMENTATION:
   ```gdscript
   var speed := 100.0 ## Movement speed in pixels/second
   
   const DAMAGE := 10 ## Base damage value
   
   func attack(): ## Performs attack action
       pass
   ```

8. PRIVATE MEMBERS:
   ```gdscript
   ## These won't appear in documentation
   var _private_var
   func _private_func():
       pass
   ```

9. FORMATTING RULES:
   ```gdscript
   ## Line breaks using [br]
   ## First line[br]
   ## Second line
   ##
   ## Lists:
   ## - Item 1
   ## - Item 2
   ##   - Sub item A
   ##   - Sub item B
   ```

10. LINKING AND REFERENCES:
    ```gdscript
    ## Links to other classes and members:
    ## See [Class] for more information
    ## Use [method Class.method_name]
    ## Access [member Class.property_name]
    ## Check [enum Class.EnumName]
    ```

11. KEYBOARD AND CODE:
    ```gdscript
    ## Press [kbd]Ctrl + S[/kbd] to save
    ##
    ## Use [code]instance.method()[/code] to call
    ##
    ## [codeblock]
    ## func example():
    ##     print("Multiple lines of code")
    ##     print("With proper formatting")
    ## [/codeblock]
    ```

12. COLOR AND STYLING:
    ```gdscript
    ## [color=red]Important warning[/color]
    ## 
    ## [center]Centered text[/center]
    ##
    ## Using custom font: [font=res://fonts/mono.ttf]Code[/font]
    ``
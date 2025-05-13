# GDSCRIPTWARNINGS

1. BASIC WARNING CONTROL:
   ```gdscript
   # Ignore single warning
   @warning_ignore("unused_variable")
   var my_unused = 5
   
   # Ignore multiple warnings
   @warning_ignore("unused_variable", "unused_parameter")
   func unused_func(unused_param):
       var unused = 10
   ```

2. WARNING REGIONS:
   ```gdscript
   # Start ignoring warnings
   @warning_ignore_start("unused_variable", "unused_parameter")
   
   func test1(unused1):
       var unused2 = 5
       
   func test2(unused3):
       var unused4 = 10
   
   # Restore warning checks
   @warning_ignore_restore
   ```

3. COMMON WARNING TYPES:
   ```gdscript
   # Unused variable warning
   @warning_ignore("unused_variable")
   var unused = 5
   
   # Unused parameter warning
   @warning_ignore("unused_parameter")
   func test(unused_param):
       pass
   
   # Untyped declaration warning
   @warning_ignore("untyped_declaration")
   var my_var
   
   # Unsafe property access warning
   @warning_ignore("unsafe_property_access")
   func test_access(node: Node):
       node.undefined_property = 5
   ```

4. TYPE-RELATED WARNINGS:
   ```gdscript
   # Inferred type warning
   @warning_ignore("inferred_declaration")
   var inferred := "string"
   
   # Narrowing conversion warning
   @warning_ignore("narrowing_conversion")
   var float_val: float = 1.5
   var int_val: int = float_val
   
   # Integer division warning
   @warning_ignore("integer_division")
   var result = 5 / 2
   ```

5. METHOD WARNINGS:
   ```gdscript
   # Return value discarded warning
   @warning_ignore("return_value_discarded")
   func test():
       some_function_with_return()
       
   # Unreachable code warning
   @warning_ignore("unreachable_code")
   func test():
       return
       print("unreachable")
   ```

6. PROPERTY WARNINGS:
   ```gdscript
   # Shadowed variable warning
   @warning_ignore("shadowed_variable")
   var value = 5
   func test():
       var value = 10  # Shadows outer value
       
   # Unused class variable warning
   @warning_ignore("unused_class_variable")
   var unused_class_var = 5
   ```

7. SIGNAL WARNINGS:
   ```gdscript
   # Unused signal warning
   @warning_ignore("unused_signal")
   signal unused_signal
   
   # Unconnected signal warning
   @warning_ignore("unconnected_signal")
   signal my_signal
   ```

8. BUILT-IN METHOD WARNINGS:
   ```gdscript
   # Override warning
   @warning_ignore("native_method_override")
   func get_class():
       return "MyClass"
       
   # Redundant await warning
   @warning_ignore("redundant_await")
   func test():
       await some_non_coroutine()
   ```

9. CONFIGURATION IN PROJECT SETTINGS:
   ```gdscript
   # Location: Project Settings > GDScript
   # Common settings:
   # - Treat warnings as errors
   # - Enable specific warnings
   # - Disable specific warnings
   ```

10. WARNING SEVERITY LEVELS:
    ```gdscript
    # Error level (prevents compilation)
    # Warning level (allows compilation)
    # Disabled (no warning shown)
    ```

11. BEST PRACTICES:
    ```gdscript
    # Document warning ignores
    @warning_ignore("unused_variable")  # Used for debugging
    var debug_var = 5
    
    # Group related warning ignores
    @warning_ignore("unused_variable", "unused_parameter")
    func debug_function(debug_param):
        var debug_local = 10
    ```

12. DEBUGGING WITH WARNINGS:
    ```gdscript
    # Check warning list in editor
    # - Status bar shows warning count
    # - Warning panel shows details
    # - Click warnings to navigate to source
    ```
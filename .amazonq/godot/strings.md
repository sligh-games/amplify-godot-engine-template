I'll create a markdown file for GDScript string formatting rules:
# GDSCRIPTSTRINGS

1. FORMAT STRING BASICS:
   ```gdscript
   # Basic placeholder %s
   var text = "Hello %s!" % "World"
   
   # Multiple placeholders
   var msg = "%s has %s points" % ["Player", 100]
   
   # Escape % with %%
   var percent = "Progress: %d%%" % 75  # "Progress: 75%"
   ```

2. PLACEHOLDER TYPES:
   ```gdscript
   # String conversion
   "%s" % value  # Convert any value to string
   
   # Character
   "%c" % 65  # "A" (ASCII/Unicode point)
   
   # Integers
   "%d" % 42    # Decimal: "42"
   "%x" % 255   # Hex lowercase: "ff"
   "%X" % 255   # Hex uppercase: "FF"
   "%o" % 64    # Octal: "100"
   
   # Floats
   "%f" % 3.14     # Float: "3.140000"
   
   # Vectors
   "%v" % Vector2(1, 2)  # "(1.000000, 2.000000)"
   ```

3. FORMAT MODIFIERS:
   ```gdscript
   # Show positive sign
   "%+d" % 42  # "+42"
   
   # Padding with spaces
   "%5d" % 42   # "   42"
   
   # Padding with zeros
   "%05d" % 42  # "00042"
   
   # Right alignment
   "%-5d" % 42  # "42   "
   
   # Float precision
   "%.2f" % 3.14159  # "3.14"
   
   # Combined modifiers
   "%+08.2f" % 3.14  # "+0003.14"
   ```

4. STRING.FORMAT() METHOD:
   ```gdscript
   # Dictionary style
   "Hello {name}!".format({"name": "John"})
   
   # Array style
   "Hello {0}!".format(["John"])
   
   # Mixed style
   "{name} is {0} years old".format([25, {"name": "John"}])
   
   # No index style
   "Hello {}!".format(["John"], "{}")
   ```

5. DYNAMIC PADDING:
   ```gdscript
   # Dynamic width and precision
   "%*.*f" % [10, 2, 3.14159]  # Width 10, 2 decimals
   
   # Dynamic zero padding
   "%0*d" % [5, 42]  # "00042"
   ```

6. STRING CONCATENATION:
   ```gdscript
   # Basic concatenation
   var name = "John"
   var text = "Hello " + name + "!"
   
   # With type conversion
   var score = 100
   var msg = "Score: " + str(score)
   ```

7. FORMAT METHOD CUSTOMIZATION:
   ```gdscript
   # Custom placeholder style
   var text = "Hi {0}".format(["John"], "{_}")  # Infix
   var text = "Hi 0%".format(["John"], "_%")    # Postfix
   var text = "Hi %0".format(["John"], "%_")    # Prefix
   ```

8. COMBINED FORMATTING:
   ```gdscript
   # Combining format() and % operator
   var text = "Score: {0}".format(["%0.2f" % 42.3456])
   ```

9. VECTOR FORMATTING:
   ```gdscript
   # Vector2 formatting
   "%v" % Vector2(1.1, 2.2)    # "(1.100000, 2.200000)"
   
   # Vector3 formatting
   "%v" % Vector3(1, 2, 3)     # "(1.000000, 2.000000, 3.000000)"
   ```

10. NUMBER FORMATTING:
    ```gdscript
    # Integer alignment
    var scores = [
        "%5d" % 42,    # "   42"
        "%5d" % 1337,  # " 1337"
        "%5d" % 3,     # "    3"
    ]
    
    # Float precision
    var prices = [
        "%7.2f" % 3.14,    # "   3.14"
        "%7.2f" % 42.123,  # "  42.12"
        "%7.2f" % 1.1,     # "   1.10"
    ]
    ```

11. ERROR PREVENTION:
    ```gdscript
    # Safe string formatting
    if typeof(value) == TYPE_INT:
        return "%d" % value
    else:
        return "%s" % value
    ```

12. PERFORMANCE CONSIDERATIONS:
    ```gdscript
    # Prefer format strings over concatenation
    # Good
    var text = "Player %s: %d" % [name, score]
    
    # Less efficient
    var text = "Player " + name + ": " + str(score)
    ```
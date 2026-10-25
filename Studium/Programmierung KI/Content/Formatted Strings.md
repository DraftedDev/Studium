# Basic Variable Insertion & Concatenation
- **Concatenation (`+`):** Combines strings and variables using the addition operator.
```python
print("Hello " + name + "!")
```

- **Basic F-String:** Embeds variables directly inside strings using curly braces `{}`.
```python
print(f"My name is {name} and I am {age} years old.")
```
# Alignment and Padding (`<`, `>`, `^`)
- **Left-align (`<`):** Pads spaces to the right of the string.
```python
f"{name:<10}"  # Result: 'Alice     '
```

- **Right-align (`>`):** Pads spaces to the left of the string.
```python
f"{name:>10}"  # Result: '     Alice'
```

- **Center-align (`^`):** Distributes padding spaces evenly on both sides.
```python
f"{name:^10}"  # Result: '  Alice   '
```
# Number Formatting & Padding (`010.2f`)
Control numeric display, width, zero-padding, and decimal precision:
- `0`: Pads the output with leading zeros instead of spaces.
- `10`: Total width of the resulting field.
- `.2f`: Formats the number as a float rounded to 2 decimal places.
```python
number = 3.14159
print(f"{number:010.2f}")  # Result: 0000003.14
```
# String Truncation (`.precision`)
When applied to strings rather than numbers, the precision specifier limits the maximum number of characters displayed:
- `.10`: Restricts the output to a maximum length of 10 characters.
```python
to_long_to_print = "Incomprehensibilities"
print(f"{to_long_to_print:.10}")  # Result: Incomprehe
```
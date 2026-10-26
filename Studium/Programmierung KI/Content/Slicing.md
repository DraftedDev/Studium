# Core Syntax Breakdown
`sequence[start:stop:step]`
- **`start`**: The index where the slice begins (**inclusive**). Defaults to `0` if omitted.
- **`stop`**: The index where the slice ends (**exclusive**—the item at this index is not included). Defaults to the end of the sequence.
- **`step`**: The stride or jump between items. Defaults to `1` if omitted.
# Common Slicing Patterns & Examples
## Basic Slicing
```python
text = "Python"
print(text[1:4])  # Result: 'yth' (captures indices 1, 2, and 3)
```
## Omitting Start or Stop

- **From the beginning up to an index (`:stop`):**
```python
print(text[:3])   # Result: 'Pyt' (indices 0, 1, 2)
```
- **From an index to the end (`start:`):**
```python
print(text[2:])   # Result: 'thon' (indices 2 to the end)
```
## Negative Indices
Negative numbers count backward from the end of the sequence (where `-1` is the last item).
```python
print(text[-3:])   # Result: 'hon' (last 3 characters)
print(text[:-2])   # Result: 'Pyth' (all characters except the last 2)
```
## Using Steps (`step`)
```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(numbers[1:8:2])  # Result: [1, 3, 5, 7] (every 2nd item from index 1 up to 8)
```
## Reversing a Sequence
A negative step traverses the sequence backward.
```python
print(text[::-1])  # Result: 'nohtyP' (reverses the string completely)
```
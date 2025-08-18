### Important Idea - List Comprehension

Without

```Python
# Create an empty list
squared_numbers = []

# Loop through numbers 0 to 4
for x in range(5):
  # Square each number and append it to the list
  squared_numbers.append(x ** 2)
```
With

```Python
squared_numbers = [x ** 2 for x in range(5)]
```

I tried an easier one and had much better success
```Python
def square_sum(numbers):
    total = 0
    for x in numbers:
      total = total + (x ** 2)
```
However I would like to take note and remember of a cleaner way, using "sum" instead of having to write out total = 0
```Python
def square_sum(numbers):
  return sum(pow(x, 2) for x in numbers)
```

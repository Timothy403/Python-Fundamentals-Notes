### Kata
Sum all the numbers of a given array ( cq. list ), except the highest and the lowest element ( by value, not by index! ).

The highest or lowest element respectively is a single element at each edge, even if there are more than one with the same value.

Mind the input validation.

Example
{ 6, 2, 1, 8, 10 } => 16
{ 1, 1, 11, 2, 3 } => 6
Input validation
If an empty value ( null, None, Nothing, nil etc. ) is given instead of an array, or the given array is an empty list or a list with only 1 element, return 0.

### Solution
```Python
def sum_array(arr):
    if arr is None or len(arr) < 2:
        return 0
    else:
        sorted_array = sorted(arr)
        short_array = sorted_array[1:-1]
        total = sum(short_array)
    return total
```
### Notes
This one was tricky, I tried to use sort instead of sorted, I didnt know about "if "" is None" and this was my original ordering
```Python
def sum_array(arr):
    sorted_array = sorted(arr)
    short_array = sorted_array[1:-1]
    if arr is None or len(arr) < 2:
        return 0
    else:
        total = sum(short_array)
    return total
```
Which didn't work because when a None value would be inputed it would try and sort it before reaching my if return 0 clause. So now I know the importance of always starting your program by checking for bad inputs.

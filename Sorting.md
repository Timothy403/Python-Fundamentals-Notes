#Sort vs Sorted

```Python
def sum_array(arr):
    if arr == None:
        return 0
    else:
        sorted_arr = sorted(arr) # arr.sort()
        sliced_arr = sorted_arr[1:-1]
    return sum(sliced_arr)
```

arr.sort may look cleaner however it is not recommended usually as it can have "side affects" due to modifying the original list
sorted() is more *Pythonic* because its creates a new sorted list, preventing potential common bugs where a function unexpectedly changes the input data

to be even more *Pythonic* you could use:
```Python
def sum_array(arr):
    return sum(sorted(arr)[1:-1]) if arr and len(arr) > 1 else 0
```

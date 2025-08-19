#Sort vs Sorted

```Python
def sum_array(arr):
    if arr == None:
        return 0
    else:
        sorted_arr = sorted(arr)         # arr.sort()
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
This might look weird but it still works because the sorted function is carried out before the slicing and then the sum is carried out after the slicing,
this will always be true as it has to follow *operator precedence*

You may have noticed how in the first example the *sorted* function required a new variable,       * side-note- you cannot use .sort to create a new variable as it returns *None*
obviously this is because you need to call it again to do something with it,
so why is this not the case in the second example?
The one-line solution works without a new variable because it chains a series of operations together, passing the result of each step directly to the next
aka you don't need to hold the results 

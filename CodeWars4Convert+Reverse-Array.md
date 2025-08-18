### Kata:Convert Number to Reversed Array of Digits
"Given a random non-negative number, you have to return the digits of this number within an array in reverse order."

### Solution
```Python
def digitize(n):
    
    int_array = []
    str_array = str(n)
    for s in str_array:
        int_array.append(int(s))
    reversed_array = list(reversed(int_array))
    return reversed_array 
```
### Notes
I learned of the "append" and "reversed" functions, you use append to add onto the end of a list and reversed reverses the order without modifying it.
"list()" or "tuple()" etc, need to come before "reversed()"

### One Liners
I find it useful to check and try to understand other peoples more efficient solutions and learn the functions they use and the logic they apply, e.g.

```Python
def digitize(n):
    return map(int, reversed(str(n)))
#-------------------------------------------
def digitize(n):
    return [int(x) for x in str(n)[::-1]]
```

the map function takes the given function (int) and applies it to every input (list) , which in this case, has first been turned into a string and reversed.

 [::-1] is Slice Notation, start:stop:step. The :: indicate that start:stop: are set to default and the -1 (step) tells Python to start at the end and step back (-) once at a time.

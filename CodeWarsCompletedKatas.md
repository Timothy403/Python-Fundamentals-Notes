### ### The KataTraining
"Write a function that takes an array of numbers and returns the sum of the numbers. The numbers can be negative or non-integer. If the array does not contain any numbers then you should return 0."

### ### The solution

Python```
def sum_array(a):
    numsum = 0
    if len(a) < 1:
        return 0
    else:
        for x in a:
            numsum = numsum + x
    return numsum
```

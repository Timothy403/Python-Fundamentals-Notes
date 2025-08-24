### Task
high_and_low("1 9 3 4 -5") # return "9 -5"

### My solution
```Python
def high_and_low(numbers):                                               
    digit = list(map(int, numbers.split()))
    return(str(max(digit)) + " " + str(min(digit)))
```
### Issues
The final outcome is good but I forgot about split and struggled, I really need to search up functions more as there are so many in Python..

### Better solution
```Python
def high_and_low(numbers):
    nums = [int(n) for n in numbers.split()]
    return f"{max(nums)} {min(nums)}"
```
List comprehension seems very common so I should try and make my own secondary solutions with one before checking the answers.

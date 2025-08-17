### ### Challenge 
"If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.
Additionally, if the number is negative, return 0.
Note: If a number is a multiple of both 3 and 5, only count it once.


### What I learned ###
you can have a while loop or "if" statement without an "else"
 -I learned about "for i in range"        # "i" is a placeholder variable created when you use a for loop
  for "" in    goes through every item in a list, range is a numerical list 
```Python
for i in range(3)
print(i)             #the output would be 0, 1, 2

for i in range(1,4)
print(i)             #the output would be 1, 2, 3
```

- I learned that the () placeholder can define a variable "number", in this case, in "def solution(number)"
```Python
def solution(number):
    total_sum = 0

    current_number = number - 1            #number will have a value once the function is called
```


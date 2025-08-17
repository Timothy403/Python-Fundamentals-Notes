### ### Challenge 
"If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.
Additionally, if the number is negative, return 0.
Note: If a number is a multiple of both 3 and 5, only count it once."


### What I learned ###
you can have a while loop or "if" statement without an "else"
 I realised that the "i" in "for i in range"    is a placeholder variable created when you use a for loop
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

- I think this is stupidly simple but need to be noted..
you make a variable and make it = to 0 so it can exist and be empty and then in a loop you can use it as a sort of counter or storage by sayign:
"x = x" and then some operation after it, im realising as i write that it would have to be a "1" instead of a "0" if you want to multiply
and then
```Python
total_sum = 0
total_sum = total_sum + current_number
```
you must return to end a while loop or def and usually you need to return aka output the data, in this case total_sum, for it to be useful

- lastly I understood I needed to use % to check for a multiple but I did not know the correct syntax, I wrote:
  ```Python
  multiple = (number % 5) or (numebr % 3)
  if multiple == 0:
  # and the correct way is:
  if number % 3 == 0 or number % 5 == 0:
  ```
 The correct way is to ask two complete, separate questions and connect them with or so it actually checks true/false instead of assigning a "more correct" numerical value to the variable "multiple"

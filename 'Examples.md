### Perfect Crab Dictionary and Challenge 1

## Dictionary counter
```Python
def count_words_by_length(words):
    letter_count = {}
    for word in words:
        if len(word) not in letter_count:        #
         letter_count[len(word)] = 1             # l = len(c)
        else:                                    # letter_count[l] = letter_count.get(l, 0) + 1   
            letter_count[len(word)] += 1         #
    return letter_count
```
## Long words / Challenge 1
```Python
def report_long_words(words):
    word_list = []
    for word in words:
        if len(word) > 10 and "-" not in word:
            if len(word) < 15:
              word_list.append(word)
            else:
              word_list.append(word[:15] + "...")
        else:
            continue
    worded = ", ".join(word_list)
    return f"These words are quite long: {worded}"

####################################################################################################

def report_long_words(words):
  processed = [w[:15] + "..." if len(w) > 15 else w for w in words if len(w) > 10 and "-" not in w]
       joined = ", ".join(processed)
       return f"These words are quite long: {joined}"
```
### Simple count Kata
```Python        #my_list.count(value) → int
def count_sheeps(arrayOfSheeps):    # in this case the array is True,True,False,
  return arrayOfSheeps.count(True)  # it can be any other iterable, like a letter in a string
```
### Katas
## List filter:    digits from strings
```Python
return [x for x in digitstring if type(x) == int]      #######  isinstance(x, int)

##########################################################################

filtered = []
for x in digitstring:
    if isinstance(x, int)           #######    if type(x) == int:
        filtered.append(x)
return filtered
```
## ("abcd") -> "A-Bb-Ccc-Dddd"
```Python
return ("-".join(x.upper() + x.lower() * i for i, x in enumterate(text)))
```
## String to array
```Python
return string.split() #or# string.split(' ')
```
## Simple map()  No.2 from highest and lowest Kata
```Python
list(map(int, str(n))) # a list of single digits from a larger number
list(map(int, n.split())) # splitting a white spaced numbers into single integers and then listing them
list(map(int, num) # turning a list of digit strings into a list of integers
# map can also apply upper and len, etc.
```
## nth term + 2 decimal places
```Python
def nth_term(n) -> str:
    total = 0.0
    divisor = 1
    for _ in range(n)                      _ can be used when you dont need to use the temporary variable again
    total = total + 1 / divisor
    divisor += 3
return f"{total:.2f}"
```
## Capitalize all words in a string
```Python
def to_jaden_case(string):
    capitalized = []
    splittext   = string.split()        #splits strings by whitespace as default
    for w in splittext:
        capitalized.append(w.capitalize())

    return " ".join(capitalized)
```
## Using set for Isograms
```Python
def is_isogram(string):
    string = string.lower()
    set_check = set(string)             #sets can only have unique elements
    if len(string) == len(set_check):
         return True 
    else:
         return False
```
## Dictionary used as stock checker
```Python
def fillable(stock, merch, n):
    for item in stock:
        if item == merch:                 #item aka key in stock    
            return stock[item] >= n           # return stock.get(merch, 0) >= n         
        else:
             continue
```
## multiple squared digits joined (not added) from one original number
```Python
joinable = (str(int(x) ** 2) for x in str(num))         #needs to be an int while calculating and a string while placing together (not addition) 
    return int("".join(joinable))
```
## two smallest numbers in an array
```Python
def sum_two_smallest_numbers(numbers):
    smallest = float('inf') 
    second = float('inf')
    for d in numbers:
        if d < smallest:
            smallest, second = d, smallest
        elif d < second:
            second = d
    return smallest + second     #or# return sum(sorted(numbers)[:2])
```
 ## "8 j 8   mBliB8g  imjB8B8  jl  B" -> "8j8mBliB8gimjB8B8jlB"
 ```Python
return "".join(s.split()) #or# s.replace(" ", "")
```
### Sorting dictionaries by max, Kata
```Python
def sort_dict(d):
    remaining = d.copy()       # copy so original dictionary is not affected
    result    = []            #empty list to put key: value tuple into eventually
    
    while remaining:         #true/loop while not empty, stops when all keys deleted
    
        max_val = None      # starting values, could also be -infinity
        max_key = None
        
        for k in remaining:         #check/iterate through all the keys
            v = remaining[k]                    #first pass always takes v and is max_val as greater than none
            
            if max_val is None or v > max_val:     #every later iteration the new v is compared to old max_val
                max_key = k                    # after looping through every v (value), or maybe just the first if it was the biggest
                max_val = v                # you have your largest value and coresponding key and those are ready to be appended
            
        result.append((max_key, max_val))       #adding that loops largest value to the list
        
        del remaining[max_key]         # one largest value has been extracted,
                                       # now you need to remove it so the second loop can find what the second biggest value is
    return result

########################################

def sort_dict(d):
  return sorted(d.items(), key=lambda x: x[1], reverse=True)       #not mine (CodeWars) but this seems a lot more simple... need to learn lambda next

```


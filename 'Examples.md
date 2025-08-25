### Long words / Challenge 1
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
### List filter:    digits from strings
```Python
return [x for x in digitstring if type(x) == int]      #######  isinstance(x, int)

##########################################################################

filtered = []
for x in digitstring:
    if isinstance(x, int)           #######    if type(x) == int:
        filtered.append(x)
return filtered
```
### ("abcd") -> "A-Bb-Ccc-Dddd"
```Python
return ("-".join(x.upper() + x.lower() * i for i, x in enumterate(text)))
```
### String to array
```Python
return string.split() #or# string.split(' ')
```
### Simple map()  No.2 from highest and lowest Kata
```Python
list(map(int, str(n))) # a list of single digits from a larger number
list(map(int, n.split())) # splitting a white spaced numbers into single integers and then listing them
list(map(int, num) # turning a list of digit strings into a list of integers
# map can also apply upper and len, etc.
```
### nth term + 2 decimal places
```Python
def nth_term(n) -> str:
    total = 0.0
    divisor = 1
    for _ in range(n)                      _ can be used when you dont need to use the temporary variable again
    total = total + 1 / divisor
    divisor += 3
return f"{total:.2f}"
```
### Capitalize all words in a string
```Python
def to_jaden_case(string):
    capitalized = []
    splittext   = string.split()        #splits strings by whitespace as default
    for w in splittext:
        capitalized.append(w.capitalize())

    return " ".join(capitalized)
```
### Using set for Isograms
```Python
def is_isogram(string):
    string = string.lower()
    set_check = set(string)             #sets can only have unique elements
    if len(string) == len(set_check):
         return True 
    else:
         return False
```
### Dictionary used as stock checker
```Python
def fillable(stock, merch, n):
    for item in stock:
        if item == merch:                 #item aka key in stock    
            return stock[item] >= n           # return stock.get(merch, 0) >= n         
        else:
             continue
```
### multiple squared digits joined (not added) from one original number
```Python
joinable = (str(int(x) ** 2) for x in str(num))         #needs to be an int while calculating and a string while placing together (not addition) 
    return int("".join(joinable))
```




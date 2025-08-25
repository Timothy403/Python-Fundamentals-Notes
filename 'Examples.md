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
    for _ in range(n)
    total = total + 1 / divisor
    divisor += 3
return f"{total:.2f}"
```
### Capitalize all words in a string
```Python
def to_jaden_case(string):
    capitalized = []
    splittext   = string.split()
    for w in splittext:
        capitalized.append(w.capitalize())

    return " ".join(capitalized)
```
### Using set for Isograms
```Python
def is_isogram(string):
    string = string.lower()
    set_check = set(string)
    if len(string) == len(set_check):
         return True 
    else:
         return False
```

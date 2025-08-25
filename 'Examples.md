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

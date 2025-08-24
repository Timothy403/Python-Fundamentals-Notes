### Dictionaries

* dictionary is a way to store and get() values by their keys

* created with {}

* key is called with []

* it goes key and then value------key: value,--------------------or   key: value, key: value, key: value
*  -----------------------------------key: value,---------------------
* e.g. ------------------------------key: value---------------------the main importance being the order and seperation by a comma *,*

* the first beginner way to add onto a dictionary is:
*  dictionary[new_key] = new_value
*  dictionary.get(key, default_value)

  If you are counting in a loop and your dictionary is empty, make sure to set the key and therefore value equal to 1

  Alternatively you can use .get() to avoid messing around with a loop. 
```Python
def counting(num)
dict = {}
 for item in dict:
    if item not in dict:
        dict[item] = 1
    else:
        dict[item] = dict[n] + 1
  return dict
```

VS

```Python
def counting(num)
dict = {}
for item in num:
  dict[item] = dict.get(item, 0) + 1
return dict
```

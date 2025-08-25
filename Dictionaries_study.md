Creation:
  #empty
- d1 = {} 
- d2 = dict()

  #adding
- scores = {"alice": 10, "bob": 12}  (adds new keys and maps values to them)

 Membership
- Direct lookup: (error if missing)
- scores["alice"]   -> 10
- scores["tim"]  -> KeyError

Testing presence:
- if "carol" in scores:
-   print("found carol")
- else:
-   print("could not find carol")

Safe access with .get()
- scores.get("key")   # = None     safe because doesn't crash/error
- scores.get("key", 0))   # = 0

Insertion and updating:
- data = {}
- data["x"] = 1     is inserting a new key     {"x": 1}
- after,  data["x"] = 5      updating the value of the same key    {"x": 5}
- ```Python      
  for item in  ["a",  "b", "c", "a"]:      # get finds it, need the = to actually change the value of that item key
    data[item] = data.get(item, 0) + 1     # get(item   gets the value, +1 adds onto it, for that specific key,
  return data # = "a": 2, "b": 1  etc      #"a" is brought up twice (same key) so its value gets +1 twice (2)
  ```
 Deletion:
 ```Python
 d = {"a":1, "b":2, "c":3}

del d["b"]   #removes entry. dict is now {"a":1, "c":3}      not as safe as pop

val = d.pop("c", 0)   #   val=3       d = {"a":1}     removes entry but also returns the removed value
val2 = d.pop("z", 0)  #    val2=0      d = {"a":1}     does nothing and defaults to 0 instead of error/crashing
 ```
Iteration:
```Python
d = {"a":1, "b":2, "c":3}

      # Over keys only
for key in d:
  print(key, d[key])        # d[key] is calling the value of that key

      # Over key-value pairs
for key, val in d.items():
  print(key, val)
```

Stock scenario:
```Python
stock = {"apple": 5, "banana": 2, "orange": 0}

statuses = []
for item in stock:
  count = stock[item]
  statuses.append(f"{item}: {count} is in stock")

print(statuses)
# -> ["apple: 5 in stock", "banana: 2 in stock", "orange: 0 in stock"]





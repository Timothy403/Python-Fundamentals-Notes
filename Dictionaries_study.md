### Creation
Empty:
- d1 = {} 
- d2 = dict()

Adding:
- scores = {"alice": 10, "bob": 12}  (adds new keys and maps values to them)

### Membership
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

Insertion and updating
- data = {}
- data["x"] = 1     is inserting a new key     {"x": 1}
- after,  data["x"] = 5      updating the value of the same key    {"x": 5}
- ```Python      
  for item in  ["a",  "b", "c", "a"]:
    data[item] = data.get(item, 0) + 1     # get finds it, need the = to actually change the value of that item key
                                           # get(item   gets the value, +1 adds onto it, for that specific key, "a" is brought up twice (same key) so its value gets +1 twice (2)
  ```

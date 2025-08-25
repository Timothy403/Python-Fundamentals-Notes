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
-

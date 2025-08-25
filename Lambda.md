### Learning lambda.md

```Python
def sort_dict(d):
  return sorted(d.items(), key=lambda x: x[1], reverse=True)
```

* .items() gets the key value pairs
*  If d = {3:1, 2:2, 1:3}, then
pairs is an iterable over [(3,1), (2,2), (1,3)].

to be continued.......

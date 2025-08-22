### Task
accum("abcd") -> "A-Bb-Ccc-Dddd"
accum("RqaEzty") -> "R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy"
accum("cwAt") -> "C-Ww-Aaa-Tttt"

### Solution
you can use both capitalize and upper/lower
I tried using upper/lower where the actual answer would be
```Python
def accum(st):
    return (str("-".join(x.upper() + (x.lower() * i) for i, x in enumerate(st))))
```

### Failed Solution
```Python
def accum(st):
    return ("-".join( upper(x), lower(x) * i ) for x, i in enumerate(st))
```
### What I was missing
* I thought the order for enumerate was item, index
* I forgot it was a generator and it wouldn't output something unless told what it was meant to come out as
* I didn't know how to correctly call upper as variable.upper()
* I thought I could add upper and lower strings with a , inside of .join. .join only takes one iterable and goes through it, therefore you need to concatate the upper and lower strings before with +

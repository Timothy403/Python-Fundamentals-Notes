### Task
n
1 --> 1 --> "1.00"
2 --> 1 + 1/4 --> "1.25"
5 --> 1 + 1/4 + 1/7 + 1/10 + 1/13 --> "1.57"

### My solution
```Python
def series_sum(n):
    total = 0
    divisor = 0
    for x in range(n):
        divided = 1 / (1 + divisor)
        divisor += 3
        total += divided
    return str(round(total))
```

### Issue
"1.00" would be returned as "1.0"

### Fix
Use a "Format specifier"
So either
*f-string* - return f"{total:.2f}"
or
*format()* - return "{:.2f}".format(total)

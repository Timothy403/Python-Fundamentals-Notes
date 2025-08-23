### simple Syntax and logic error

```Python
def is_isogram(string):
    seen = []
    lower_string = string.lower()
    for c in lower_string:
        seen.append(c)
        for x in seen:
            if x in seen:
                return False
        else:
            seen.append(c)
            return True

```

I almost got it right on my own but for some reason I was adding before checking so it will always be false (checking the same added character),
by checking first and appending last, a new loop starts and a new character is checked compared to the old one

return False and True cannot both be part of the loop otherwise it won't loop, so be mindful of the indentation for *return* (*True* in this case)

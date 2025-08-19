### Repeated notes or notes that will be sorted in the future

I have made this file because I thought I could try a harder challenge by now however it took a while and I got a bit sidetracted and want to write down everything I learned

* Level 6 kyu

Implement a function that computes the difference between two lists. The function should remove all occurrences of elements from the first list (a) that are present in the second list (b). The order of elements in the first list should be preserved in the result.

Examples
If a = [1, 2] and b = [1], the result should be [2].

If a = [1, 2, 2, 2, 3] and b = [2], the result should be [1, 3].


```Python
def array_diff(a, b):
    return [x for x in a if x not in b]

Show Variations
def array_diff(a, b):
    new_list = []
    for item in a:
        if item not in b:
            new_list.append(item)
    return new_list
```

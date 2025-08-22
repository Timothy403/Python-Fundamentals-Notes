### Level 6 kyu

Implement a function that computes the difference between two lists. The function should remove all occurrences of elements from the first list (a) that are present in the second list (b). The order of elements in the first list should be preserved in the result.
If a = [1, 2] and b = [1], the result should be [2].
If a = [1, 2, 2, 2, 3] and b = [2], the result should be [1, 3].


```Python
def array_diff(a, b):
    return [x for x in a if x not in b]

########################################

def array_diff(a, b):
    new_list = []
    for item in a:
        if item not in b:
            new_list.append(item)
    return new_list
```

These are the two solutions I will be looking at, the later, less *Pythonic* solution is what I eventually got to but I made many errors on the way, such as:

* trying to use *in* instead of not in, the *in* operator checks for the complete object (the entire list). [2] != 2
* trying to convert the list into integers with map(int, str(b)) (so I could use *in*), unessecarily complicated and wouldn't work anyway because *str* converts everything including the brackets. map applies the function to everything, resulting in an error when using *in* on "[" "]"
* trying to call/build the whole (a, b) list and then using .remove which would succeed when removing the first item but then throwing out an error when looping to remove items from an already empty list.
* probably the worst logical error was trying to use .remove and .append with list comprehension which is completely contradictory as the later creates a list and .remove/.append modify lists and return None values, so naturally when Python tried to create the list it would result in [None]                                           ****REMEMBER****

If i want to use *side effects* (modifying an existing list) I need to use a for loop instead of a list comprehension
Don't assume a function like *in* would work in Python as it seems in english
Don't spend so long on a question out of my league, ask and learn instead of creating more problems with more convoluted code

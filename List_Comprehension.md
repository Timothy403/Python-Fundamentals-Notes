### What it is

```Pyton
new_list = [expression for item in iterable]
```
its slightly confusing because its using two new imaginary objects with the same name ("x" in this case) but different actions
In english, reading left to right, the first one (experssion) is "what do you want to do to this?" and the second one (item) is the standard for loop placeholder "I am the current item from the iterable"
In python, working inwards to outwards, "item" is the generator which provides items one by one from the iterable to the transformer "expression" which transforms the provided item (which must be called) by performing an action

```Python
list_from_number = [int(x) for x in str(n)]
#for improved learning/readability ill write it as
list_from_number = [int(character) for character in str(n)]
#because even though it ends up as a integer/digit and it comes from a digit/number,
the for loop is going through it as iterable characters after it has been turned into a string
 and the expression is transforming it back into an integer
```
### When to use it

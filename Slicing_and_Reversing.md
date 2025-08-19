### Continuining from List_Comprehension
```Python
list_from_number = [int(character) for character in str(n)]
```
At first I thought to put the *step* into the expression "int(character)[::-1]" but it does not work as reversing is not an operator but a syntax operator.
Meaning it has to be attatched to an object, in this case, it has to be the list once it is created OR *str(n)* which is also an already completed object.
* Therefore you have have the choice to place it:
```Python
list_from_number = [int(character) for character in str(n)][::-1]     #here
                                                                  #or
list_from_number = [int(character) for character in str(n)[::-1]]     #here
```

If you only want the reversed list/lists then the second option would be better because it is more memory efficient 
because you are only reversing and storing small strings compared to two integer lists

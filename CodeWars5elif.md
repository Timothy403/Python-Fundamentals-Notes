### Kata
Grade book
Complete the function so that it finds the average of the three scores passed to it and returns the letter value associated with that grade.

Numerical Score	Letter Grade
90 <= score <= 100	'A'
80 <= score < 90	'B'
70 <= score < 80	'C'
60 <= score < 70	'D'
0 <= score < 60	'F'

### Solution
```Python
def get_grade(s1, s2, s3):
    score = (s1 + s2 + s3) / 3
    if score >= 90:
        return 'A'
    elif score >= 80:
        return 'B'
    elif score >= 70:
        return 'C'
    elif score >= 60:
        return 'D'
    else:
        return 'F'
  ```

### Notes

I learned to use elif, especially in the right order, my first try I started with F and ended with A
```Python
if score <= 60:
  return "F"
elif score >= 60:
  return "D"
elif score >= 70:
  return "C"
```
but every score would be greater than 60 so all would be returned as "F" or "D", I fixed this by adding an "and"
```Python
if score <= 60:
  return "F"
elif score >= 60 and score <= 70:
  return "D"
elif score >= 70 and score <= 80:
  return "C"
```
this works however it is too long and sligtly confusing, I now know that logically it makes sense to start with the higher scores so it either returns them and finishes, or moves onto the next elif if it fails. Instead of always succeeding at the first step.

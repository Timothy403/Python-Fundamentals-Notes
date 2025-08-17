### ### Operators

- `+` (Addition)
- `-` (Subtraction)
- `*` (Multiplication)
- `/` (Division)
- `%` (Modulo/Remainder)

### ### Forms

- `x = 1` : integers
- `x = 1.1` : floats (decimals)
- `x = a + bi` : complex numbers

### ### Division

Standard python division `/` is decimal division, meaning that 2/5 is 2.5 and is not automatically rounded towards 0 (as in other languages).

If you want to do that then you need to type `//`. Rounding 2/5 down (not the same as towards 0) to 2.

```python
# Standard division
print(5 / 2)
# Expected output: 2.5

# Integer division (floor division)
print(5 // 2)
# Expected output: 2
```

### ### Remainders

Modding, like division, is not the same as most languages when negative.

```python
print(10 % 3)
# Expected output: 1

print(-10 % 3)
# Expected output: 2
```

A useful example of this in action is with calendars or anything that uses cycles where you want the number to be positive without needing extra `if` statements. e.g. days of the week = 0-6, you want to know what day it was 39 days ago, you do `-39 % 7` and get an obvious, positive `3` instead of `-4`.

### ### Math Helpers

If you do need a negative answer you need to import the `math` module.

```python
import math

# fmod provides standard remainder calculation as seen in C and other languages
print(math.fmod(-10, 3))
# Expected output: -1.0
```

#### Other helpers of note:

- **math.sqrt(x)**: Calculates the square root of a number. `math.sqrt(25) -> 5.0`
- **math.ceil(x)**: Rounds a number up to the nearest integer. `math.ceil(7.2) -> 8`
- **math.floor(x)**: Rounds a number down to the nearest integer. `math.floor(7.9) -> 7`
- **math.pow(x, y)**: Raises x to the power of y. `math.pow(2, 3) -> 8.0`
- **math.pi**: Provides the constant Pi (π). `math.pi -> 3.141...

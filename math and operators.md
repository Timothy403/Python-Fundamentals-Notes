###Operators

"+" (Addition)

"-" (Subtraction)

"*" (Multiplication)

"/" (Division)

"%" (Modulo/Remainder)

###Forms

x = 1            :     integers                               
x = 1.1          :     floats (decimals)    
x = # a + bi     :     complex numbers



###DIVISION
Standard python division is "/" which is decimal division, meaning that 2/5 is 2.5 and it is not automatically roudned towards 0 (as in other languages)
If you want to do that then you need to type "//", rounding 2/5 down (not the same as towards 0) to 2
However since its rounding "down", print(-3 // 2) = -2 instead of -1.5 to -1
the solution is to use int, print(int(-3 // 2)) = -1

###REMAINDERS
modding, like division, is not the same as most languages when negative
'''python
print(10 % 3)
# Expected output: 1
print(-10 % 3)
# Expected output: 2
'''
why is this the case and why can it be useful instead of wrong? because python uses the sign of the second value so it has to be positive and works through (-7, -4, -1, 2)
a useful example of this in action is with calendars or anything that uses cycles where you want the number to be positive without needing extra IF statements
eg. days of the week = 0-6,  you want to know what day it was 39days ago, you do (-39 % 7) and get an obvious, positive 3 instead of -4. So you and the app/website easily know it was thursday.

###MATHS HELPERS
continuing from modding
if you do want a negative answer you need to

import math                 #importing the math module
print(math.fmod(-10, 3))           #fmod = standard remainder calculation as seen in C and other languages

Other helpers of note.

math.sqrt(x)	    Calculates the square root of a number.              	math.sqrt(25) -> 5.0
math.ceil(x)	    Rounds a number up to the nearest integer.	          math.ceil(7.2) -> 8
math.floor(x)	    Rounds a number down to the nearest integer.	        math.floor(7.9) -> 7
math.pow(x, y)    Raises x to the power of y.	                          math.pow(2, 3) -> 8.0
math.pi	          Provides the constant Pi (π).	                        math.pi -> 3.141...

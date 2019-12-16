*Python Notes*
<h1>(WHEN VIEWING IN GITHUB, ALWAYS CHOOSE "Raw" TO PREVENT PYTHON FORMATTING!!)</h1>
<h6>(Best viewed in Visual Studio Code)</h6>

Python treats words not in quotes as commands.

Arithmetics are same as JavaScript and follow PEMDAS. (+, -, *, /, %)

When the result of a division is a decimal, it will be rounded to a whole number. To get the decimal, change the numerator/denominator to a float.

When a multi-line string is not assigned to a variable, it becomes a multi-line comment.

**DEFINITIONS:**
-_Editor:_ The area where we write our code.
-_Integer:_ Whole number with no decimal point
-_Float:_ Number with a decimal point ('e' can be used for scientific notation. float = 1.5e2)
-_Dot Notation:_ (lion.upper()) Only works with string

**COMMANDS**
_To display text._
    _Python 2:_ print "Enter your text here"
    _Python 3:_ print("Enter your text here")

_Combining two strings._
print "Hello" + "Jeremy"

_Multi-line Strings._
address_string = """136 Whowho Rd
Apt 7
Whosville, WZ 44494"""

_Using an apostrophe (')_
'There\'s a snake in my boot.'

_Changing integer to string._
age = 16
print "I am " + str(age) + " years old."

_Changing string to integer._
number1 = "100"
number2 = "10"
int_addition = int(number1) + int(number2)

_Keep float when using int()_
string_num = "7.5"
print float(string_num)

_Using boolean._
age_is_16 = True
name_is_dave = False

_Using variables._
greeting_message = "Welcome to Python!"

_Using indexes._
c = "cats"[0]

_Using arithmetic operators._
test_addition = 98234 + 7834
use_combinations = 35 * 235 + 345 / 235 - 85

_Finding float in a division._
quotient = 7./2
quotient = 7/2.
quotient = 7./2.
quotient = float(7)/2

_Leaving comments._
# This is a comment

**VARIABLES:**
Variables are used to define things that are subject to change.

_Using variables._
greeting_message = "Welcome to Python!"

_Updating Variables:_
money_in_wallet = 40
sandwich_price = 7.50
sales_tax = .08 * sandwich_price

sandwich_price += sales_tax
money_in_wallet -= sandwich_price

**STRING METHODS:**
_len()_ Gets the length of a string.
bird = "Blue"
print len(bird)

_lower()_ Turns all characters into lowercase.
"Ryan".lower()

bird = "Blue"
print bird.lower()

_upper()_ Turns all characters into uppercase.
bird = "Blue"
print bird.upper()

_str()_ Turns non-string into string.
str(2048)

_String formatting with %_ The % is used to combine a string with variables. %s are placeholders.
string_1 = "Camelot"
string_2 = "place"

print "Let's not go to %s. 'Tis a silly %s." % (string_1, string_2)
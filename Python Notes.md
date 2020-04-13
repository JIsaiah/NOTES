*Python Notes*
<h1>(WHEN VIEWING IN GITHUB, ALWAYS CHOOSE "Raw" TO PREVENT PYTHON FORMATTING!!)</h1>
<h6>(Best viewed in Visual Studio Code)</h6>

Python treats words not in quotes as commands.

Arithmetics are same as JavaScript and follow PEMDAS. (+, -, *, /, %)

When the result of a division is a decimal, it will be rounded to a whole number. To get the decimal, change the numerator/denominator to a float.

When a multi-line string is not assigned to a variable, it becomes a multi-line comment.

**DEFINITIONS:**
-_Environment:_ A housing which contains different tools and packages for each project. Imagine this as a house with furniture. Environments can be made and deleted freely.
-_Editor:_ The area where we write our code.
-_Integer:_ Whole number with no decimal point
-_Float:_ Number with a decimal point ('e' can be used for scientific notation. float = 1.5e2)
-_Dot Notation:_ (lion.upper()) Only works with string

**MINICONDA VS ANACONDA**
These are both package managers. Miniconda only includes Python and Jupyter Notebook. Anaconda includes Python, Numpy, Jupyter Notebook, and more. The only difference is that one includes more tools than the other, just like choosing between buying an empty house or one that is fully furnished. The choice exists due to storage size differences since you might not use all the tools which will take up space.

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

**ARRAYS:**
Inclusive:Exclusive
Arrays start from 0

_Get range from array:_
e.g. a = [0, 1, 2, 3, 4]

a[0:3] = [0, 1, 2]
a[:5] = [0, 1, 2, 3, 4]
a[::-1] = [4, 3, 2, 1, 0]

_Check amount in array:_
e.g. a = [0, 1, 2, 3, 4]

len(a) = 5

_Adding to an array:_
e.g. a = [0, 1, 2, 3, 4]

a.append(5) = [0, 1, 2, 3, 4, 5]

_Joining string:_
a = ['dog', 'cat', 'fish']

','.join(a) = 'dog,cat,fish'
'+'.join(a[0]) = 'd+o+g'

_Splitting string:_
a = 'Array Content 1'
b = 'Hello, this is my array'

a.split() = ['Array', 'Content', '1']
b.split(',') = ['Hello', 'this is my array']

**DICTIONARIES**
a = {'cat': 'kucing', 'dog': 'anjing', 'fish': 'ikan'}

_Accessing a value:_
a['cat'] = 'kucing'
-Cat is the key, kucing is the value. You can only access the value using the key-

_Add new entry:_
a['pig'] = 'babi' = {'cat': 'kucing', 'dog': 'anjing', 'fish': 'ikan', 'pig': 'babi'}

_Look up all keys:_
a.keys()

dict_keys(['cat', 'dog', 'fish'])

_Look up all values:_
a.values()

dict_values(['kucing', 'anjing', 'ikan'])

_Update a value:_
a['cat'] = 'tikus'

a = {'cat': 'tikus', 'dog': 'anjing', 'fish': 'ikan'}

_Remove a value:_
a.pop('cat')

a = {'dog': 'anjing', 'fish': 'ikan'}

_Replace multiple values at once:_
a.update(dict.fromkeys(['dog', 'fish'], 'kucing'))

a = {'dog': 'kucing', 'fish': 'kucing'}

**CONDITIONALS**
e.g. score = 50

if 0 <= score < 60:
    print("index: C")
elif 60 <= score < 80:
    print("index: B")
elif 80 <= score < 100:
    print("index: A")
elif score == 100:
    print("index: S")
else:
    print("Fail")

Result = "Index: C"

**FUNCTIONS**
e.g. def total(a,b)
        return a + b

    total(10,11) =  21

e.g. scores = [90, 80, 60, 70]

    mean = 0
    for score in scores:
        mean = mean + score
    mean / len(scores)

    Result = 75.0

**LOOPS**
e.g. numbers = [1, 2, 3, 4, 5, 6]

    for i in numbers:
        print(i + 1) = 2 3 4 5 6 7

e.g. numbers = [1, 2, 3, 4, 5, 6]

    for i in numbers:
        i = i**2
        print(i) = 1 4 9 16 25 36

e.g. animals = ['fish', 'cat', 'elephant']

    for animal in animals:
        print(animal) = fish cat elephant

    for animal in animals:
        print(animal.upper()) = FISH CAT ELEPHANT

**NUMPY**
Importing with numpy is importing functions made by other people. These are used to save time and use more efficient functions, usually mathematical formulas. You can only use numpy functions with NumPy arrays (Numpy arrays have the text 'array' in the front).

_Make an array:_
numbers = np.arange(0, 11, 2)

array([ 0, 2, 4, 6, 8, 10])
-The two at the end is to signify jumps in digits-

_Sum an array:_
numbers = array([ 0, 2, 4, 6, 8, 10])

numbers.sum() = 30

_Linspace:_
numbers = np.linspace(0, 10, 5)

array([ 0., 2.5, 5., 7.5, 10.])
-Number at the end is how many zeroes in between-

_Logspace:_
numbers = np.logspace(-3, 3 ,7)

array([1.e-03, 1.e-02, 1.e-01, 1.e+00, 1.e+01, 1.e+02, 1.e+03])
-Number at the end is the power-

_Random(RNG):_
np.random.rand(3,2)

array([[0.3077662 , 0.40693044],
       [0.86609681, 0.15790726],
       [0.68423774, 0.61636793]])
-The 3 is the amount of rows, 2 is the amount of columns-

_Controlled Randomness(Rigged RNG):_
np.random.RandomState(3)
-3 is interchangeable-

np.random.RandomState(1)
state.randint(1, 10, 5) = array([6, 9, 6, 1, 1])
-1 and 10 is the range, 5 is how many numbers will be chosen at random-
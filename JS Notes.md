*JavaScript Notes*
<h1>(WHEN VIEWING IN GITHUB, ALWAYS CHOOSE "Raw" TO PREVENT JAVASCRIPT FORMATTING!!)</h1>
<h6>(Best viewed in Visual Studio Code)</h6>

If you stack variables, the previous one will be replaced when displayed with 'console.log()'.
End commands with a semicolon; It is usually not required but is needed in some cases and is best to practice using semicolons.
JvS reads the newest entry of code and if there copies of a variable with different values, the newest value will override the older value.



**DEFINITIONS:**
-_Syntax:_ The rules that specify the correct combined sequence of symbols that can be used to form a correctly structured program.

-_Variable:_ A name of a storage location. (e.g. "var number= 5;")

-_Operator:_ Performs oeprations on a single/multiple operand(s) (data value) and produces a result.

-_Snake case:_ Using an underline to separate words. (e.g. "type_number")

-_Camel case:_ Using an uppercase letter to separate words. (e.g. "typeNumber")

-_Branching:_ When you stack 'if's and 'else's.



**DATA TYPES:**
-_Number_ (idk what these are)

-_String_ (Characters/letters) Always add quotation marks to make the type a string. (' weakest, " stronger, ` strongest.)

-_Boolean_(True or false, yes or no, etc.)



**OPERATOR TYPES:**
_Assignment Operator:_ An operator that assigns a value.

_Arithmetic Operator:_ An operator that does math using the functions below.
  + Addition
  - Subtraction
  * Multiplication
  / Division
  % Remainder (Divides the first number by the second number and returns the numerator of the division. Returns 1 (Has remainder) or 0 (Has no remainder).)

_Comparison Operator:_ An operator that compares one value with another. Answers in boolean.
  -Equal operator "==": To only compare variables.
  
  -Strict equal operator "===": To also compare types.

  -Strict not equal operator "!==": To compare different values and types.

  -Less than/Greater than "<>": To compare values.


_Conditional Operator:_ Will evaluate the truth from a value.
  -OR "||": Will result in 'true' if anything contains true.
  
  -AND "&&": Will result in 'true' only if all premises are true.

    e.g. A system verifies students and teachers for room entrance. Using 'OR',     if the person is not a teacher (false) but is a student (true), they       are allowed in.
         Using 'AND', if the person is a teacher (true), but not a student (false), they will not be allowed access because not all premises are true.



**COMMANDS:**
_To declare a variable:_
var name =

_To display data entered inside the brackets:_
console.log()

_Setting a password:_
  var password 'hi world';
  if password('hi world'){
      console.log("Welcome in!")
  }
    else{
        console.log("The password is incorrect.")
    }

_Switch-case conditional scenario:_
(switch = the variable affects the command, 
break = tells the program where to end the command if executed, 
default = the command that will be executed if no premises are met.)

  var buttonPushed= 1;
  switch(buttonPushed){
      case1: {console.log("Turn off TV");break;}
      case2: {console.log("Reduce volume");break;}
      case3: {console.log("Increase volume");break;}
      default: {console.log("Nothing happened");break;}
      }

_To allow a variable to be reassigned a different value:_
let

_Can store any value in a constant variable, cannot be reassigned:_
const/constant

_To execute a function:_
function name(parameter1, parameter2, parameter3){
  code to be executed
}

_To reset/erase an assigned value: (Leave a blank string)_
= ''

_To write a comment only visible to the programmer: (Mainly used for multiple line or inbetween code comments)_
/* text */

_To write a comment only visible to the programmer on only one line:_
// text

_To find the position of the first occurrence of a specified value in a string:_
indexOf()



**FUNCTIONS:**
The function is basically a giant container for code or a shortcut for running code. The code inside the function will execute when "something" calls the function:
  -When an event occurs (When the user clicks a button).
  -When it is called from JvS code.
  -Automatically

When JvS reaches a 'return' statement, the function stops. Functions compute a return value.

_To call a function:_
functionName(); when run, whatever is inside the function will be exectued.

_To execute a function:_
function name(parameter1, parameter2, parameter3){
  code to be executed
}

_e.g. executing a function_ 
  function makeTriangle(){
    var triangle = "*";
    for(s = '1'; s <= '5'; s++){
      console.log(triangle)
      triangle += "*"
    }
  }
  makeTriangle()              The code inside 'function makeTriangle()' will run when 'makeTriangle()'                                     is called.

_e.g. parameter function_
  function thisFunction(age){
    if(age > 17){
      console.log('Allowed in')
    else
      console.log('Not allowed in')
    }
  }

  function thisFunction(17)

_e.g. return function_
  function thisFunction(){
    return 'Jeremy'
  }
  var name = thisFunction()
  console.log(name)   

_e.g. math function_
  function thisFunction(a, b){
    console.log(a)
    console.log(b)
    return a - b
  }
  var number1 = 5
  var number2 = 7

  var result = thisFunction(number1)

  console.log(result)      



**MODULAR FUNCTIONS:**
_Reversing text_
var name = reverseText(name)

_Removing spaces_
var name = removeSpaces(name)

_e.g. Turn wirtimid => wjrtjmjd_
function updateVowels(text){
  var text = wirtimid
  var abjad = 'abcdefghijklmnopqrstuvwxyz'
  var vowels = 'aeiuo'
  var isThere = false
  var newUpdateVowels = ''
  for(i = 0; i < text.length; i++){
    for(j = 0; j < vowels.length; j++){
      if(text[i] === vowels[j]){
        isThere = true
      }
    }
    if(isThere === true){
      for(k = 0; k < abjad.length; k++){
        if(text[i] === abjad[k]){
          newUpdateVowels += abjad[k+1]
        }
      }
    } else{
      newUpdateVowels += text[i]
    }
  }
  return newUpdateVowels
}



**LOOPS:**
-WHEN DOING LOOPS, VARIABLES MUST ALWAYS BE DIFFERENT.

_While-loop:_
  while(condition){
      process
  }
The true or false value will be taken. If true, the process will run, if not, the process will not. The loop will continue to run until the condition is no longer true.

_For-loop:_
  for(initialisation, condition, incremental/decremental){
      process
  }
The 'for' statement becomes the controller of the loop. The statement will accomodate 3 parameters to control when the loop ends.



**REGEX(Regular Expression):**
Regex is an object that describes a pattern of characters. Basically finds text and gives a return value based on the results of the search.

var name = new RegExp("abc");

or

var name = /abc/;

_Using literal values:_
var regexPattern = new RegExp('[A-Z]');

var message = 'Regex itu Mudah!';
console.log(regexPattern.test(message));               Will check the message to see if there is a capital                                                            letter (from A-Z) in the message. Will return in true/                                                         false.
or

var message = 'Regex is simple!';
console.log(/[A-Z]/.test(message));                    Will check the message to see if there is a capital                                                            letter (from A-Z) in the message. Will return in true/                                                         false.
_Splitting:_
var str = 'learning regex is fun';
console.log(str.split(/\s/));                          Returns "learning, regex, is, fun" because \s splits the                                                       sentence every 'space'.

_Replacing:_
var string1 = 'Regex is very difficult!';
var string2 = string1.replace(/difficult/, 'easy');    Every 'difficult' text will be replaced with 'easy'.
console.log(string2);

_Match:_
var message = 'Regex is FUN!';                         Will search for the letter 'e' and will stop after the  console.log(message.match(/e/));                       first match.             

var message = 'Regex is FUN!';                         Will search for 'e'. The 'g' causes it to stop after    console.log(message.match(/e/g));                      all 'e's are found.

var message = 'Regex is FUN!';                         Will search for all 'e's. 'gi' causes it to find all    console.log(message.match(/e/gi));                     the 'e's while ignoring letter cases.

_Metacharacters:_
.: Find a single character, except newline or line terminator.
\w: Find a word character.
\W: Find a non-word character.
\d: Find a digit.
\D: Find a non-digit character.
\s: Find a whitespace character.
\S: Find a non-whitespace character.
\b: Find a match at the beginning.end of a word.
\B: Find a match, but not at the beginning/end of a word.
\0: Find a NUL character.
\n: Find a new line character.
\f: Find a form feed character.
\r: Find a carriage return character.
\t: Find a tab character.
\v: Find a vertical tab character.
\xxx: Find the character specified by an octal number xxx.
\xdd: Find the character specified by a hexadecimal number dd.
\udddd: Find the Unicode character specified by a hexadecimal number dddd.

_Quantifiers:_
n+: Matches any string that contains at least one n.
n*: Matches any string that contains zero or more occurences of n.
n?: Matches any string that contains zero or one occurences of n.
n{X}: Match any string that contains a sequence of X n's.
n{X,Y}: Matches any string that contains a sequence of X to Y n's.
n{X,}: Matches any string that contains a sequence of at least X n's.
n$: Matches any string with n at the end of it.
^n: Matches any string with n at the beginning of it.
?=n: Matches any string that is followed by a specific string n.
?!n: Matches any string that is not followed by a specific string n.



**ARRAYS:**
Used to store multiple values in a single variable. Results are overwritten with recent entries.
Counting with arrays starts at 0. [1, 2, 3] = [0, 1, 2]

var arrayName = [item1, item2, item3, ...];

arrayName[5]; to search for the 5th item in the array.

_Array functions:_
.push: Adds the element to the rearmost array index.
.pop: Erases an element from the rearmost array index.
.unshift: Adds the element to the frontmost array index.
.shift: Erases an element from the frontmost array index.
.join: (Only for string) Combines all array elements into a string.
.sort: Sorts all elements alphabetically.
.slice: Takes slices of data.
.splice: Changes array values by adding/removing new values.
.split: Breaks up a string into an array.
name.length: Automatically counts amount of arrays.

e.g. var array = []
     array.push(1)
     array.push(2)
     array.push(3)

     console.log(array[0])
     console.log(array[1])
     console.log(array[2])

Result will be 1, 2, 3.

e.g. var array = [0,1,2];
     array.unshift(3);

Result will be 3,0,1,2.

e.g. var array = [1, 84, 35, 7]
     array.sort(
       function(value1, value2) {return value 1 > value 2});

Result will be 1, 7, 35, 84. Without the function, the result will be 1, 35, 7, 84. The sort only reads the first digit.

e.g. var array = [0, 1, 2, 3, 4];
     var slice1 = array.slice(1,4)

Result will be 1, 2, 3. (1,4) = slice (1-4), the first parameter is not included in the slice. (1,1) = 0.

e.g. var array = ["book", "laptop, "computer"];
     var splice1 = array.splice(2, 0, "tv");

Result will be "book", "laptop", "tv", "computer". 2 = insert into that index. 0 = erase none

e.g. var sentence = "I am a programmer.";
     var word = sentence.split(" ");
     var combine = word.join("-")

Result I-am-a-programmer. ("-") = combine with -.

e.g. var sentence = "I am a programmer.";
     var word = sentence.split(" ");

Result "I", "am", "a", "programmer". (" ") = split by space.

e.g. var arr = [1, 2, 3]
     for (i = 0; i < arr.length; i++){
      console.log(arr[i])
     }

Result will be 1, 2, 3, ...

e.g. var arr = [1, 2, 3, 4, 5]
     var result = 0
     for(i = 0; i< arr.length; i++){
       if(arr[i]%2 === 0){
         console.log('genap')
       } else{
         console.log('ganjil')
       }
     }

Result will be ganjil, genap, ganjil, genap, ... until arr.length cap is reached.

_Multi-dimensional Arrays:_
An array inside an array.

e.g. var arr = [1, 2, 3, 4, 5];
     
     console.log(arr[0])

Result will be 1.

e.g. var arr = [[1, 2, [3]], 2, 3, 4, 5];
     
     console.log(arr[0][2][0]);

Result will be 3 (Use [0] to get rid of one layer of []).



**OBJECTS:**
Objects are variables that can contain many values. These can be called by using "objectName[index#]" or "objectName.propertyName". All other data types can be put inside an object.

e.g. var car = {type:"Fiat", model:"500", color:"white"};

"type:, model:, color:" are the object's 'Keys'.

Objects can be looped using keys.

e.g. for(key in car){
        console.log(car[key])
      }
This will loop through every key and display each key's contents.

e.g. var supermanObj={
        id: 123,
        name: 'stefany',
        address: {
          number: 55,
          street: 'radio dalam'
        },
        hobby: [1, 2, 3],
     };
     for(i in supermanObj){
       if(i === 'address'){
         for(j in address){
           console.log(supermanObj[i][j])
         }
       }
     }
This will display "55, radio dalam".



**RECURSION:**
Recursion is when a function calls itself inside itself, directly or indirectly. ALWAYS have a stopping command to prevent an infinite loop.

e.g. function factorial(n) {
     if (n <= 1) {
       return 1;
     } else {
       return n * factorial(n - 1);
       }
     }



**DOM (Document Object Model):**
Nodes: HTML element.
You cannot console.log elements from HTML in JavaScript. Instead use the browsers built in console.
You can use looping to access elements.

This is used to link HTML with JavaScript, and allows the JavaScript to access and change elements of the HTML and CSS. The HTML DOM is a standard for how to get, change, add or delete HTML elements. In the DOM, all HTML elements are defined as objects.

The DOM is a W3C (World Wide Web Consortium) standard, and is separated into 3 different parts:
-The Core DOM - The standard model for all document types.
-The XML DOM - The standard model for XML documents.
-The HTML DOM - The standard model for HTML documents.

Property: A value that you can get or set.
Method: An action you can do.

e.g. document.getElementById("demo").innerHTML = "Hello World!";
     In this example, getElementById is a method, innerHTML is a property.

!!!ALWAYS START COMMANDS WITH .document!!!

_Commands:_
getElementById(""): The easiest way to access an HTML element through its id.
document.getElementById("page-title")

.innerHMTL: To get or replace the content of an HTML element.
e.g. pageTitleElement.innerHTML = "Changed text here"

.getElementsByClassName(""): Lists all class names in an array.

.getElementsByTagName(""): Takes all elements within a specific tag and lists them in an array.

document.createElement(""): Creates an element inside the HMTL.

document.createAttribute(""): Creates an attribute inside the HTML.

"node".appendChild(): Put a node as the last child of that node.
e.g. document.getElementById("title").appendChild("new text");  

"node".removeChild(): Remove a child from that node.
e.g. var list = document.getElementById("myList");
     list.removeChild(list.childNodes[0]); 

"node".style."style type": Add a style to a HTML element.
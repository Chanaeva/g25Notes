#Programming
at it's basic level takes an input transforms it and gives you an output. Programs are made up of programs.

input to binary to logic-gates to processor to circuit   

##Communication
Sudo code is for people to understand when talking about code. Used to discuss concepts that
translate to different languages.

A programming language is something that can do these 4 things:
Sequence = control what order things happen in (order)
Selection = being able to pick parts of code to execute (conditions)
Iteration = repeating (loops)
Recursion

review side note - for in loop is for key for of loop is for value.

Structured English
using English to express computer stuff, using syntax of structured programming. A reduced language set then sudo code.
see
http://image.slidesharecdn.com/lecture4-090714220353-phpapp02/95/lecture-4-33-728.jpg?cb=1247609060

##Terms
Expression = is something that can be evaluated
Statement = instruction to the computer
Operator = used to evaluate something like + = - % > instanceOf typeOf && || ++
== delete in ?:
?: is the only ternary Operator
Three types of Operator
unary
binary
ternary
denoted by the number of operands not by the number of symbols

side note review - assertion is for tests
  two parenthesis after a function are called the invocation
  new js primative is symbol with js2015

##truthy vs falsy

falsy = false, 0, empty strings, null, undifined, NaN

everything else is truthy

edge case is something other than how it's going to happen in the computer

##Javascript
reference types
primitive values vs referencing types (objects, arrays, and function)
reference types - do not store data they point to where the data is stored, they are
based off of an object.
primitive values - store data such as strings, numbers, booleans, null, undefined...

scope  

##vocab
declaration = creating or making
assignment = setting a value
identifiers = variables, words that you use to point to another thing
keywords = IF, RETURN ... have special meaning  
literals = primative value types

##why Javascript

only natural/natively supported language that web-browsers read
only language you can use front and back isomorphic
sustained adoption - it's going to be around for a while, it's highly supportive and used by
major companies.

Javascript is a prototype-based with firs-class functions making it a multi-paradigm
language that supports object oriented

Run Javascript in relp.it and in terminal in node.

##types
string, boolean, number, undefined, null, undefined, objects

null vs undefined
undefined is lack of assignment to identifier
null is nothing, different from 0 as 0 is a number

how computers go through Javascript explains undefined...

create variables with var to avoid scope issues.

== is looking for value, it converts (corhersion) to similar types so they can be compared
for the value, ignores types
=== is looking for type and value, a strict comparison

##Environment
  where your running your stuff
  front-end Browsers
  back-end Server
      node
      nginx
      rhino
      televisions

      caniuse.com- to check compatibility

##Control Flow
the order statements of a program run determined by the code.

##Errors
Common Errors
  Reference Error = you probably made a typo, you tried to reference something that does't
  exist, could have not defined a variable.
  Type Error = performing an action on a value of the wrong type.
  syntax Error = you messed up the formula, possibly missing a curly bracket or mistyping
  "function"
  logic Errors = bugs written by developers

  2 main error families : runtime or compile-time

#Object
 objects are a list of key (property), value pairs contained in curly braces.

 a property is variable attached to object with a value.
 add property to object:
  in creation of variable or
  use dot notation
        cat.firstName = "Felix";
  use bracket notation
      cat["first name"] = "Felix"

 method is a property that's value is a function.just like a function it is followed by ()
 when called.

delete is an operator

Javascript inheritance is prototype, objects inherit properties all the way down the
nesting path
hasOwnProperty() returns a boolean indicating whether the object has the specified property
Object.keys([object]) returns the keys of an object.
  ex: Object.keys(cat);

  Object.values([object]) - new to 2015

  Iterator For In
    cannot use for loops on objects, but can be iterated through
    for in iterates over enumerable properties of an object, in arbitrary order
    returns value based on keys
    for(key in cat) {
      console.log(cat[key])
    }
 a for loop ( for (i=0; i<....)) is for arrays not for objects

#Arrays
arrays us a dynamic list in Javascript, it is a container for values in order,
0-indexed, of any type.
array literal is var array = []
var people = new array[] <-- don't use this Danny does not like this

"real arrays" other languages and computer science = collection of items of a single
type, has a defined number of items

methods on arrays
##Stack
a stack is a list where you can only add or remove from a single side, such as dishes
push and pop to add and remove from the stack

##Queues
queue is first in first out, shift (removes) and unshift (adds)

##Functions
A way to encapsulate code so that it can be reused.
functions accept parameters in parenthesis following the keyword "function" followed by
the {}, inside the {}, is the body where the stuff happens.

function declaration doesn't use var, function expression uses var =
stick to declaration.
to invoke a function call it, include parameters, even if it's empty  

pure vs non-pure function
non-pure mutates the argument

##return
console.log() is for humans, return is for the computer.
Return exits the function!

##parameters and arguments
parameters are when you define, creating local variables of non-specific type
arguments are when you invoke, when you call the function using values instead of the
parameters, arguments need to be a type.
"arguments" is a keyword only within a function but it is a keyword for the arguments.

##HigherOrder functions
 it is a function that takes a function as an argument or returns a function.
 when passing a function as an argument you don't include the parameter of the function
 with in the function because then you are invoking the function which means you are really
 calling the output of the function instead of the function.  

#Scope
scope refers to the variables you have access to.

##Global vs Local
Global -
Local - any scope defined past the global,

function scope- the rule, a new function creates a new scope, not loops or expression
statements. the opposite would be like block scope.

scope chain designates the scope for a given function.

Lexical scope or Closure is function within a function, the inner function has access to
the scope of the outer function.
The call-back function is the inner-function which is used because it's repetitive,
anonamous

hoist is the concept that the computer compiles all variables at the top.

see for scopes
https://toddmotto.com/everything-you-wanted-to-know-about-javascript-scope/
adripofjavascript

variable shadowing is the idea to use the same variable on a global and local scope, the
local variable will override the global within the function.

when a variable is declared inside a function without "var" it becomes global which is
usually bad

***function expression is var = function () {} ONLY THE VARIABLE IS HOISTED, NOT THE WHOLE FUNCTION.
this creates a "variable" so you
can get undefined, you can't use a variable before you've defined it.
function declaration is function () {} GETS HOISTED
Order matters so this matters

let and const in ES2015 have different scope not functional but block, which means
the



hints for project: use bracket for var bracket notation great for when you have to look up
variables inside loops.
var name = "wife"
var propertytype = "name"
kyle[name][propertytype]
to get "Elyse"
kyle = {
  wife{
    name: "Elyse"
  }
}

for(conditionalization; termination; iteration)

# Variables

## Declaration (creating a new variable)

- let
- const
- var

### let
This is the basic variable that you should be using.  
It is scoped, meaning that it is only accessible where it is declared.  
If I declare it in a function, you can only access it within that function.

Example: 
<pre>
let outside = "outside";  
function example() {  
  let inside = "inside";  
  // I can access outside and inside here
}  
// I can only access outside here  
// I can access inside
</pre>


### const
The same thing as let, but once it's set it cant be changed.
>const stands for constant

### var
The same idea as let, but I can access it anywhere, which can create problems if there are two functions with the same variable name.

Example:
<pre>
function a() {
  var x = 1;
  b();
  console.log(x);
}

function b() {
  var x = 2;
  console.log(x)
}

a();

// Output:
// 2
// 2
</pre>

But x was set to 1 in function a!

## Variable Types

### Basic Types
- boolean - true or false
- number - int, float, double, etc.
- string - an array of characters
- null - no value
- undefined - declared variable that doesn't have a value set
- symbol - a unique value not equal to any other value (don't worry for now, just know it's there)

### Objects (The 'Other' Type)

Everything that isn't classified as a basic type is an object.  
Examples:
- Arrays
- Dictionaries
- Classes

### Implicit Types

#### Falsy vs Truthy
In JavaScript you can use any type of variable to evaluate a boolean conditional.  

Certain values are truthy, meaning they will evaluate to true but the value is not true.

Truthy:
- numbers (greater than 0)
- string
- Objects

The same thing applies to falsy, but the value evaluates to false.

Falsy:
- numbers
- null
- undefined

Example:
<pre>
int a = 1;
if(a) {
  console.log("a = true");
}
console.log(a);

// Output:
// a = true
// 1
</pre>

So a's value is 1, but evaluates to true in the if statement.  
And of course true and false still work as expected.

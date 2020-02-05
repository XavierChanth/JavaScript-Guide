# Arrays and Objects

All of the following is a type of Object.

## Arrays 

### Basics
- Adding elements to end - array.push(data)
- Removing (and returning) elements from end - array.pop()
- Read an element by index - array[0], array[1]
- Update an element = array[0] = data
- delete something other than the last element del array[0], del array[1]

### Advance Functions (Super Useful)

Some useful function built into arrays:
- forEach
- map
- filter
- reduce
- indexOf
- every

Research these!  
Start at 
https://developer.mozilla.org/en-US/


## Basic Objects (Sometimes Called Dictionary)

A Dictionary is a key value pair.  

### Key
- Must be a unique number or string
- Strings do not need quotation marks in JavaScript

### Values
- Don't have to be unique
- Can be any type of data

Example:
<pre>
const dictionary = {
  key: 12,
  anotherKey: [1, 2, 3, 4]
};

console.log(dictionary.key)

// Output
// 12
</pre>

## Spreading

This applies to objects (dictionaries) as well.  
Basically this assigns different elements in an array to a variable.

Example:
<pre>
let array = ["John", "Appleseed", 21, "pilot", "single"];

// lets say I only need the name and age...
let [firstName, lastName, age, ...rest] = array;
</pre>

What the data looks like:  
- firstName = "John"
- lastName = "Appleseed"
- age = 21
- rest = ["pilot", "single"]

How does this work for an Object?

<pre>
  let obj = {
    firstName: "John",
    lastName: "Appleseed",
    age: 21,
    occupation: "pilot",
    status: "single"
  };

  // getting the data we want ...

  let { firstName, age, lastName, ...rest } = obj;
</pre>

What the data looks like:  
- firstName = "John"
- lastName = "Appleseed"
- age = 21
- rest = { occupation: "pilot", status: "single" }

## Classes
Two major keywords associated with Classes.
- this
- new

this:
- can only be used inside the class
- used to refer to the whole class  
  - You know *this* class...

new:
- Used to create a new instance of a class
- Classes cant be used by themselves, an instance of them needs to be created.

> Study OOP (Object Oriented Programming)

## Functions

Also an Object but will continue in next Document...

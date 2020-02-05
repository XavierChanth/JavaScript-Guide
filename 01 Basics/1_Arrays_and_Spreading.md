# Arrays

## Basics
- Adding elements to end - array.push(data)
- Removing (and returning) elements from end - array.pop()
- Read an element by index - array[0], array[1]
- Update an element = array[0] = data
- delete something other than the last element del array[0], del array[1]

## Advance Functions (Super Useful)

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


# Functions (Methods)

## Function Formats

"Regular Form":
<pre>
function nameOfFunction(parameters) {
  // do something
}
</pre>

"Arrow Form":
<pre>
const nameOfFunction = (parameters) => {
  // do something
}
</pre>

Arrow benefits from shorter syntax:
<pre>
{
  f1: () => {},
  f2: function() {}
}
</pre>

Auto return arrow functions:
<pre>
const getData = (res) => res.data;
</pre>

This function takes res and immediately returns res.data

## Closure Functions

<pre>
const getCounter = () => {
  let counter = 0;
  const increment = () => {
    counter = counter + 1;
  }
  return {
    counter,
    increment
  };
}

const counter1 = getCounter();
const counter2 = getCounter();

// counter1.counter is a different variable than counter2.counter

counter1.increment();
counter1.increment();

counter2.increment();

console.log(counter1.counter + " " + counter2.counter);

// Output:
// 2 1
</pre>

## Sync vs Async

In most coding languages, code only runs synchronously, meaning that each line of code is executed in order.

>i.e. Line 1 runs, then line 2, then line 3...

<pre>
console.log('ONE')
console.log('TWO')

// Output:
// ONE
// TWO
</pre>

### Promises

JavaScript code can also be executed asynchronously using functions. If you call an async function, the async function will run, but the code will continue without waiting for the function to finish.

<pre>

function delay(seconds) {
  const resolve = () => {console.log('Promise Finished!')}
  return new Promise(() => setTimeout(resolve, seconds * 1000));
}

console.log(delay(1));

// Output: 
// Promise { <pending> }
// Promise Finished!

</pre>

If an asynchronous piece of code needs to return something, but it doesn't know what to return yet, it will return a Promise.

We cannot use const with a promise, since it initially returns a promise object.  
If we were to use a const, then the object would never resolve since it would forever be stuck as a promise object.

#### Promise Summary

A Promise is literally a promise to return actual data later. 

Don't use const, use let.

There are three ways to handle Promises:
- Callback Functions
- Promise.then
- Async/Await

#### Callback Functions

Callback functions pass a function as a parameter which can then be called after the result is evaluated. The result will be passed as an argument to the function.

<pre>
const f1 = () => {
  console.log('Callback!');
}

const f2 = (callback) => {
  console.log('Before callback');
  callback();
  console.log('After callback');
}

f2(f1);

// Output:
// Before callback
// Callback!
// After callback
</pre>

As you can see we pass f1 as the callback for function f2.  
The callback can be run at any point inside of f2.  
Callbacks are commonly used to run some code after a function does what it needs to do.

For example, many of the array functions use callbacks:
- find
- forEach
- map
- reduce

Review these now that you have a better understanding of callback functions.

#### Promise.then

Promise.then will call the callback function when it resolves.  
But what if we are waiting for a database that crashed...  
A promise won't wait forever, we will also need a .catch to catch any errors.

<pre>
  Promise
  .then(successCallbackFunction)
  .catch(failureCallbackFunction)
</pre>

#### Async Functions & Await Keyword

Another alternative is to use Async functions with await.

This makes sense if you have nothing else to do while you wait for the data to resolve.  

In order to use the await key word we need to declare an async function.
<pre>
// Either
async function example1() {
  // do something
}

// Or
const example2 = async() => {
  // do something
}
</pre>

Again, await can ONLY be used in an async function.

Let's say we have a function to get Users from a database called getUsers(). 
Of course we have to wait for the database to return the data to us...
<pre>
const example = async() => {
  try {
    let users = await getUsers();
    // do something with users...
    console.log(users[0].name)
  } catch(error) {
    // do something with the error
    console.log('Yeah, our database broke...')
  }
}

// Alternatively to try/catch (as long as your database returns null/undefined/false if theres an error)
const example = async() => {
  let users = await getUsers();
  if(!users) {
    // handle error
  } else {
    // do something with users
  }
}

</pre>


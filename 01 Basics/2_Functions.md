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

## Callback Functions

## Async Functions

## Promises


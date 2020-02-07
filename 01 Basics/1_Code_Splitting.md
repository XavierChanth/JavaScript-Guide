# Code Splitting

## If statements

<pre>
if(conditional_A) {
  // runs when conditional_A is true
} else if (conditional_B) {
  // runs when conditional_A is false, but conditional_B is true
} else {
  //runs when both conditional_A and conditional_B is false
}
</pre>

## Switch Statements

*Review the break and continue keywords to better understand this section!*

When you have to many else if's it might be better to use a switch.  
However, switches don't use conditionals.  
They compare values for equality...

<pre>
switch(the_variable_to_compare) {
  case value_to_compare_to_1:
    //When it matches this case this will run
  break; 
    // Without a break, the switch will continue running until the end.
  case value_to_compare_to_2:
  case value_to_compare_to_3:
    // This will run if it matches either case above
  break;
  default:
    //runs if no cases match.
  break;
}
</pre>

## Try Catch Finally Statements

When a piece of code has the potential to throw an Error we wrap it with a try/catch or try/catch/finally statement.

<pre>
try {
  // try to run some code that could throw an error
} catch (error) {
  // do something with the error if one is thrown
} finally {
  // the finally part is not mandatory but will always run after the try/catch regardless of whether it threw an error
}
</pre>

## Loops
// todo
### For

### While

### Do while

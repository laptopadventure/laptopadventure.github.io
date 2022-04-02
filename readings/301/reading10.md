
# Reading Notes 10

[Back to the table of contents](../README.md)

## Reading 1

* What is a ‘call’?
  * A call is a single function in the last in first out list that is the call stack. The call stack is a list of functions waiting to resolve because they are waiting on the return value of a function called inside itself. So for example, if you have a function, and then in that function you call a toUppercase, your stack will now have two levels deep while it is in toUppercase because it is processing that function and then will go back to the lower level one with the result of toUppercase to continue. If toUppercase errored, the call stack would show two levels of depth.
* How many ‘calls’ can happen at once?
  * As many as the browser can accomodate. In essense, it doesn't really matter since the browser WILL accomodate for you, except for situations you make a stack overflow happen. Will talk about that in its own section.
* What does LIFO mean?
  * I mention it above, Last In, First Out. It's a data structure that means a list of data will have the last thing added to it as the first thing removed. So using my previous example, the stack is empty, then has my function, then has toUppercase, then removes toUppercase when its done, then removes my function when that is done as well.
* Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
  * Going to use a code block for the functions:
```js
function myFunc() {
  functionTwo();
};

function functionTwo() {
  throw new Error('Die!');
}
```
  * And how the stack trace would look:
    * ![Stack trace example](../../img/stack.png)
* What causes a Stack Overflow?
  * The point where your browser can't keep adding calls to the call stack. The only situation that really comes up in is when you accidentally add a recursive loop that adds to the call stack, aka a function that calls itself. It will keep calling itself, but never finishing what it calls because it goes deeper to run itself again, so on and so forth until the browser has had enough with you and stops the code from running with a stack overflow error.

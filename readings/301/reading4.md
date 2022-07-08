
# Reading Notes 4

[Back to the table of contents](../../README.md)

* What is a ‘Controlled Component’?
  * Some html components in react actually do hold state for themselves, ones that make sense for them to do so, like inputs, selects, and textareas. That means the "value" attribute for inputs can live update from state. We listen to the input's `onChange` signal, update state every time they type, and then set value to the state. Wonderful!
* Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
  * I see a use case for both:
    * On submit works better for my site where I turn search terms into filter labels that can be added and removed.
    * On change could make sense when having a dynamic search update with every letter, but... that may be expensive! If it's not, sounds like a great idea.
* How do we target what the user is entering if we have an event handler on an input field?
  * Signals pass event objects to the function that handles them, event.target.value is event object, html element, and what was entered into it respectively!
* Why would we use a ternary operator?
  * I think the following rewrite will prove why, but very often it can condense a lot of lines into one elegantly. Great for readability, which is one of the most important parts of coding.

Rewrite the following statement using a ternary statement:

```js
if(x===y){
  console.log(true);
} else {
  console.log(false);
}
```

Too long, too long! I'll make it shorter with a ternary...

```js
 console.log(x === y ? true : false)
```

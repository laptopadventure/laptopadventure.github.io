# Reading 27

[Back to the table of contents](../../README.md)

## Introducing Hooks

- What was the motivation for introducing Hooks?
  - Only hacky solutions existed before hooks, like putting state on a higher order class and passing it down through render props. But changing your architecture not around the website but rather the code for the website turns repositories into messes.
- What changes are important regarding implementing Hooks versus Component Classes?
  - Class components aren't going anywhere, and hooks work alongside classes. Adopting can be gradual, and doesn't require one massive refactor pr.
- Hooks allow you to reuse stateful logic without changing ___ _______.
  - component hierarchy

## Hooks Api

- Name two rules imposed by React Hook usage.
  - Only call hooks at the top level. Don't call them in loops, conditions, or nested functions
  - Only call hooks from react function components. Don't call them from normal JS functions or wherever else.
- How would you identify a custom Hook and why might you create one?
  - Naming scheme has the function for a custom hook start with "use"
  - Custom hooks are good for preventing copy paste code, aka needing to do the same operation in multiple places, independently. Otherwise, you'd need to pass the result on a parent component down to both children components that need it as a prop.

## The State Hook

- What is a Hook?
  - Hooks are the functional equivalent of features provided by class components, given to prevent having to change your component structure to enable functionality.
  - But long story short: "A Hook is a special function that lets you “hook into” React features."
- When would I use the useState Hook?
  - Any time you want your component to have a state, like how a class component sets up state when it needs t.. You can use it multiple times for multiple entries.
- If you were to add React state to a function component by declaring a state variable:
  - What does calling useState do?
    - it declares a state variable, and gives you a function for mutating it. you collect both of these returns as constant variables
  - What do we pass to useState as an argument?
    - the initial setting.
  - What does useState return?
    - an array, with both a value referring to the current value of the state variable, and a function for mutating that value. we capture both by destructuring the array into constant vars.

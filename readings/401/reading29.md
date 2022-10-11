# Reading 27

[Back to the table of contents](../../README.md)

## useReducer hook

- Name an alternative to the useState Hook.
  - useReducer is an alternative to hook that calls a function to calculate new state after an action
- Why might the useReducer Hook be preferable to the useState Hook?
  - In complicated state logic where you have multiple sub-values
  - When the next state depends on the last one, reducers make it super easy.
- What are two ways to set the initial state?
  - Pass in the initial state as the second argument
  - Pass in a function to "lazy create the initial state", which is useful for resetting the state to an original value later in the reducer.

## Ultimate Guide to useReducer

- In terms of state, what does useReducer expect to receive as a parameter?
  - It only recieves what the initial state should be, in terms of state.
- What does useReducer return?
  - the initial state you put in as a variable for display, and a dispatch function. Dispatch function passes actions which calls the reducer function to consider it and make a new state object.
- Explain dispatch to a non-technical recruiter.
  - we have a check for deciding a value. when we want to change the value, we pass in actions into the dispatch to rerun the check for deciding said value, but with different actions for different outcomes on what the state will be.

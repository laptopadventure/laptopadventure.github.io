## Application State with Redux

[Back to the table of contents](../../README.md)

### Dan Abramov Redux Tutorials

- What is the first principle of Redux?
  - Represent the whole state of your app as a single (immutable) JS object.
- what is a store and what do we use our reducers for within that store?
  - Store is the equivalent of context: global object. We can't change it, but we can create an entirely new object to replace it, and we use reducers to consider data and reduce that into one object.
- Name three Redux store methods given to us by createStore and describe their use.
  - getState() returns the current state of your store, aka the last return value a reducer gave.
  - dispatch(action) invokes the reducer function with the previous state and the action given to the dispatch, so it can be reduced into a new global object.
  - subscribe(listener) invokes the listener when the store changes, for additional tweaking before the reducers do their thing. Returns a function that can be invoked to unsubscribe.
- Explain to a non-technical recruiter what combineReducers() does and why it is useful.
  - As we have processes for handling if one thing or another changes, it may get really complicated keeping track of what handles what. So we can use combineReducers and feed in all our processes for a single combined process that will run each process it was given to decide the output.

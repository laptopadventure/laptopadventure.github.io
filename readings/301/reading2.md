

# Reading Notes 2

[Back to the table of contents](../README.md)

## Reading

There are three phases to a component's lifestyle, and triggering those parts of the lifestyle has a process from start to finish to execute it.

* Mounting
  * Components mount onto the dom and render. It gets state from the props and then renders onto the page.
* Updating
  * When a component either recieves a new state or is forced to update, it... does indeed update! This requires getting the state from the props again, along with some extra stuff, and then re-rendering onto the page.
* Unmounting
  * This happens when a component is leaving the webpage, it only has a single function and cannot be cancelled.

### Methods

#### constructor()

Called before mounting, should call super if it is a subclass of another component. Can be used to set up state as well.

#### render()

Required method, for obvious reasons. This is where you return all the tags in your component that decide how it looks and what other components should be inside it.

```
 >Do NOT change state in the render proc! State is changed elsewhere to cause this method to re-render!
```

#### componentDidMount()

Essentially a blank method for after the component is fully loaded and rendered, good for adding network requests (API calls) since everything else is set up.

## Video

### Props?

Think of it as an argument to a function. You give components props when you tell it to render, and it has access to props for its own render. When props change, it will re-render

### State?

Big difference here, state is only IN a component. You pass props into a component and it uses that, but state is entirely managed by the component itself. We could update a counter with state only because its inside, props have to be updated from outside a component. (you pass in the title as a prop, the title updates. vs you setstate inside a component to a new title, the title updates.)

Also, since its managed by the component, it... holds state! Crazy, I know, but yeah, think of it as a variable you can update to re-render the component and redo logic.

```
You can't change props, but you can change state! Something ELSE has to decide to give new props!
```

## Takeaways

### Reading

* Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
  * render went first!
* What is the very first thing to happen in the lifecycle of React?
  * The constructor, before aaanything else.
* Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`
  * constructor
  * render
  * React Updates
  * componentDidMount
  * componentWillUnMount
* What does `componentDidMount` do?
  * Essentially a blank method for after the component is fully loaded and rendered, good for adding network requests (API calls) since everything else is set up.

### Video

* What types of things can you pass in the props?
  * Anything a function could recieve in javascript.
* What is the big difference between props and state?
  * Props are handed into a component from outside a component, and state is managed by the component itself. If its managed only in a component, you should use state. Otherwise, props.
* When do we re-render our application?
  * When the state or props changes, but keep in mind components can't update their own props, only wait to recieve new ones.
* What are some examples of things that we could store in state?
  * A counter! While the initial value could be handed in by props, a counter has to manage how much its counting by itself (aka a component managing its own state).
  * An input field! After entering in your name, we can set the state to keep that name in the input field as a default and hold it rendered.

Why Redux?

The key aspect that separates Redux from most other state containers such as MobX, Relay, and most other Flux based implementations is that Redux has a single state that can only be modified via “actions” (plain JavaScript objects), which are dispatched to the Redux store. Most other data stores have the state contained in React components themselves, allow you to have multiple stores and/or use mutable state.

This in turn causes the store’s reducer, a pure function that operates on immutable data, to execute and potentially update the state. 
This process enforces unidirectional data flow, which is easier to understand and more deterministic.

Since Redux reducers are pure functions operating on immutable data, they always produce the same output given the same input, making them easy to test.

Working with React

While Redux isn’t tied to any specific companion library, it works especially well with React.js since React components are pure functions that take a state as input and produce a virtual DOM as output.

React-Redux is a helper library for React and Redux that eliminates most of the hard work connecting the two. To most effectively use React-Redux, let’s go over the notion of presentational components and container components.

Presentational components describe how things should look visually, depending solely on their props to render; they invoke callbacks from props to dispatch actions. They’re written by hand, completely pure, and are not tied to state management systems like Redux.

Container components, on the other hand, describe how things should function, are aware of Redux, dispatch Redux actions directly to perform mutations and are generally generated by React-Redux. They are often paired with a presentational component, providing its props.
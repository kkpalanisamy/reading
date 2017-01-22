Why Redux?

The key aspect that separates Redux from most other state containers such as MobX, Relay, and most other Flux based implementations is that Redux has a single state that can only be modified via “actions” (plain JavaScript objects), which are dispatched to the Redux store. Most other data stores have the state contained in React components themselves, allow you to have multiple stores and/or use mutable state.

This in turn causes the store’s reducer, a pure function that operates on immutable data, to execute and potentially update the state. 
This process enforces unidirectional data flow, which is easier to understand and more deterministic.
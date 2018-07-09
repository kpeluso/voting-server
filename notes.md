# Notes from Voting App with Redux:

https://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html#loading-entries

*Core functions* = are types of pure functions that control app logic.

- Pure functions should always map old states to new states.
  This also helps with future-proofing for horizontal data scaling.

- With Redux, you don't call core functions directly.
  *Actions* = layer of indirect interaction with core functions.
  - Actions are objects whose properties form the arguments to
    core functions (excluding the state).

*Reducers* = Generic function taking any action and current state
  and invokes core function matching the action.
  - Just returns the current state if action not recognized.
  - Called reducer since if given collection of past actions, it gets
    reduced into 1 state. i.e. Batch/Replay collection of actions.

- Reducer Composition = Modularizes code so whole state need not be parsed / modified by reducer that only cares for subset of state. More here: http://rackt.github.io/redux/docs/basics/Reducers.html

*Redux Store* = Stores app states over time.
  Initialized with a reducer.
  You could then *dispatch* actions to that store, which uses your reducer.




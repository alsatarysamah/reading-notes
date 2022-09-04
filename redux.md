# Using combineReducers
```js
export default theDefaultReducer = (state = 0, action) => state

export const firstNamedReducer = (state = 1, action) => state

export const secondNamedReducer = (state = 2, action) => state

// rootReducer.js
import { combineReducers, createStore } from 'redux'

import theDefaultReducer, {
  firstNamedReducer,
  secondNamedReducer
} from './reducers'

// Use ES6 object literal shorthand syntax to define the object shape
const rootReducer = combineReducers({
  theDefaultReducer,
  firstNamedReducer,
  secondNamedReducer
})

const store = createStore(rootReducer)
console.log(store.getState())
// {theDefaultReducer : 0, firstNamedReducer : 1, secondNamedReducer : 2}
```
# combineReducers(reducers)

The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

```js
rootReducer = combineReducers({potato: potatoReducer, tomato: tomatoReducer})
// This would produce the following state object
{
  potato: {
    // ... potatoes, and other state managed by the potatoReducer ...
  },
  tomato: {
    // ... tomatoes, and other state managed by the tomatoReducer, maybe some nice sauce? ...
  }
}
```


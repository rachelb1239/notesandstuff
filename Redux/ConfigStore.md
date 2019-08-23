# Redux - Config Store
Date 7/21/2019

# Links
- Configure Store: https://redux-docs.netlify.com/recipes/configuring-your-store#the-solution-configurestore

# Middleware vs Enhancers
- Middleware (more common)
    - Adds functionality to dispatch function
- Enhancers (less common)
    - Adds functionality to the store

# STORE
## Ideal index.js Setup for creating store
- All middleware and enhancements configured in seperate file
    - Keeps index.js file clean

```javascript
import React from 'react'
import { render } from 'react-dom'
import { Provider } from 'react-redux'
import App from './components/App'
import configureStore from './configureStore'

const store = configureStore()

render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('root')
)
```
## Example configStore file - w/o dev tools
- Has custom middleware logger and enhancer for monitoring

```javascript
import { applyMiddleware, compose, createStore } from 'redux'
import thunkMiddleware from 'redux-thunk'

import monitorReducersEnhancer from './enhancers/monitorReducers'
import loggerMiddleware from './middleware/logger'
import rootReducer from './reducers'

export default function configureStore(preloadedState) {
  const middlewares = [loggerMiddleware, thunkMiddleware]
  const middlewareEnhancer = applyMiddleware(...middlewares)

  const enhancers = [middlewareEnhancer, monitorReducersEnhancer]
  const composedEnhancers = compose(...enhancers)

  const store = createStore(rootReducer, preloadedState, composedEnhancers)

  return store
}
```
## Example configStore file - w dev tools
- requires redux-devtools-extension as a dependency

```
npm install --save-dev redux-devtools-extension
```

```javascript
import { applyMiddleware, createStore } from 'redux'
import thunkMiddleware from 'redux-thunk'
import { composeWithDevTools } from 'redux-devtools-extension'

import monitorReducersEnhancer from './enhancers/monitorReducers'
import loggerMiddleware from './middleware/logger'
import rootReducer from './reducers'

export default function configureStore(preloadedState) {
  const middlewares = [loggerMiddleware, thunkMiddleware]
  const middlewareEnhancer = applyMiddleware(...middlewares)

  const enhancers = [middlewareEnhancer, monitorReducersEnhancer]
  const composedEnhancers = composeWithDevTools(...enhancers)

  const store = createStore(rootReducer, preloadedState, composedEnhancers)

  return store
}
```
# Redux Action Creator/Action/Reducer Overview 
Date: 07/25/19

# Links
- Basics for Actions: https://redux.js.org/basics/actions
- Basics for Reducers: https://redux.js.org/basics/reducers

# Action Creators
- Action creators are functions that create actions
- Define valid action types and payloads of information that will be sent with the action
- Return an action

# Actions
- Actions are payloads of information - specifed by type and info to update
- Actions describe what happened, not how the state changes
- Actions are DISPATCHED to the reducer inside components through events (onclick, on component mount, etc)

# Reducers
- Specifies how state is changed in response to an action
- Checks if action type is valid
- Updates store/state based on action (either with payload or existing state)
- Update of state/store causes rerender of connected/effected components

# Example
- On click
- make an api call
- get results back
- dispatch an action w/ results of api call as payload
- reducer checks action type 
    - if action type is valid
        - Update store with payload
    - else
        - return existing state
- Connected components rerender upon store update
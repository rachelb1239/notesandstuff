# Redux Selector Pattern - 07/29/19

# Links
- Redux Selector Pattern: https://medium.com/@matthew.holman/what-is-a-redux-selector-a517acee1fe8
- Reselect: https://rangle.io/blog/react-and-redux-performance-with-reselect/

## Selector Pattern (as I have interpreted it)
  - A way to 'query' the store and transform the data outside of the component
  - Component gets the data it needs exactly as it should render it
  - Good for seperation of concerns
    - If shape of the data changes, component doesn't care - just update the selector
  - Live along side reducers (typically in the same file)
    - Reminds you to update reducers and selectors at the same time
  - Memoization!
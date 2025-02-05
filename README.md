# React useEffect Hook - Missing Dependency
This example demonstrates a common error in React's `useEffect` hook: a missing dependency in the dependency array, leading to an infinite loop. 
The component `MyComponent` uses `setInterval` to update a counter every second. However, the dependency array is empty (`[]`), meaning the effect runs after every render. This causes a loop because setting `count` triggers a re-render, which in turn runs the effect again.
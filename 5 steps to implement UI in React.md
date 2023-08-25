#steps #react 
# Step 1: Break the UI into a component hierarchy

# Step 2: Build a static version in React

# Step 3: Find the minimal but complete representation of UI state

## Props vs State
There are two types of “model” data in React: props and state. The two are very different:

- [**Props** are like arguments you pass](https://react.dev/learn/passing-props-to-a-component) to a function. They let a parent component pass data to a child component and customize its appearance. For example, a `Form` can pass a `color` prop to a `Button`.
- [**State** is like a component’s memory.](https://react.dev/learn/state-a-components-memory) It lets a component keep track of some information and change it in response to interactions. For example, a `Button` might keep track of `isHovered` state.

Props and state are different, but they work together. A parent component will often keep some information in state (so that it can change it), and _pass it down_ to child components as their props. It’s okay if the difference still feels fuzzy on the first read. It takes a bit of practice for it to really stick!

# Step 4: Identify where your state should live

# Step 5: Add inverse data flow

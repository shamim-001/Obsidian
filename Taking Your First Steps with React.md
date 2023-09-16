# Differentiating between declarative and imperative programming
- imperative programming as a way of describing how things work, and declarative programming as a way of describing what you want to achieve.
- Declarative programming tends to avoid creating and mutating a state.

# How React elements work
- To control the UI flow, React uses a particular type of **object** called an element. These elements are created using the `React.createElement()` function, or more commonly, with JSX syntax. Elements contain only the information that is strictly needed to represent the interface.
```js
{
  type: Title,
  props: {
    color: 'red',
    children: {
      type: 'h1',
      props: {
        children: 'Hello, H1!'
      }
    }
  }
}

```

- The element’s type is crucial because it informs React on how to handle it. If the type is a string, the element represents a DOM node, while if it’s a function, the element represents a component.
- React uses a technique called the Virtual DOM, which is an in-memory representation of the actual DOM. It compares the current and new trees to minimize the number of actual DOM updates. This process is called reconciliation and is used by both React DOM and React Native to create UIs for their respective platforms.


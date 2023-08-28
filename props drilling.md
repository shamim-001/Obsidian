![[Pasted image 20230828100129.png]]
Props are essentially objects that contain various properties and their corresponding values.
![[Pasted image 20230828101734.png]]


```jsx
// ParentComponent.jsx
import React from 'react';
import ChildComponent from './ChildComponent';

const ParentComponent = () => {
  const name = 'John';
  const age = 30;

  return <ChildComponent name={name} age={age} />;
};

export default ParentComponent;
```

```jsx
// ChildComponent.jsx
import React from 'react';

const ChildComponent = (props) => {
  return (
    <div>
      <p>Name: {props.name}</p>
      <p>Age: {props.age}</p>
    </div>
  );
};

export default ChildComponent;
```

Remember that you can destructure the `props` object in functional components to make the code more readable:

```jsx
// ChildComponent.jsx
import React from 'react';

const ChildComponent = ({ name, age }) => {
  return (
    <div>
      <p>Name: {name}</p>
      <p>Age: {age}</p>
    </div>
  );
};

export default ChildComponent;
```

Using props, you can create reusable and configurable components by passing different data to them as needed.


![[Pasted image 20230828101836.png]]

```jsx
const Paragraph = (props) => {
  return <p>{props.children}</p>;
};

const App = () => {
  return (
    <>
      <h1>App</h1>
      <Paragraph>
        <h1>This is a heading inside a paragraph component</h1>
        <p>This is some text inside a paragraph component.</p>
      </Paragraph>
    </>
  );
};

export default App;

```

=
```js
var Paragraph = function(props) {
    return React.createElement("p", null, props.children);
};

var App = function() {
    return React.createElement(React.Fragment, null,
        React.createElement("h1", null, "App"),
        React.createElement(Paragraph, null,
            React.createElement("h1", null, "This is a heading inside a paragraph component"),
            React.createElement("p", null, "This is some text inside a paragraph component.")
        )
    );
};

```
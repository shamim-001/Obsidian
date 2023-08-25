#react #state #hook 
[Github code](https://github1s.com/jherr/fcc-state)

1. [useState]:
   - If we change the state of the component, we'll get a re-render ==which means it calls the component function again to generate the updated output.==

This anonymous function runs only once.
```js
const [name, setName] = useState(() => "");
```

2. [useReducer]:
   
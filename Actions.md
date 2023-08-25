![[Pasted image 20230810085012.png]]

1. An action is an object with a 'type' property
2. An action creator is a function that returns the 'action object'
```js
const CAKE_ORDERED = 'CAKE_ORDERED'

function orderCake() {
return {
	type: CAKE_ORDERED,
	quantity: 1
}
}
```

#async #js #callback

```js
console.log("Order Pizza!");

const orderPizza = (callback) => {

	setTimeout(() => {
	
	const pizza = "Pizza";
	
	callback(pizza);

}, 2000);

};

  

const pizzaReady = (pizza) => {

	console.log(`Eat the ${pizza}`);

};

  
orderPizza(pizzaReady);

console.log(`Call Sajid!`);

```


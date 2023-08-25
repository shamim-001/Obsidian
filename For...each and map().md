#js-concept #js #array-method #for-each #map 
# forEach()
The `forEach()` method iterates over each element of an array and executes a provided callback function for each element. ==It does not return a new array.==
```js
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((number) => {
  console.log(number);
});

```

# map()
The `map()` method also iterates over each element of an array, executes a callback function, and ==returns a new array with the results of the callback function.==
```js
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map(function (number) {
  return number * 2;
});

console.log(doubledNumbers); // [2, 4, 6, 8, 10]

```

`forEach()` is used when you want to perform an action on each element of an array without creating a new array, while `map()` is used when you want to transform each element of an array and create a new array with the transformed values.

# reduce()
- The `reduce()` method in JavaScript is used to iterate over an array and accumulate its values into a single value. 
- It takes a callback function as an argument, which is executed for each element in the array.
- The `reduce()` function keeps track of an accumulator variable, which holds the accumulated result. The callback function takes two parameters: the accumulator and the current element of the array. It performs some operation on the accumulator and the current element, and ==returns the updated accumulator value.==
```js
const number = [10, 20, 30];

let total = number.reduce((acc, cnum) => {
	console.log(`Acc: ${acc} `);
	console.log(`current num: ${cnum} `);
	return acc + cnum;
}, 100); // Here current value of the accumulator is set to 100;

console.log(`Total: ${total}`);
```
result:
```js
	Acc: 100
	current num: 10
	Acc: 110
	current num: 20
	Acc: 130
	current num: 30

	Total: 160
```

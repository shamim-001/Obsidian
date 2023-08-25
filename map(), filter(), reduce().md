#interview-js 
[[For...each and map()]]

1. **`map()`**: The `map()` method creates a new array by applying a given function to each element of the original array. ==It returns a new array with the same length as the original, where each element is the result of the applied function.==

   Example:
   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   const doubledNumbers = numbers.map(num => num * 2);
   // doubledNumbers will be [2, 4, 6, 8, 10]
   ```
- map() returns modified value

1. **`filter()`**: The `filter()` method creates a new array containing all elements that pass a given test (provided by a callback function). It returns a new array with only the elements that satisfy the condition.

   Example:
   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   const evenNumbers = numbers.filter(num => num % 2 === 0);
   // evenNumbers will be [2, 4]
   ```

3. **`reduce()`**: The `reduce()` method "reduces" an array to a single value by applying a given function to each element and accumulating the result. It takes an initial value and a callback function that defines how the accumulation is done.

   Example:
   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   const sum = numbers.reduce((acc, num) => acc + num, 0);
   // sum will be 15 (1 + 2 + 3 + 4 + 5)
   ```

```javascript
const cart = [
  { name: 'Shirt', price: 20 },
  { name: 'Jeans', price: 50 },
  { name: 'Shoes', price: 80 },
  // ... more items
];

const totalCost = cart.reduce((accumulator, item) => {
  return accumulator + item.price;
}, 0);

console.log(`Total cost of items in the cart: $${totalCost}`);
```


```javascript
const nums = [1, 2, 3, 4, 5, 6, 7, 8];

const numsAddOneEvens = nums.reduce((acc, current) => {
  const incremented = current + 1;
  if (incremented % 2 === 0) {
    acc.push(incremented);
  }
  return acc; // initial value represents the 'acc'
}, []);

console.log(numsAddOneEvens);
```


- It is used to iterate over an array and accumulate a single value based on the elements of the array. 
- It can be used calculating the total price of items in a shopping cart.
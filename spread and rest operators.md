#interview-js 
In JavaScript, the spread (`...`) and rest (`...`) operators are used for working with arrays and function arguments. They have different applications and behaviors:

**Spread Operator (`...`)**:
The spread operator is used to split an array (or other iterable) into individual elements. It is primarily used for creating shallow copies of arrays, combining arrays, and passing elements as separate arguments to functions.

Usage examples:

1. **Copying an Array**:
   ```javascript
   const originalArray = [1, 2, 3];
   const copiedArray = [...originalArray];
   ```

2. **Combining Arrays**:
   ```javascript
   const array1 = [1, 2, 3];
   const array2 = [4, 5, 6];
   const combinedArray = [...array1, ...array2];
   ```

3. **Passing Array Elements as Arguments**:
   ```javascript
   function add(a, b, c) {
       return a + b + c;
   }
   const numbers = [1, 2, 3];
   const sum = add(...numbers); // Equivalent to add(1, 2, 3)
   ```

**Rest Parameter (`...`)**:
The rest parameter allows you to represent an indefinite number of arguments as an array. It is used in function parameter lists to capture remaining arguments into an array.

Usage example:

```javascript
function sumNumbers(...nums) {
    return nums.reduce((sum, num) => sum + num, 0);
}

const result = sumNumbers(1, 2, 3, 4, 5); // Result will be 15
```

In this example, the `...nums` syntax in the function parameter list captures all provided arguments into an array named `nums`, allowing you to perform operations on them collectively.

In summary, the spread operator is used to expand elements from an iterable (like an array), while the rest parameter is used to collect multiple function arguments into an array. Both operators are useful for handling arrays and function arguments in a more flexible and concise way.
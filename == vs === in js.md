#interview-js 
`==` compares only the value not type
`===` compares both the value and the type

In JavaScript, `==` and `===` are comparison operators used to compare values for equality. However, they behave differently due to their type coercion behavior:

1. **`==` (Equality Operator)**: This operator performs type coercion before comparison. It converts the operands to the same type and then compares their values. It returns `true` if the values are equal after type coercion, otherwise, it returns `false`.

   Example:
   ```javascript
   5 == '5'; // true (number 5 is coerced to string '5')
   1 == true; // true (boolean true is coerced to number 1)
   ```

2. **`===` (Strict Equality Operator)**: This operator performs a strict, type-safe comparison. It compares both the value and the data type of the operands. It returns `true` only if both the value and type are the same, otherwise, it returns `false`.

   Example:
   ```javascript
   5 === '5'; // false (number 5 is not the same as string '5')
   1 === true; // false (number 1 is not the same as boolean true)
   ```

In most cases, it's recommended to use the `===` (strict equality) operator because it prevents unexpected type coercion and ensures a more predictable comparison. It helps to write safer and more reliable code. Use `==` only when you intentionally want to perform type coercion and are aware of its implications.


#interview-js 
```js
// var firstNameVar -> hoisting // lexical scope
if (false) {
	var firstNameVar = "Shamim";
	let firstNameLet = "Shamim";
}

console.log(firstNameVar); // undefined
console.log(firstNameLet); // error
// Both of them can be re-assigned
```

```js
const PI = 3.14;
PI = 3.145 // error

const user = {
firstName: 'Shamim'
}
user.firstName = 'MD. Shamim' // modification possible for array, object property

```

In JavaScript, `const`, `let`, and `var` are used to declare variables, but they have different behaviors and scopes. Here's a breakdown of their differences:

1. **`const`**: Variables declared with `const` are constants and cannot be reassigned after their initial value is set. They are block-scoped, which means they are only accessible within the block (a pair of curly braces) in which they are defined.

   Example:
   ```javascript
   const pi = 3.14159;
   pi = 3.14; // Error: Cannot reassign a constant variable
   ```

2. **`let`**: Variables declared with `let` can be reassigned after their initial value is set. Like `const`, they are also block-scoped.

   Example:
   ```javascript
   let count = 10;
   count = 20; // Allowed: Reassigning a variable declared with let
   ```

3. **`var`**: Variables declared with `var` are function-scoped or globally-scoped, depending on whether they are declared within a function or outside of it. Unlike `const` and `let`, `var` variables can be reassigned and their scope is not limited to blocks.

   Example:
   ```javascript
   var x = 5;
   if (true) {
       var x = 10; // This will modify the outer x variable
   }
   console.log(x); // Outputs 10
   ```

It's generally recommended to use `const` by default for variables that won't be reassigned, and use `let` when you need to reassign a variable. Avoid using `var` in modern JavaScript as it can lead to scope-related issues and make code harder to maintain.
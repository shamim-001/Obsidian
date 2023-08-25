#js #js-concept #static-method 
A static method is a method that belongs to a class itself, rather than to the instances of the class. This means that static methods are called on the class itself, not on individual objects created from the class.

Utility Functions: Static methods are often used to define utility functions or operations that are not specific to a particular instance but are relevant to the class as a whole.

```js
class MathUtils {
  static add(a, b) {
    return a + b;
  }

  static multiply(a, b) {
    return a * b;
  }

  static isEven(num) {
    return num % 2 === 0;
  }
}

console.log(MathUtils.add(2, 3)); // Output: 5
console.log(MathUtils.multiply(4, 5)); // Output: 20
console.log(MathUtils.isEven(6)); // Output: true
console.log(MathUtils.isEven(7)); // Output: false
```


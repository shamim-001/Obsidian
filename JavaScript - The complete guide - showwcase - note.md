#js-notes

# Closure
Whenever an execution context's execution phase is over, that execution context is lost from the call stack.

Definition of closures: Any execution context's function + it's parent's lexical environment together forms a closures. So, the closure is always there but hidden!

# Arrow function
Arrow functions do not have their own `**this**`, `**arguments**`, `**super**`, or `**new.target**` are often used when you don't need these features.

Arrow functions do not have their own `this` binding. In regular functions, the value of `this` is determined by how the function is called. However, arrow functions inherit the `this` value from the surrounding lexical context (the nearest enclosing non-arrow function). This means that the value of `this` inside an arrow function will be the same as the value of `this` outside the arrow function.


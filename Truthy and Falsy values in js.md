#interview-js 

```js
null
undefined
0
""
false
```

In JavaScript, values are categorized as either "truthy" or "falsy" based on their behavior in boolean contexts (such as conditions in `if` statements and loops). Understanding truthy and falsy values is important when working with conditions and logical operations. Here are the truthy and falsy values in JavaScript:

**Falsy Values**:
1. `false`
2. `0` (zero)
3. `''` (empty string)
4. `null`
5. `undefined`
6. `NaN` (Not-a-Number)

Example:
```javascript
if (false) {
    // This block won't be executed
}

if (0) {
    // This block won't be executed
}

if ('') {
    // This block won't be executed
}

if (null) {
    // This block won't be executed
}

if (undefined) {
    // This block won't be executed
}

if (NaN) {
    // This block won't be executed
}
```

**Truthy Values**:
Any value that is not falsy is considered truthy. This includes, but is not limited to:
1. Non-empty strings (`'hello'`)
2. Numbers other than 0 (`42`)
3. Arrays (`[1, 2, 3]`)
4. Objects (`{ key: 'value' }`)
5. Functions (`function() { ... }`)
6. Positive and negative infinity (`Infinity`, `-Infinity`)

Example:
```javascript
if ('hello') {
    // This block will be executed
}

if (42) {
    // This block will be executed
}

if ([1, 2, 3]) {
    // This block will be executed
}

if ({ key: 'value' }) {
    // This block will be executed
}

if (function() {}) {
    // This block will be executed
}

if (Infinity) {
    // This block will be executed
}
```

Understanding truthy and falsy values helps you write concise and effective code when working with conditions and logical expressions.
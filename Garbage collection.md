#garbage-collection #js-concept #js 

# Definition:

In JavaScript, garbage collection is the automatic process of reclaiming memory that is no longer needed by the program. It helps manage memory efficiently by identifying and freeing up memory that is no longer in use, allowing developers to focus on writing code without explicitly de-allocating memory.

```js
// Example 1: garbage collected
function createObjects() {
  var obj1 = {};
  var obj2 = {};
  obj1.ref = obj2;
  obj2.ref = obj1;
}
createObjects();
```

```js
// Example 2
function createObjects() {
  var obj1 = {};
  var obj2 = {};
  obj1.ref = obj2;
  obj2.ref = obj1;
  return obj1;
}
var result = createObjects();
```

As long as there are references to an object, it will not be garbage collected.


#json #js #js-concept 

```js
// JSON.stringify() --> JS object to JSON String
// JSON.parse() -->  JSON String to JS Object

let student = {
    name: "Rahim",
    age: 26,
    hometown: "Dhaka"
};

let student_json = JSON.stringify(student);

console.log(student_json);

let student_new = JSON.parse(student_json);
console.log(student_new);
```


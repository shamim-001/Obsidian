#tech-book 
[Source Code](https://github.com/PacktPublishing/JavaScript-from-Beginner-to-Professional)

# 3. JavaScript Multiple Values
## Array methods
```js
splice()
arr.splice(1, 3);
//adding
concat()
// deleting
pop()
shift()

// finding
find()
arr8 = [ 2, 6, 7, 8 ]; let findValue = arr8.find(function(e) { return e === 6}); let findValue2 = arr8.find(e => e === 10); console.log(findValue, findValue2);

indexOf()
`If the value is not found, it will return -1`

lastIndexOf()
let animals = ["dog", "horse", "cat", "platypus", "dog"]; 
let lastDog = animals.lastIndexOf("dog");

// Sorting
let names = ["James", "Alicia", "Fatiha", "Maria", "Bert"]; names.sort();
`It sorts numbers from small to high and strings A-Z`

// Reversing
names.reverse();
```

# 5. Loops
```js
while
do while
for
for in
for of
```

The `startsWith()` method just checks whether the string starts with a certain character
```js
let names = ["Chantal", "John", "Maxime", "Bobbi", "Jair"]; for (let i = 0; i < names.length; i ++){ if(names[i].startsWith("M")){ delete names[i]; continue; } names[i] = "hello " + names[i]; } console.log(names);
```

- `for of`: It cannot be used to change the value associated with the index as we can do with the regular loop.
```js
let names = ["Chantal", "John", "Maxime", "Bobbi", "Jair"]; for (let name of names){ 
	console.log(name); 
}
```

`for in`
```js
let car = { model: "Golf", make: "Volkswagen", year: 1999, color: "black", }; 
for (let prop in car){ 
	console.log(car[prop]); 
}
```



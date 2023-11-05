https://www.bigocheatsheet.com/

- how efficient your code is
- Time complexity - based on number of operation
- Space complexity - amount of memory the code uses
- ![[Pasted image 20231102092534.png]]
best case - average case - worst case

- O(n)- straight line on graph:
```js
const logItems = (n) => {
  for (let i = 0; i < n; i++) {
    console.log(i);
  }
};

logItems(10);
```

- Big O: Drop constant
```js
const logItems = (n) => {
  for (let i = 0; i < n; i++) {
    console.log(i);
  }

  for (let j = 0; j < n; j++) {
    console.log(j);
  }
};

logItems(3);
```
O(n+n) -> O(2n) -> O(n)

- O(n^2) - It's generally considered inefficient code
![[Pasted image 20231102095244.png]]
```js
const logItems = (n) => {
  for (let i = 0; i < n; i++) {
    for (let j = 0; j < n; j++) {
      console.log(i, j);
    }
  }
};

logItems(3);
```

- Big(O): Drop non-dominants
```js
const logItems = (n) => {
  for (let i = 0; i < n; i++) {
    for (let j = 0; j < n; j++) {
      console.log(i, j);
    }
  }

  for (let k = 0; k < n; k++) {
    console.log(k);
  }
};

logItems(3);
```
O(n^2 + n) -> O(n^2)

- Big O: O(1) - The most efficient code
![[Pasted image 20231102100730.png]]
```js
const logItem = (n) => {
	return n + n + n ...
}
```

- O(log n)
![[Pasted image 20231102101325.png]]

- Different terms for inputs
```js
const logItems = (a,b) => {
  for (let i = 0; i < a; i++) {
    console.log(i);
  }

  for (let j = 0; j < b; j++) {
    console.log(j);
  }
};

logItems(3);
```
O(a + b)

```js
const logItems = (a,b) => {
  for (let i = 0; i < a; i++) {
    for (let j = 0; j < b; j++) {
      console.log(i, j);
    }
  }
};

logItems(3);
```
O(a * b)

- Big O: array
array.push() and array.pop() are both O(1)

array.shift() and array.unshift() are both O(n)

array.splice(1,0,'hi') -> O(n)
adding or removing in the array

finding an element:
search by value - O(n)
search by index - O(1)

![[Pasted image 20231105153254.png]]


The execution process js program can be divided into two steps: ==compilation and execution.==


1. Compilation: During the compilation phase, the JavaScript engine scans through the entire code and performs some initial setup tasks. One important task that happens during compilation is the creation of an execution context, which includes the creation of the variable and function declarations.

==Hoisting== is a JavaScript behavior that allows variables and function declarations to be moved to the top of their respective scopes during the compilation phase. It means that you can use variables and call functions before they are actually declared in the code.

It's important to note that only variable and function declarations are hoisted, not their assignments or initializations.

==using `let` instead of `var` prevents hoisting==


# questions:
```js
// Question 1
function test(){
    var x  = 10;
    var x;
    console.log('X is ' + x);
}
test();


// Question 2
function varTest() {
    var x = 1;
    {
        var x = 2;  
        console.log(x);  
    }
    console.log(x); 
}

// Question 3
function letTest() {
    let x = 1;
    let x = 2;
    console.log(x); 
    console.log(x);
}


// Question 4
function do_something() {
    console.log(bar); 
    var bar = 111;
    console.log(bar);
}


// Question 5
var rat = 10
function getRate() {
  if (rat === undefined) {
      var rate = 6;
      return rate;
   } else {
      return 10;
   }
}
console.log("Rate is", getRate());
// If there is a conflict between global variable and local variable, local variable always wins.
```


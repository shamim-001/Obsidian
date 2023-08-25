#js-project #project-code #project-note 
First JS project done.
# Source Code: [TaskList Source code](https://github.com/shamim-001/TaskList)

# App link: [TaskList](https://tasklist-flame.vercel.app/)

I tried to implement the "DRY" concept. 

# Notes
## note 1

When you retrieve the value of the taskInput element using let newValue = taskInput.value;, it assigns the current value of the taskInput element to the newValue variable. However, when you later set newValue = "";, you are only modifying the value of the newValue variable and not the actual taskInput element.
```js
// Define UI elements

const form = document.querySelector("#task-form");

const taskList = document.querySelector("ul");

const clearBtn = document.querySelector("#clear-task-btn");

const filter = document.querySelector("#task-filter");

const taskInput = document.querySelector("#new-task");

// Define event listeners

form.addEventListener("submit", addTask);

// Define functions

function addTask(e) {

let newValue = taskInput.value;

if (newValue === "") {

alert("Add a task");

} else {

let li = document.createElement("li");

let textNode = document.createTextNode(newValue);

li.appendChild(textNode);

taskList.appendChild(li);

taskInput.value = "";

}

}
```


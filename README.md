# Todolist
# Ex03 To-Do List using JavaScript
## Date:17-11-2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```

<!DOCTYPE html>
<html>
<head>
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>My To-Do List</h1>

        <div class="input-box">
            <input type="text" id="taskInput"
            placeholder="Enter your task">

            <button onclick="addTask()">Add</button>
        </div>

        <ul id="taskList"></ul>

        <button class="clear" onclick="clearTasks()">
            Clear All
        </button>
    </div>

    <script src="script.js"></script>
</body>
</html>

```
script.js
```

function addTask() {
    let input = document.getElementById("taskInput");
    let task = input.value.trim();

    if (task === "") {
        alert("Please enter a task!");
        return;
    }

    let li = document.createElement("li");

    let span = document.createElement("span");
    span.textContent = task;

    span.onclick = function() {
        span.classList.toggle("completed");
    };

    let deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";
    deleteBtn.className = "delete";

    deleteBtn.onclick = function() {
        li.remove();
    };

    li.appendChild(span);
    li.appendChild(deleteBtn);

    document.getElementById("taskList").appendChild(li);

    input.value = "";
}

function clearTasks() {
    document.getElementById("taskList").innerHTML = "";
}

```
style.css
```

body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    display: flex;
    justify-content: center;
    padding-top: 50px;
}

.container {
    background: white;
    width: 350px;
    padding: 25px;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 0 10px gray;
}

h1 {
    color: #333;
}

.input-box {
    display: flex;
    gap: 5px;
}

input {
    flex: 1;
    padding: 10px;
}

button {
    padding: 10px;
    background: #007bff;
    color: white;
    border: none;
    cursor: pointer;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    background: #eee;
    margin: 10px 0;
    padding: 10px;
    display: flex;
    justify-content: space-between;
}

.completed {
    text-decoration: line-through;
    color: gray;
}

.delete {
    background: red;
}

.clear {
    background: #555;
    margin-top: 10px;
}

```

## OUTPUT
![alt text](<Screenshot 2026-11-17 170831.png>)
## RESULT
The program for creating To-do list using JavaScript is executed successfully.

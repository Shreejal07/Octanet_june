Step 1: Set Up Your Project

Create a new directory for your project and navigate into it.

```bash
mkdir todo-list
cd todo-list
Step 2: Create HTML Structure
Create an index.html file and set up the basic structure of your HTML document.

html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>To-Do List</h1>
        <input type="text" id="taskInput" placeholder="Add a new task...">
        <ul id="taskList"></ul>
    </div>
    <script src="script.js"></script>
</body>
</html>
Step 3: Style Your To-Do List
Create a styles.css file to add some basic styles to your to-do list.

css
Copy code
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 600px;
    margin: 50px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
}

input[type="text"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 20px;
    border: 1px solid #ccc;
    border-radius: 3px;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    padding: 10px;
    border-bottom: 1px solid #ccc;
}

.completed {
    text-decoration: line-through;
}
Step 4: Implement JavaScript Functionality
Create a script.js file to add interactivity to your to-do list.

javascript
Copy code
const taskInput = document.getElementById('taskInput');
const taskList = document.getElementById('taskList');

taskInput.addEventListener('keypress', function(e) {
    if (e.key === 'Enter' && taskInput.value.trim() !== '') {
        addTask(taskInput.value.trim());
        taskInput.value = '';
    }
});

function addTask(taskText) {
    const li = document.createElement('li');
    li.textContent = taskText;
    li.addEventListener('click', function() {
        li.classList.toggle('completed');
    });
    taskList.appendChild(li);
}
Step 5: Test Your To-Do List
Open index.html in your web browser to test your to-do list application. You should be able to add tasks by typing in the input field and pressing Enter.
![Screenshot (61)](https://github.com/Shreejal07/Octanet_june/assets/158570133/4b858512-8f4d-42c9-b8f7-dc596d8d3e8b)


![Screenshot (62)](https://github.com/Shreejal07/Octanet_june/assets/158570133/08b9ea5b-9883-4861-82e1-9e26858d09ef)
















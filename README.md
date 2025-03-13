<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Automation App</title>
</head>
<body>
    <h1>Welcome to My Automation App</h1>
    <p>This app helps businesses streamline their tasks using AI.</p>

    <label for="taskInput">Enter a task:</label>
    <input type="text" id="taskInput" placeholder="e.g. Send email reminder">
    <button onclick="automateTask()">Automate Task</button>

    <h2>Automated Tasks:</h2>
    <ul id="taskList"></ul>

    <script>
        function automateTask() {
            let taskInput = document.getElementById('taskInput').value;
            if(taskInput === '') {
                alert('Please enter a task!');
                return;
            }
            let taskList = document.getElementById('taskList');
            let newTask = document.createElement('li');
            newTask.textContent = taskInput;
            taskList.appendChild(newTask);
            document.getElementById('taskInput').value = '';
        }
    </script>
</body>
</html>

# online
asdffdsfgf
**Online Project Management System**

<!DOCTYPE html>
<html>
<head>
    <title>Online Project Management</title>
    <style>
        body {
            font-family: Arial;
            background: #eef2f7;
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 750px;
            margin: auto;
            background: white;
            padding: 25px;
            border-radius: 12px;
        }

        h1 {
            text-align: center;
            color: #263c63;
        }

        input, select, button {
            width: 100%;
            padding: 12px;
            margin: 8px 0;
            box-sizing: border-box;
        }

        button {
            background: #2563eb;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }

        .project {
            background: #f1f5f9;
            padding: 15px;
            margin-top: 12px;
            border-radius: 8px;
        }

        .delete {
            background: #dc2626;
        }
    </style>
</head>

<body>

<div class="container">
    <h1>Online Project Management System</h1>

    <h3>Add New Project</h3>

    <input type="text" id="name"
           placeholder="Enter Project Name">

    <input type="text" id="description"
           placeholder="Enter Project Description">

    <input type="date" id="deadline">

    <select id="status">
        <option>Pending</option>
        <option>In Progress</option>
        <option>Completed</option>
    </select>

    <button onclick="addProject()">Add Project</button>

    <h2>Project List</h2>

    <div id="projectList"></div>
</div>

<script>
    function addProject() {
        let name = document.getElementById("name").value;
        let description = document.getElementById("description").value;
        let deadline = document.getElementById("deadline").value;
        let status = document.getElementById("status").value;

        if (name === "" || description === "") {
            alert("Please enter project details!");
            return;
        }

        let project = document.createElement("div");
        project.className = "project";

        project.innerHTML = `
            <h3>${name}</h3>
            <p>${description}</p>
            <p>Deadline: ${deadline || "Not set"}</p>
            <p>Status: ${status}</p>
            <button class="delete"
                onclick="this.parentElement.remove()">
                Delete Project
            </button>
        `;

        document.getElementById("projectList")
            .appendChild(project);

        document.getElementById("name").value = "";
        document.getElementById("description").value = "";
        document.getElementById("deadline").value = "";
    }
</script>

</body>
</html>

The Online Project Management System is a web-based application designed to manage projects efficiently. It allows users to create projects, assign tasks, track progress, and manage deadlines. It helps students and teams collaborate easily, improves productivity, and saves time through online project management.

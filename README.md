<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dear Future - Login</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            background-color: #f5e1c0;
            text-align: center;
            padding: 20px;
        }
        .container {
            background: #d4a373;
            padding: 20px;
            border-radius: 15px;
            display: inline-block;
        }
        input, button {
            padding: 10px;
            font-size: 16px;
            margin-top: 10px;
        }
        button {
            background-color: #8b5e3b;
            color: white;
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #5c3d2e;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container" id="login-container">
        <h1>Login to Dear Future</h1>
        <input type="email" id="email" placeholder="Enter your email"><br>
        <input type="password" id="password" placeholder="Enter your password"><br>
        <button onclick="login()">Login</button>
    </div>

<div class="container hidden" id="schedule-container">
        <h1>Schedule Your Future Message</h1>
        <label for="schedule-date">Choose a Date:</label>
        <input type="date" id="schedule-date" min="">
        <br>
        <button onclick="goToForm()">Proceed</button>
    </div>

<script>
        function login() {
            let email = document.getElementById('email').value;
            let password = document.getElementById('password').value;
            if (email && password) {
                document.getElementById('login-container').classList.add('hidden');
                document.getElementById('schedule-container').classList.remove('hidden');
            } else {
                alert("Please enter your credentials.");
            }
        }

    let today = new Date().toISOString().split('T')[0];
        document.getElementById('schedule-date').setAttribute('min', today);

        function goToForm() {
            let selectedDate = document.getElementById('schedule-date').value;
            if (selectedDate) {
                window.location.href = `form.html?date=${selectedDate}`;
            } else {
                alert("Please select a date.");
            }
        }
    </script>
</body>
</html>




   




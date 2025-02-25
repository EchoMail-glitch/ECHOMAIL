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
    </style>
</head>
<body>
    <div class="container">
        <h1>Login to Dear Future</h1>
        <input type="email" id="email" placeholder="Enter your email"><br>
        <input type="password" id="password" placeholder="Enter your password"><br>
        <button onclick="login()">Login</button>
    </div>

<script>
        function login() {
            let email = document.getElementById('email').value;
            let password = document.getElementById('password').value;
            if (email && password) {
                window.location.href = 'schedule.html';
            } else {
                alert("Please enter your credentials.");
            }
        }
    </script>
</body>
</html>

<!-- Schedule Page (schedule.html) -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dear Future - Schedule a Message</title>
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
        input[type="date"], select {
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
    </style>
</head>
<body>
    <div class="container">
        <h1>Schedule Your Future Message</h1>
        <label for="schedule-date">Choose a Date:</label>
        <input type="date" id="schedule-date" min="">
        <br>
        <button onclick="goToForm()">Proceed</button>
    </div>

<script>
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

<!-- Form Page (form.html) -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dear Future - Select Message Type</title>
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
        select, button {
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
    </style>
</head>
<body>
    <div class="container">
        <h1>Select Your Message Type</h1>
        <label for="message-type">Choose a Message Type:</label>
        <select id="message-type">
            <option value="text">Text Message (Free)</option>
            <option value="audio">Audio Message (Paid)</option>
            <option value="video">Video Message (Paid)</option>
            <option value="gift">Physical Gift (India Only)</option>
        </select>
        <br>
        <button onclick="proceed()">Next</button>
    </div>

<script>
        function proceed() {
            let messageType = document.getElementById('message-type').value;
            let userLocation = "India"; // This should be dynamically fetched in a real app
            
            if (messageType === "gift" && userLocation !== "India") {
                alert("Physical Gift is only available in India.");
                return;
            }
            
            if (messageType === "gift" || messageType === "audio" || messageType === "video") {
                window.location.href = "payment.html";
            } else {
                window.location.href = "compose.html?type=" + messageType;
            }
        }
    </script>
</body>
</html>



   




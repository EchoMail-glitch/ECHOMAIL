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
        <p><a href="#" onclick="forgotPassword()">Forgot Password?</a></p>
    </div>

<div class="container hidden" id="reset-password-container">
        <h1>Reset Password</h1>
        <input type="email" id="reset-email" placeholder="Enter your email"><br>
        <button onclick="sendResetCode()">Send Code</button>
        <div class="hidden" id="code-container">
            <input type="text" id="reset-code" placeholder="Enter Code"><br>
            <input type="password" id="new-password" placeholder="New Password"><br>
            <input type="password" id="confirm-password" placeholder="Confirm Password"><br>
            <button onclick="resetPassword()">Submit</button>
        </div>
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
            
            let passwordPattern = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,12}$/;
            
            if (!passwordPattern.test(password)) {
                alert("Password must be 8-12 characters long, include at least 1 uppercase, 1 lowercase, 1 number, and 1 special character.");
                return;
            }
            
            if (email && password) {
                document.getElementById('login-container').classList.add('hidden');
                document.getElementById('schedule-container').classList.remove('hidden');
                alert("Login successful!");
            } else {
                alert("Please enter your credentials.");
            }
        }

        function forgotPassword() {
            document.getElementById('login-container').classList.add('hidden');
            document.getElementById('reset-password-container').classList.remove('hidden');
        }
        
        function sendResetCode() {
            let email = document.getElementById('reset-email').value;
            if (email) {
                alert("A reset code has been sent to your email.");
                document.getElementById('code-container').classList.remove('hidden');
            } else {
                alert("Please enter your email.");
            }
        }

     function resetPassword() {
            let code = document.getElementById('reset-code').value;
            let newPassword = document.getElementById('new-password').value;
            let confirmPassword = document.getElementById('confirm-password').value;
            
            let passwordPattern = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,12}$/;
            
            if (!passwordPattern.test(newPassword)) {
                alert("Password must be 8-12 characters long, include at least 1 uppercase, 1 lowercase, 1 number, and 1 special character.");
                return;
            }
            
            if (newPassword !== confirmPassword) {
                alert("Passwords do not match.");
                return;
            }
            
            if (code) {
                alert("Password reset successful!");
                document.getElementById('reset-password-container').classList.add('hidden');
                document.getElementById('schedule-container').classList.remove('hidden');
            } else {
                alert("Invalid code.");
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




   




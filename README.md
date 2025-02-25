<!-- login.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        body {
            background-color: #FADADD; /* Pink Salt Color */
            text-align: center;
            font-family: Arial, sans-serif;
        }
        .container {
            background-color: white;
            width: 300px;
            padding: 20px;
            margin: auto;
            margin-top: 100px;
            border-radius: 15px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        .hearts::before {
            content: "\2764\FE0F \2764\FE0F \2764\FE0F";
            color: pink;
            font-size: 20px;
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
        }
        input {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border-radius: 10px;
            border: 1px solid #ccc;
        }
        button {
            background-color: #ff69b4;
            color: white;
            padding: 10px;
            width: 100%;
            border: none;
            border-radius: 10px;
            cursor: pointer;
        }
        .google-btn {
            background-color: #db4437;
        }
    </style>
</head>
<body>
    <div class="container hearts">
        <h2>Login Page</h2>
        <input type="email" id="email" placeholder="Email or Phone Number">
        <input type="password" id="password" placeholder="Password">
        <button onclick="login()">Login</button>
        <button class="google-btn" onclick="googleLogin()">Continue with Google</button>
        <p>New user? <a href="register.html">Register here</a></p>
    </div>
    <script>
        async function login() {
            const email = document.getElementById("email").value;
            const password = document.getElementById("password").value;
            const res = await fetch("http://localhost:5000/login", {
                method: "POST",
                headers: { "Content-Type": "application/json" },
                body: JSON.stringify({ email, password }),
            });
            const data = await res.json();
            if (data.token) {
                localStorage.setItem("token", data.token);
                window.location.href = "dashboard.html";
            } else {
                alert(data.message);
            }
        }
    </script>
</body>
</html>





   




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EchoMail - Smart Email Support</title>
        <!-- CSS Inside HTML -->
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
        }
        h1 { color: #e63946; }
        form { background: white; padding: 20px; width: 300px; margin: auto; border-radius: 8px; }
        input, button { width: 100%; margin: 10px 0; padding: 8px; }
        button { background: #e63946; color: white; border: none; cursor: pointer; }
    </style>

</head>
<body>
    <h1>Welcome to EchoMail</h1>
    <p>Your Smart Email Management Solution</p>
    <form onsubmit="submitForm(); return false;">
        <input type="text" id="businessName" placeholder="Enter Business Name" required>
        <input type="email" id="email" placeholder="Enter Email" required>
        <input type="tel" id="contactNumber" placeholder="Enter Contact Number" required>
        <button type="submit">Enroll</button>
    </form>
   <!-- JavaScript Inside HTML -->
    <script>
        function submitForm() {
            let businessName = document.getElementById('businessName').value;
            let email = document.getElementById('email').value;
            let contactNumber = document.getElementById('contactNumber').value;

  if (businessName && email && contactNumber) {
                alert("Thank you for enrolling! Our team will contact you soon.");
            } else {
                alert("Please fill in all fields before submitting.");
            }
        }
    </script>

</body>
</html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EchoMail - Smart Email Support</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #000000, #00B2CA, #ffffff);
            color: #ffffff;
        }
        header {
            background: #000000;
            padding: 20px;
            text-align: center;
            color: #ffffff;
            font-size: 24px;
            font-weight: bold;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .logo {
            position: absolute;
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
            height: 50px;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: auto;
            padding: 20px;
            text-align: center;
        }
        .cta {
            background-color: #00B2CA;
            color: white;
            padding: 15px;
            display: inline-block;
            margin-top: 20px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            cursor: pointer;
        }
        .features, .vision, .unique {
            margin-top: 40px;
            padding: 20px;
            background-color: rgba(26, 26, 26, 0.9);
            box-shadow: 0 0 10px rgba(0, 178, 202, 0.5);
            border-radius: 8px;
        }
        .features h2, .vision h2, .unique h2 {
            color: #00B2CA;
        }
        footer {
            background-color: #000000;
            color: white;
            text-align: center;
            padding: 10px;
            margin-top: 20px;
        }
        .enrollment {
            margin-top: 40px;
            padding: 20px;
            background-color: rgba(0, 178, 202, 0.2);
            border-radius: 8px;
        }
        .enrollment input, .enrollment button {
            padding: 10px;
            margin: 10px;
            width: 80%;
        }
        @media (max-width: 768px) {
            header {
                font-size: 18px;
                padding: 15px;
            }
            .logo {
                height: 40px;
                left: 10px;
            }
            .cta {
                display: block;
                width: 80%;
                margin: 10px auto;
            }
            .container {
                width: 95%;
            }
        }
    </style>
</head>
<body>
    <header>
       <img src="https://yourwebsite.com/EchoMAIL_NEW_LOGO.png" alt="EchoMail Logo" width="150">

Welcome to EchoMail - Smart Email Support
    </header>
    
<div class="container">
        <h1>Effortless Email Support for Your Business</h1>
        <p>At EchoMail, we specialize in providing seamless and efficient email support solutions for businesses of all sizes. Our goal is to ensure that every customer query is handled professionally, promptly, and with a personal touch. With our expert team and smart automation, we help businesses maintain strong customer relationships without the stress of managing overwhelming email volumes.</p>
        <button class="cta" onclick="scrollToSection('enroll')">🚀 Get Started</button>
        <button class="cta" onclick="scrollToSection('contact')">📩 Talk to Us</button>
    </div>
    
<div class="container features">
        <h2>Why Choose EchoMail?</h2>
        <p>✨ 24/7 Email Support: Ensure your customers always receive timely responses.</p>
        <p>⚡ Smart Email Sorting: Prioritize important emails and automate responses.</p>
        <p>🔒 Secure & Confidential: Your customer interactions remain private and protected.</p>
        <p>📈 Scalable for Growth: Flexible solutions that grow with your business needs.</p>
        <p>💡 Easy Integration: Works seamlessly with Gmail, Outlook, and other platforms.</p>
    </div>
    
<div class="container unique">
        <h2>Unique Features</h2>
        <p>✔ AI-Powered Prioritization: Our system learns which emails are most important and handles them first.</p>
        <p>✔ Customizable Automation: Set up rules for auto-responses and workflow triggers.</p>
        <p>✔ Real-Time Analytics: Track customer queries and measure response efficiency.</p>
        <p>✔ Multi-Platform Support: Manage emails across multiple accounts from a single dashboard.</p>
    </div>
    
<div class="container vision">
        <h2>Our Vision</h2>
        <p>At EchoMail, our vision is to revolutionize customer support by offering businesses a hassle-free and intelligent email management solution. We believe in providing technology-driven, yet human-centric support services that empower businesses to enhance customer satisfaction, reduce response times, and focus on what they do best. Join us on this journey as we shape the future of email communication.</p>
    </div>
    
<div id="enroll" class="container enrollment">
        <h2>Enroll Now</h2>
        <p>Sign up today and let EchoMail streamline your email management.</p>
<form action="https://formspree.io/f/xwpvnaao" method="POST">
      <input type="text" name="businessName" placeholder="Enter Business Name" required>
        <input type="email" name="email" placeholder="Enter Email" required>
        <input type="tel" name="contactNumber" placeholder="Enter Contact Number" required>
     <button onclick="submitForm()">Submit</button>
   
 </form>



<footer>
<p>Follow us on: 
            <a href="https://www.linkedin.com/in/echo-mail-408174350" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn" width="20"></a> 
            <a href="https://www.instagram.com/echomail_care?igsh=MWV2NjhkcXlwNmZiYg==" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/174/174855.png" alt="Instagram" width="20"></a> 
            <a href="https://twitter.com/echomailcare" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/733/733579.png" alt="Twitter" width="20"></a>
        </p>
        &copy; 2025 EchoMail. All Rights Reserved.
    
<footer>
 <script>
        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
        }

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



   




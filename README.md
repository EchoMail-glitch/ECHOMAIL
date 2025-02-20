<script>
    document.addEventListener("DOMContentLoaded", function() {
        let unwantedText = document.querySelector("h1"); // Adjust if needed
        if (unwantedText && unwantedText.innerText.trim() === "ECHOMAIL") {
            unwantedText.style.display = "none";
        }
    });
</script>

<path fill="#4458F6" d="M-.072-.154h44.133v44.308H-.072V-.154Z" data-color="1"></path>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
       .logo-container {
    display: flex;
    justify-content: left;
    align-items: center;
    background-color: black; /* Black background */
    padding: 30px; /* Adjust padding */
    max-height: 300px; /* Reduce the height */
    overflow: hidden; /* Prevent extra spacing */
}

.logo-container img {
    max-width: 100%;
    height: auto;
    max-height: 200px; /* Reduce image height */
}

}
        .cta {
            background-color: #00B2CA;
            color: white;
            padding: 15px;
            display: inline-block;
            margin-top: 20px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 1px;
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
                height:30px;
                left: 30px;
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
<div style="display: flex; align-items: center; padding: 20px;">
   <img src="EchoMAIL NEW LOGO.png" alt="EchoMail Logo"  style="width: 120px; height: auto; margin-left: 0;">
    <h2 style="color: white; margin-left: 20px;">Seamless Email Management</h2>
</div>

<hr>
</header>
    
<div class="container">
        <h1>Effortless Email Support for Your Business</h1>
        <p>At EchoMail, we specialize in providing seamless and efficient email support solutions for businesses of all sizes. Our goal is to ensure that every customer query is handled professionally, promptly, and with a personal touch. With our expert team and smart automation, we help businesses maintain strong customer relationships without the stress of managing overwhelming email volumes.</p>
        <button class="cta" onclick="scrollToSection('enroll')">🚀 Get Started</button>
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
     <h2 style="color: #004466;">📩 Ready to Connect? Let's Talk!</h2>
<p style="color: #004466;">Have questions? Need support? We’re here for you!</p>

<p><strong>Email Us:</strong> 
    <a href="mailto:echomailcare@gmail.com" style="color: #004466; text-decoration: none; font-weight: bold;">
        echomailcare@gmail.com
    </a>
</p>

<p style="color: #004466;">Or, simply fill out our contact form, and we’ll get back to you ASAP! 🚀</p>

<form action="https://formspree.io/f/xwpvnaao" method="POST">
      <input type="text" name="businessName" placeholder="Enter Business Name" required>
        <input type="email" name="email" placeholder="Enter Email" required>
        <input type="tel" name="contactNumber" placeholder="Enter Contact Number" required>
     <button onclick="submitForm()">Submit</button>
   
 </form>



<footer>

<p> 
<footer style="background-color: #000000; color: white; text-align: center; padding: 20px;">
    <h2 style="margin: 0;">&nbsp;EchoMail</h2>
     <!-- Clickable Privacy Policy -->
    <a href="privacy-policy.html.docx" style="color: white; text-decoration: none; display: block; margin: 5px 0;">
        Privacy Policy
    </a>   
Follow us on: 
               
<div style="margin: 10px 0;">            
<a href="https://www.linkedin.com/in/echo-mail-408174350" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn" width="25"></a> &nbsp;
    
            
<a href="https://www.instagram.com/echomail_care?igsh=MWV2NjhkcXlwNmZiYg==" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/174/174855.png" alt="Instagram" width="25"></a> &nbsp;
            
<a href="https://twitter.com/echomailcare" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/733/733579.png" alt="Twitter" width="25"></a> &nbsp;
</div>

<p style="margin: 0;">All Rights Reserved © EchoMail</p>
    
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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EchoMail</title>
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
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: relative;
        }
        .menu-button {
            font-size: 24px;
            cursor: pointer;
            background: none;
            border: none;
            color: white;
        }
        .menu {
            display: none;
            position: absolute;
            top: 60px;
            right: 20px;
            background: rgba(0, 0, 0, 0.9);
            border-radius: 8px;
            padding: 10px;
        }
        .menu a {
            display: block;
            color: white;
            text-decoration: none;
            padding: 10px;
        }
        .menu a:hover {
            background: #00B2CA;
        }
        .pricing, .features {
            margin-top: 40px;
            padding: 20px;
            background-color: rgba(0, 178, 202, 0.2);
            border-radius: 8px;
            text-align: center;
        }
        .pricing h2, .features h2 {
            color: #004466;
        }
        .pricing table {
            width: 100%;
            background: white;
            color: black;
            text-align: left;
            border-collapse: collapse;
        }
        .pricing th, .pricing td {
            padding: 10px;
            border: 1px solid #004466;
        }
    </style>
</head>
<body>
    <header>
        <div style="display: flex; align-items: center;">
            <img src="EchoMAIL NEW LOGO.png" alt="EchoMail Logo" style="width: 120px; height: auto;">
            <h2 style="color: white; margin-left: 20px;">Seamless Email Management</h2>
        </div>
        <button class="menu-button" onclick="toggleMenu()">☰</button>
        <div class="menu" id="menu">
            <a href="purpose.html">Purpose</a>
            <a href="packages.html">Packages</a>
            <a href="about.html">About Us</a>
            <a href="contact.html">Contact</a>
            <a href="faq.html">FAQ</a>
        </div>
    </header>

<div class="features">
        <h2>🚀 Key Features</h2>
        <p>✅ 24/7 Email Support</p>
        <p>✅ AI-Powered Email Sorting</p>
        <p>✅ Secure & Confidential Email Handling</p>
        <p>✅ Real-Time Analytics & Performance Tracking</p>
        <p>✅ Multi-Platform Email Integration</p>
        <p>✅ Automated Responses & Customizable Workflows</p>
    </div>

<div class="pricing">
        <h2>📦 Our Pricing Plans</h2>
        <table>
            <tr>
                <th>Plan</th>
                <th>Features</th>
                <th>Price</th>
            </tr>
            <tr>
                <td>Free Trial</td>
                <td>1 Week Free - Limited Features</td>
                <td>$0</td>
            </tr>
            <tr>
                <td>Basic Plan</td>
                <td>Email Support for Small Businesses</td>
                <td>$9.99/month</td>
            </tr>
            <tr>
                <td>Pro Plan</td>
                <td>Advanced Features & Priority Support</td>
                <td>$19.99/month</td>
            </tr>
        </table>
    </div>

<script>
        function toggleMenu() {
            let menu = document.getElementById("menu");
            menu.style.display = menu.style.display === "block" ? "none" : "block";
        }
    </script>
</body>
</html>




   




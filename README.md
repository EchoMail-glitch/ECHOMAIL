<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dear Future - Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 50px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
        }
        button:hover {
            background-color: #45a049;
        }
        a {
            display: block;
            margin-top: 10px;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Login to Dear Future</h2>
        <input type="email" id="email" placeholder="Enter your email" required>
        <input type="password" id="password" placeholder="Enter your password" required>
        <button onclick="login()">Login</button>
        <a href="#">Forgot Password?</a>
        <a href="#">Create an Account</a>
    </div>

<script>
        function login() {
            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;
            if (email && password) {
                alert('Login Successful! Redirecting to Calendar...');
                window.location.href = 'calendar.html';
            } else {
                alert('Please enter email and password');
            }
        }
    </script>
</body>
</html>
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
        input[type="date"] {
            padding: 10px;
            font-size: 16px;
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
        // Set min date to current date
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
</html>import { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Textarea } from "@/components/ui/textarea";
import { Button } from "@/components/ui/button";
import { BarChart, Bar, XAxis, YAxis, Tooltip, ResponsiveContainer } from "recharts";
import Sentiment from "sentiment";

export default function FeedbackAI() {
  const [feedback, setFeedback] = useState("");
  const [analysis, setAnalysis] = useState(null);
  const sentiment = new Sentiment();

  const analyzeFeedback = () => {
    const result = sentiment.analyze(feedback);
    const insights = {
      sentimentScore: result.score,
      words: result.words,
      positiveWords: result.positive,
      negativeWords: result.negative,
    };
    setAnalysis(insights);
  };

  return (
    <div className="p-4 space-y-4">
      <Card>
        <CardContent className="p-4 space-y-4">
          <h2 className="text-xl font-bold">Submit Feedback</h2>
          <Textarea
            value={feedback}
            onChange={(e) => setFeedback(e.target.value)}
            placeholder="Type your feedback here..."
            className="w-full p-2 border rounded"
          />
          <Button onClick={analyzeFeedback} className="w-full">
            Analyze Feedback
          </Button>
        </CardContent>
      </Card>
      {analysis && (
        <Card>
          <CardContent className="p-4">
            <h2 className="text-xl font-bold">AI Insights</h2>
            <p>Sentiment Score: {analysis.sentimentScore}</p>
            <p>Positive Words: {analysis.positiveWords.join(", ") || "None"}</p>
            <p>Negative Words: {analysis.negativeWords.join(", ") || "None"}</p>
            <h3 className="mt-4 font-bold">Sentiment Distribution</h3>
            <ResponsiveContainer width="100%" height={200}>
              <BarChart data={[{ name: "Score", value: analysis.sentimentScore }]}> 
                <XAxis dataKey="name" />
                <YAxis />
                <Tooltip />
                <Bar dataKey="value" fill={analysis.sentimentScore >= 0 ? "#4caf50" : "#f44336"} />
              </BarChart>
            </ResponsiveContainer>
          </CardContent>
        </Card>
      )}
    </div>
  );
}


   




import { useState } from "react";
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


   




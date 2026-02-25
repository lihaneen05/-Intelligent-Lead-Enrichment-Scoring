🚀 Intelligent Lead Enrichment & Scoring Pipeline
An automated workflow built in n8n that intercepts new lead data, enriches it using external APIs, and uses conditional logic to route high-priority leads to a dedicated Slack channel.

🧠 Project Overview
The goal of this project was to move away from generic, "dumb" data entry and create a system that thinks before it acts. Instead of notifying the team about every single lead, this workflow:
Enriches data with real-time scoring.
Evaluates the lead based on custom business rules.
Alerts the team only when a lead is deemed "High Priority."

🛠️ The Workflow Architecture
Trigger: Manual execution node for controlled testing and data simulation.
Data Input: A JavaScript node that simulates incoming lead data (e.g., Name: "Haneen").
Enrichment (HTTP Request): Connects to the Agify API to fetch a numeric probability score (Age: 51) based on the lead's name.
Scoring Logic (If Node): An "Intelligent Gatekeeper" that checks if the Enrichment Score is greater than 50.
Routing (Slack Node): High-priority leads are formatted into a professional alert and sent to the #high-priority-leads Slack channel.

✅ Key Success Indicators
Automated Decision Making: The system successfully identified a lead with a score of 51 and automatically routed it to the True branch.
Real-time Communication: The Slack bot successfully posted the alert in the workspace, ensuring no high-value lead is missed.

🚀 Future Enhancements
Swap the manual trigger for a live Webhook to process real website form submissions.
Add a Google Sheets node to log all leads, even those that don't meet the "High Priority" threshold.

# AI-Powered Task Automation with QC Dashboard

Set-and-forget workflow for operational efficiency: Parses Gmail tasks to Clockify, uses Gemini AI to flag anomalies (e.g., missing due date, unassigned High Pri, confidential risks), sends alerts, and logs to Sheets for insights.

Key Wins (From 6 Test Scenarios):
- 5/6 anomalies flagged (83% detection; e.g., "High Priority without assignee").
- Time saved: 50 min/week (10 min/fix x 5 flags).
- Uptime: 100% in tests; scalable to 100 tasks/month on free tiers.

## Demo Flow
1. Email Task: Urgent Fix\nPriority: High (no assignee) → Zap triggers.
2. Parses Title/Priority/Assignee → Clockify entry.
3. Gemini QC: Flags "High Priority without assignee" → Alert + Log.
4. Insights: Efficiency drops to 76%, Saved=10 min.

Live Links:
- Zap: [Public View](https://zapier.com/share/your-zap-id) – Toggle public in Zap settings.
- Dashboard: [Sheets Table](your-share-link) – Shows 5 flags, 76% efficiency.


### Metrics Table
|       Metric        |      Test Result     |       Tool       |
|---------------------|----------------------|------------------|
| Error Catch         | 83% (5/6 scenarios)  | Gemini QC        |
| Time Saved          | 50 min (5 flags)     | Sheets Calc      |
| Utilization         | 0-5% (parse pending) | Clockify Logs    |
| Unassigned High Pri | 3 (from logs)        | COUNTIFS Formula |

## Tech Stack
- Automation: Zapier (triggers/parse).
- Tracking: Clockify (time entries).
- QC: Gemini AI (anomaly JSON).
- Insights: Google Sheets (formulas/table).

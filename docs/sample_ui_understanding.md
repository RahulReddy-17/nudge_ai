# Nudge.ai — Feature UX Design and Sample UI

> UX guide for the 12 core functionalities, including low-fidelity wireframes. All sample values are illustrative.

## Product UX Vision

Nudge.ai should guide users from noticing a business change to understanding it, exploring predictions, and deciding what to investigate next.

**Core journey:** Overview → Analytics → Diagnosis → Predictions → AI Assistant → Business decision.

## Application Navigation

Recommended navigation: Overview, Analytics, Diagnosis, Predictions, AI Insights, AI Assistant, Data Management, and Administration. Keep the global date filter, data freshness indicator, notifications, and user profile in the top bar.

```text
┌────────────────────────────────────────────────────────────────────────────┐
│ Nudge.ai                          Demo data | Updated 10:42 | Notifications │
├──────────────────┬─────────────────────────────────────────────────────────┤
│ Overview         │ Business Overview        Date: [Last 30 days ▼]         │
│ Analytics        │                                                         │
│ Diagnosis        │ [ Revenue ] [ Orders ] [ Avg Order Value ] [ Customers ]│
│ Predictions      │                                                         │
│ AI Insights      │ [ Revenue trend chart                       ]           │
│ AI Assistant     │ [ Top products chart       ] [ Needs attention ]        │
│ Data Management  │                                                         │
│ Administration   │ [ Ask Nudge.ai _____________________________ ] [Ask]    │
└──────────────────┴─────────────────────────────────────────────────────────┘
```

## Feature-by-Feature UX Design

### 1. Business Dashboard

- **User goal:** Understand business performance quickly.
- **UI design:** KPI cards for revenue, orders, average order value and customers; revenue trend; product rankings; global date filter; 'Needs attention' section.
- **Interactions:** Click KPIs or chart elements to drill down. Global filters update all relevant views.
- **UX principle:** A user should understand the business state in seconds.

### 2. Real-Time Analytics

- **User goal:** See relevant changes as events are processed.
- **UI design:** Live/Paused/Data delayed indicator, last processed event timestamp, updating KPIs and recent-event feed.
- **Interactions:** Open event details; pause/resume replay where supported; explain delays.
- **UX principle:** Never present replayed historical events as live production data.

### 3. Sales Analysis

- **User goal:** Discover which products, regions and periods drive sales.
- **UI design:** Date and dimension filters, revenue trend, product rankings, sortable table and drill-down links.
- **Interactions:** Click a product or chart bar to inspect contributing records; show active filters and Reset.
- **UX principle:** Preserve context when moving from summary to detail.

### 4. Business Diagnosis

- **User goal:** Understand factors contributing to a business change.
- **UI design:** Detected issue, comparison period, ranked factors, evidence metrics and suggested next checks.
- **Interactions:** Open factor breakdowns and supporting records.
- **UX principle:** Show evidence first; distinguish measured contributions from hypotheses.

### 5. Sales Forecasting

- **User goal:** Understand expected sales and plan ahead.
- **UI design:** Actual-versus-forecast chart, 7/30-day horizon selector, uncertainty interval if supported, model metrics and last training date.
- **Interactions:** Change horizon and compare later forecasts with actuals.
- **UX principle:** Label predictions as estimates, not guarantees.

### 6. Customer Segmentation

- **User goal:** Understand groups of customers with similar purchasing behavior.
- **UI design:** Segment cards, customer counts, average spend, purchase frequency and distribution chart.
- **Interactions:** Open a segment to inspect customers and defining characteristics.
- **UX principle:** Use business-friendly labels only when supported by data.

### 7. Anomaly Detection

- **User goal:** Find unusual activity that deserves review.
- **UI design:** Flagged-record table, anomaly score, transaction details, relevant features and review status.
- **Interactions:** Filter, inspect records, mark reviewed or needing investigation.
- **UX principle:** An anomaly is not proof of fraud.

### 8. AI Business Assistant

- **User goal:** Ask business questions without navigating every report.
- **UI design:** Chat interface, suggested prompts, concise answers, supporting metrics and chart links.
- **Interactions:** Ask follow-ups and open the supporting analysis.
- **UX principle:** Numerical answers must come from verified analytics.

### 9. AI-Generated Insights

- **User goal:** Discover important findings without examining every chart.
- **UI design:** Prioritized cards grouped into trends, risks and opportunities; each includes metric, period and evidence link.
- **Interactions:** Open evidence or dismiss irrelevant insights.
- **UX principle:** Avoid generic or repetitive AI text.

### 10. Alerts and Notifications

- **User goal:** Know which changes need attention.
- **UI design:** Notification bell, alert center, severity, trigger details, timestamp and history.
- **Interactions:** Open diagnosis, acknowledge/resolve and filter alerts.
- **UX principle:** Keep alerts actionable and avoid notification overload.

### 11. Data Management

- **User goal:** Import data and understand whether it is ready for analysis.
- **UI design:** Guided upload, preview, validation errors, progress and dataset history.
- **Interactions:** Preview before import, inspect failed rows, and see which dataset powers each view.
- **UX principle:** Help users fix data issues before analysis.

### 12. User Management

- **User goal:** Manage access securely.
- **UI design:** Login, profile, user table, roles and permissions.
- **Interactions:** Authorized admins add/deactivate users and update roles.
- **UX principle:** Protect administrative actions and communicate access limits clearly.

## Sample UI Wireframes

### Overview Dashboard

```text
┌────────────────────────────────────────────────────────────────────────────┐
│ Nudge.ai                          Demo data | Updated 10:42 | Notifications │
├──────────────────┬─────────────────────────────────────────────────────────┤
│ Overview         │ Business Overview        Date: [Last 30 days ▼]         │
│ Analytics        │                                                         │
│ Diagnosis        │ [ Revenue ] [ Orders ] [ Avg Order Value ] [ Customers ]│
│ Predictions      │                                                         │
│ AI Insights      │ [ Revenue trend chart                       ]           │
│ AI Assistant     │ [ Top products chart       ] [ Needs attention ]        │
│ Data Management  │                                                         │
│ Administration   │ [ Ask Nudge.ai _____________________________ ] [Ask]    │
└──────────────────┴─────────────────────────────────────────────────────────┘
```

### Diagnosis Panel

```text
┌───────────────────────────────────────────────────────────────┐
│ Business Diagnosis    This week vs Previous week              │
├───────────────────────────────────────────────────────────────┤
│ REVENUE CHANGE: -18%  (illustrative example)                   │
│                                                               │
│ Measured factors                                              │
│ 1. Order volume         -12%     [View order trend]            │
│ 2. Average order value   -7%     [View basket analysis]        │
│ 3. Product category A    Largest measured contribution        │
│                                                               │
│ AI summary: Revenue declined alongside lower order volume and  │
│ weaker sales in selected categories. The underlying cause is   │
│ not established by these metrics alone.                        │
│                                                               │
│ [Open product breakdown] [Ask AI about this finding]           │
└───────────────────────────────────────────────────────────────┘
```

### Sales Forecast

```text
┌───────────────────────────────────────────────────────────────┐
│ Sales Forecast                 Horizon: [Next 30 days ▼]       │
├───────────────────────────────────────────────────────────────┤
│ [ Historical actuals ───── Forecast ··············· ]          │
│                                                               │
│ Forecast summary: [Model-generated value]                      │
│ Expected range: [If supported by model]                        │
│ Evaluation: [MAE / RMSE / baseline comparison]                 │
│ Last trained: [timestamp]   Data through: [timestamp]          │
│                                                               │
│ Forecasts are estimates and may differ from actuals.           │
└───────────────────────────────────────────────────────────────┘
```

### AI Assistant

```text
┌───────────────────────────────────────────────────────────────┐
│ Ask Nudge.ai                                                   │
├───────────────────────────────────────────────────────────────┤
│ Suggested: [Top products] [Revenue change] [Sales forecast]    │
│                                                               │
│ You: Why did revenue decrease last week?                       │
│                                                               │
│ Nudge.ai: Revenue was lower in the selected period. The        │
│ measured changes and contributing categories are below.        │
│                                                               │
│ Evidence: [Order trend] [Product breakdown] [Date range]       │
│                                                               │
│ Ask a follow-up... [______________________________] [Send]     │
└───────────────────────────────────────────────────────────────┘
```

## Sample Diagnosis Experience

**Detected change:** Revenue down 18% vs previous week (illustrative).

**Measured evidence:** Order volume down 12%; average order value down 7% (illustrative).

**Next step:** Review product-level trends and validate whether inventory, pricing, or demand data is available. Do not claim an underlying cause unless the data supports it.

## UX Guidelines

- Label historical, synthetic, simulated-live, measured, predicted, and AI-generated information clearly.
- Show evidence for diagnoses and AI explanations.
- Do not present anomalies as proof of fraud or forecasts as guarantees.
- Use clear loading, error, and empty states.
- Make important actions accessible by keyboard and keep layouts responsive.

## Recommended Build Order

1. Overview dashboard and sales analytics.
2. Evidence-based diagnosis.
3. Sales forecasting.
4. Customer segmentation and anomaly review.
5. AI assistant grounded in analytics functions.
6. Simulated streaming and alerts.
7. Data management, permissions, testing, and deployment polish.

# Performance Monitoring Dashboard

This dashboard tracks and displays performance metrics (URL, Status Code, Duration, Timestamp) for every request in the e-commerce app.

## Features
- Logs every HTTP request.
- Displays performance data in a dashboard view.
- Helps identify slow or failing requests.
- Local-only, no external services needed.

---

## File Structure
- Models/PerformanceLog.cs: Model for log entry.
- Middleware/PerformanceLoggingMiddleware.cs: Middleware that writes logs.
- Controllers/DashboardController.cs: Reads logs and sends to view.
- Views/Dashboard/Index.cshtml: UI to display logs.
- Logs/performance.txt: Storage for log entries.

---

## Setup Instructions

### 1. Register Middleware
In Program.cs:
```csharp
app.UseMiddleware<PerformanceLoggingMiddleware>();
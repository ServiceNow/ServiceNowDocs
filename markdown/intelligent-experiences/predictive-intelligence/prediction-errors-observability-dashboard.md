---
title: Reviewing prediction errors with the Observability Dashboard
description: The Observability Dashboard offers a unified view and actionable insights for errors detected in Predictive Intelligence. Use this dashboard to visualize logged errors and gain information on prediction reliability and potential problem areas.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Testing and monitoring predictions, Predictive Intelligence, Enable AI experiences]
---

# Reviewing prediction errors with the Observability Dashboard

The Observability Dashboard offers a unified view and actionable insights for errors detected in Predictive Intelligence. Use this dashboard to visualize logged errors and gain information on prediction reliability and potential problem areas.

View the PI - Observability Dashboard by navigating to **Predictive Intelligence** &gt; **Observability** &gt; **Observability Dashboard**. The dashboard contains the following widgets.

-   Total Number of Prediction Errors
-   Prediction Errors Breakdown by Date
-   Prediction Errors Count by Capability
-   Prediction Error Count by Error Type
-   Error Types by Capability
-   Successful and Unsuccessful Predictions Breakdown by Date

You can drill down to the underlying records from the widget graphics. You can also change the date range of all widgets by selecting **Date** to open the selector.

![The Predictive Intelligence dashboard, showing four widgets: Total Number of Prediction Errors, Prediction Errors Breakdown by Date, Prediction Errors Count by Capability, Prediction Error Count by Error Type.](../images/prediction-errors-observability-dashboardZ1.png "PI Observability Dashboard — upper four widgets")

The PI - Observability Dashboard draws from a table dedicated to logging prediction errors: **ML Predictor Error Logs** \[ml\_predictor\_error\_logs\].

-   Fields in the table include Error Type, Error Message, Status code, Solution, and Capability.
-   View this table's records directly by navigating to **Predictive Intelligence** &gt; **Observability** &gt; **Prediction Error Logs**.
-   Roles required to access the table: ml\_report\_user or ml\_admin.

The table logs the following types of granular errors.

-   Client-side issues \(400 Series\) — captures request errors such as timeouts and invalid inputs.
-   Server-side issues \(500 Series\) — tracks internal server errors encountered during prediction.
-   Internal prediction failures — identifies instances when the model was unable to generate a prediction.
-   Low confidence predictions — records log results falling below a defined confidence threshold.

**Note:** Errors in training aren't included in this table.

![The lower section of the Predictive Intelligence Observability dashboard, showing two widgets: Error Types by Capability, Successful and Unsuccessful Predictions Breakdown by Date.](../images/prediction-errors-observability-dashboardZ2.png "PI Observability Dashboard — lower two widgets")


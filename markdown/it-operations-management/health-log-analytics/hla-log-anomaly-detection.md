---
title: Influence anomaly detection in Health Log Analytics with lexical keywords
description: Influence how Health Log Analytics finds anomalies by managing keywords it looks for in your log data. When text in log data for a source matches a lexical keyword that exceeds a specified count threshold, the system identifies an anomaly and generates an alert.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Influence anomaly detection in Health Log Analytics with lexical keywords

Influence how Health Log Analytics finds anomalies by managing keywords it looks for in your log data. When text in log data for a source matches a lexical keyword that exceeds a specified count threshold, the system identifies an anomaly and generates an alert.

Health Log Analytics scans your logs for words that can indicate important issues. Lexical keywords such as 'crashed' or 'failed' signal conditions that may require attention. The application sets a threshold for each lexical keyword based on its normal occurrence pattern and frequency in your logs.

When Health Log Analytics scans your logs, it identifies all occurrences of the keyword. If the frequency of a lexical keyword in the log data for a source exceeds the specified threshold, the system identifies an anomaly and generates an alert.

Health Log Analytics comes with many default global keywords. You can add, edit, and delete these global keywords or phrases, which apply to all source types.

**Note:** To add a specified keyword associated with a specific source type, see [Configure source type capabilities in Health Log Analytics](../task/hla-source-types.md).

You can manage lexical keywords as follows:

-   [Add, edit, or delete lexical keywords in Health Log Analytics](../task/hla-lexical-keywords-admin.md)

    Add, edit, and delete global keywords or phrases.

-   [View the lexical keywords that generate alerts in Health Log Analytics](../../health-log-analytics-operator/task/hla-op-lexical-keywords-manage.md)

    View the list of lexical keywords that can indicate important issues in log entries. By default, the table lists only global keywords.


-   **[Add, edit, or delete lexical keywords in Health Log Analytics](../task/hla-lexical-keywords-admin.md)**  
Manage the keywords that Health Log Analytics looks for in your log data.
-   **[View the lexical keywords that generate alerts in Health Log Analytics](../../health-log-analytics-operator/task/hla-op-lexical-keywords-manage.md)**  
View the list of lexical keywords that can indicate important issues in log entries.

**Parent Topic:**[ITOM AIOps](../../it-operations-management/reference/itom-health-landing-page.md)


---
title: Analyzing and resolving Log Analytics alerts
description: Analyze and resolve Log Analytics alerts by investigating log data and taking action to resolve the underlying issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/hla-analyzing-resolving-hla-alert.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Analyzing and resolving Log Analytics alerts

Analyze and resolve Log Analytics alerts by investigating log data and taking action to resolve the underlying issue.

## Overview of analyzing and resolving a Log Analytics alert

As an Operator, you are responsible for analyzing and resolving the alerts that Health Log Analytics generates. When HLA creates an alert, you review the alert's severity, the affected Configuration Item \(CI\), the log data associated with the anomaly, and the impacted services. You try to identify the root cause by investigating the logs that surround the anomaly.

In the Express List, review alert details and use Now Assist to get an in-depth analysis of the alert and potential resolutions in straightforward, human-readable language. By drilling down into the alert, you can quickly identify the issue and proceed to resolve it before it affects your users.

Using the Log Viewer, you can browse the alert logs by timestamp or range for further investigation. You can visualize the frequency of anomalous log lines in a chart.

-   [Start remediation of a Log Analytics alert from the Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-overview-tab-view.md)

    Begin the remediation process of a Log Analytics alert from the alert **Overview** tab. This tab provides information on the alert, log data associated with the anomalous behavior, CIs associated with the alert, and services impacted by it.

-   [Analyze the logs that surround the anomaly](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-surrounding-logs-view-concept.md)

    Review the log lines surrounding the anomaly for clues about the state of faulting systems. This information can help you narrow down the root cause of the alert.

-   [Use log correlators to identify relationships in log data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-correlator-what-is-a.md)

    Identify relationships between alerts to help you determine whether an alert is part of a larger issue.

-   Navigate to the [Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/express-list.md) and select an alert from the Alerts list.

    Use [Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/alert-summary-now-assist-express-list.md) to get an in-depth analysis of the alert and potential resolutions. By drilling down into the alert, you can quickly identify the issue and proceed to resolve it.

-   [Review the logs for an alert on the Log viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-logs-log-viewer-concept.md)

    For further investigation you can navigate to the **Log Viewer** to browse the alert logs by timestamp or time range, and visualize anomaly frequency within a time period for a comprehensive view of log data over a specified time range.

-   [Add a KB article to a Log Analytics alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-alert-add-kb.md)

    When you have resolved an alert that Health Log Analytics generated, you can add a knowledge base \(KB\) article to it. For example, provide information that might help others resolve similar issues.


## Use cases

[Use Case: Proactive monitoring of your ServiceNow instance in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-use-case-syslogs.md) - Use Health Log Analytics to detect and resolve emerging issues in your organization's ServiceNow instance before they affect platform users.


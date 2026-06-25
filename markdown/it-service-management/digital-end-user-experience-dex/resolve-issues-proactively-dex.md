---
title: Resolve issues proactively with DEX Proactive Resolution
description: Use ServiceNow, Inc. Digital End-User Experience \(DEX\) to detect and resolve device and application issues before users report them, reducing disruptions and improving the end-user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/resolve-issues-proactively-dex.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 2
breadcrumb: [Digital End-User Experience, IT Service Management]
---

# Resolve issues proactively with DEX Proactive Resolution

Use ServiceNow, Inc. Digital End-User Experience \(DEX\) to detect and resolve device and application issues before users report them, reducing disruptions and improving the end-user experience.

DEX supports two proactive resolution strategies depending on how quickly an issue must be addressed:

-   [Real-time proactive resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/proactive-resolution-real-time.md)

    Detect and remediate device and application issues within minutes using metric rules, alerts, and automated or manual remediation actions. Use this approach for time-sensitive issues such as device crashes, disk usage thresholds, or application crashes.

-   [Non-real-time proactive resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/proactive-resolution-non-real-time.md)

    Detect and remediate issues that require periodic review of aggregated or configuration data. Use this approach for issues such as system compliance, battery health, system performance, and DEX Score trends.


## Detection and remediation methods

Each proactive resolution strategy uses different detection and remediation methods. The following table summarizes the options available in each strategy.

|Strategy|Detection|Remediation|
|--------|---------|-----------|
|Real-time \(metric-based\)|Metric rules that generate alerts when a threshold is breached|Automated actions defined in the metric rule, or manual bulk actions from the alert|
|Real-time \(auto-correction scripts\)|Check definitions wrapped in policies, run at a defined frequency|Scripts that detect and correct conditions automatically, including when the device is offline|
|Non-real-time|Reports, dashboards, and scheduled jobs that query aggregated data tables|Custom flows, scheduled jobs, or bulk actions from insight reports|

## Other DEX resolution methods

Proactive resolution is one of several ways DEX helps resolve device and application issues. Depending on the role and the workflow, you can also use the following methods, many of which work together with the real-time and non-real-time strategies.

-   **Custom insights reports and bulk remediation**

    Identify a population of devices that meet a condition and remediate them as a group. See [Create an insights report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/create-insights-report.md), [Trigger bulk remediation from Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/trigger-bulk-remediation-insights.md), and [DEX remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-remedial-actions.md) for more details.

-   **Metric Analyzer**

    Investigate device and application metrics interactively when no metric rule has been authored yet. See [View collected metrics with Metrics analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/view-dex-metrics.md) and [DEX remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-remedial-actions.md) for more details.



---
title: Non-real-time proactive resolution
description: Use reports, dashboards, and scheduled jobs to periodically detect and remediate device issues that require aggregated or configuration data, such as system compliance, battery health, and DEX Score trends.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/proactive-resolution-non-real-time.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 1
breadcrumb: [Resolve, Digital End-User Experience, IT Service Management]
---

# Non-real-time proactive resolution

Use reports, dashboards, and scheduled jobs to periodically detect and remediate device issues that require aggregated or configuration data, such as system compliance, battery health, and DEX Score trends.

Non-real-time proactive resolution addresses issues that don't require immediate action and that are best identified by reviewing aggregated data or device configuration data on a periodic basis. Examples include system compliance violations, degraded battery health, overall system performance trends, and DEX Score changes.

## Detection methods

DEX provides in-product reports and dashboards for manual detection, and supports customer-created scheduled jobs for automated detection against aggregated data tables.

-   **Manual detection**

    Use in-product reports and dashboards to identify devices or users that meet a condition of interest. Review insight reports for battery health, system compliance, and similar metrics on a schedule that fits your organization's operational cadence.

-   **Automated detection**

    Create scheduled jobs that query aggregated data tables, such as DEX Score tables or insight report tables for battery health and system compliance. When the scheduled job identifies devices that meet a condition, it can trigger a remediation action automatically.


**Note:** DEX ships a scheduled job for battery replacement requests as demonstration data. You can use this as a reference when creating your own scheduled jobs.

## Remediation methods

-   **Manual remediation**

    After identifying affected devices through reports or dashboards, trigger bulk remediation directly from an insights report to remediate multiple devices in a single action. You can also use customer-created custom flows for cases that require additional logic beyond a single remedial action. For the bulk remediation procedure, see [Trigger bulk remediation from Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/trigger-bulk-remediation-insights.md).

-   **Automated remediation**

    Configure scheduled jobs to both detect and remediate issues. The scheduled job evaluates a condition in an aggregated data table and executes a remediation action for all matching devices.



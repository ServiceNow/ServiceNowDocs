---
title: Instance scan checks
description: Instance scan checks in Service Exchange proactively identify issues and system inconsistencies, helping administrators maintain system health and reduce downtime. The health dashboard displays findings, errors, and check statuses, helping you quickly identify and resolve problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/service-bridge-v2-scan-checks.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [instance scan checks, health dashboard, system health, scan suites]
breadcrumb: [Service Exchange Center, Explore, Service Exchange]
---

# Instance scan checks

Instance scan checks in Service Exchange proactively identify issues and system inconsistencies, helping administrators maintain system health and reduce downtime. The health dashboard displays findings, errors, and check statuses, helping you quickly identify and resolve problems.

Service Exchange scan checks provide the following benefits:

-   Reduce case task loads and promote stability and reliability of Service Exchange integrations.
-   Reduce downtime and troubleshooting efforts by identifying issues early.
-   Provide known errors with detailed solutions.
-   Improve overall productivity through automation and visibility.

## Supported Service Exchange scan checks

Service Exchange provides two main suites, on-demand and scheduled.

Each suite contains multiple child suites and each child suite contains multiple scan checks. For more information on suite and scan checks, see [Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/hs-landing-page.md).

-   On-demand suites: On-demand checks can be run as and when required.
-   Scheduled suites: Scheduled checks run at a scheduled time every day.

You can also customize when scheduled suites run or assign a scheduled execution time to on-demand suites.

To view the list of Service Exchange supported scan checks, see [List of scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-list-of-scan-checks-in-sb.md).

These Service Exchange scan checks are available through the Service Exchange Health plugin. This plugin is activated when you install or upgrade Service Exchange. You can also activate this plugin manually. For activation instruction, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateAPlugin.md).

**Note:** The Service Exchange Health plugin is backward compatible. If you're using an older version of the Service Exchange application, you can install this plugin to use its features.

**Related topics**  


[List of scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-list-of-scan-checks-in-sb.md)

[Execute a scan suite as a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-execute-scan-check.md)

[Execute a scan suite as a consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-con-execute-scan-check.md)

[Modify the scan suite schedule as a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-execute-scan-check.md)

[se-scan-check-details]

[Manage a scan check as a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-execute-scan-check.md)


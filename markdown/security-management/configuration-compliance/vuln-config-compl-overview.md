---
title: Configuration Compliance reporting
description: The Configuration Compliance homepage provides an executive view into policies, CIs, tests, and test results, helping security staff pinpoint areas of concern quickly. Configuration Compliance significance charts can be added, as needed. You can also return Configuration Compliance -related information using the global search feature.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analytics and Reporting, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance reporting

The Configuration Compliance homepage provides an executive view into policies, CIs, tests, and test results, helping security staff pinpoint areas of concern quickly. Configuration Compliance significance charts can be added, as needed. You can also return Configuration Compliance -related information using the global search feature.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

In each chart, you can point to any part of a chart \(bar, pie, data point\) to view general data specific to that part of the chart. If you click any part of a report, a list opens to provide detailed information.

**Note:**

-   Dashboards on the Configuration Compliance homepage are available only when the Performance Analytics for Configuration Compliance application is activated. For steps to activate this application, see [Activate Performance Analytics for Configuration Compliance](../../../use/application-content-packs/concept/configuration-compliance-install.md).
-   Anyone with the sn\_vulc.read role can view the dashboard. Anyone in the sn\_vulc.write or sn\_vulc.admin role can create and edit a dashboard. Only sn\_vulc.admin can delete a dashboard.



![v10.3 Configuration Compliance report - top](../image/v11ccdashboard-2.png)

![v10.3 Configuration Compliance report - Bottom](../image/v11ccdashboard-1.png "Configuration Compliance report")

|Name|Visual|Description|
|----|------|-----------|
|Test Results by Compliance|Donut|Displays the number of open tests that have passed or failed.|
|Polices|Number|Number of policies with failed test results.|
|Tests|Number|Number of tests with failed test results.|
|Hosts|Number|Number of hosts with failed test results.|
|Test Results|Number|Displays the number of test results.|
|Failed Test Results by Risk Rating|Donut|Displays the number of failed tests by risk rating.|
|Failed Test Results by Technology|Donut|Displays models with failed tests.|
|Failed Test Results by Category|Bar|Displays categories with the most failed test results.|
|Open Test Result by Risk Rating|Bar|Displays the number of open test results by risk rating.|
|Remediation Tasks|Chart|Displays remediation tasks by state and risk rating.|


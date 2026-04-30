---
title: Instance scan checks and health dashboard
description: Instance scan checks in Service Exchange proactively identify issues and system inconsistencies, helping administrators maintain system health and reduce downtime. The health dashboard displays findings, errors, and check statuses, helping you quickly identify and resolve problems.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Service Exchange]
---

# Instance scan checks and health dashboard

Instance scan checks in Service Exchange proactively identify issues and system inconsistencies, helping administrators maintain system health and reduce downtime. The health dashboard displays findings, errors, and check statuses, helping you quickly identify and resolve problems.

Service Exchange scan checks provide the following benefits:

-   Reduce case task loads and promote stability and reliability of Service Exchange integrations.
-   Reduce downtime and troubleshooting efforts by identifying issues early.
-   Provide known errors with detailed solutions.
-   Improve overall productivity through automation and visibility.

## Supported Service Exchange scan checks

Service Exchange provides two main suites, on-demand and scheduled.

Each suite contains multiple child suites and each child suite contains multiple scan checks. For more information on suite and scan checks, see [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   On-demand suites: On-demand checks can be run as and when required.
-   Scheduled suites: Scheduled checks run at a scheduled time every day.

You can also customize when scheduled suites run or assign a scheduled execution time to on-demand suites.

To view the list of Service Exchange supported scan checks, see [List of scan checks](../reference/service-bridge-v2-list-of-scan-checks-in-sb.md).

These Service Exchange scan checks are available through the Service Exchange Health plugin. This plugin is activated when you install or upgrade Service Exchange. You can also activate this plugin manually. For activation instruction, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** The Service Exchange Health plugin is backward compatible. If you're using an older version of the Service Exchange application, you can install this plugin to use its features.

## Health Dashboard

The Service Exchange Health Dashboard consolidates findings, errors, and scan task statuses into a single view. You can select any widget to view information about the scan checks.

Each scan task includes a work note that contains a link to relevant known error documentation. This documentation provides step-by-step guidance that may help you resolve the problem.

You can access the Health Dashboard from the Service Exchange **Administration** menu.

**Related topics**  


[List of scan checks](../reference/service-bridge-v2-list-of-scan-checks-in-sb.md)


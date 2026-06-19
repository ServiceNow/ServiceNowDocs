---
title: Automatic dashboard setup in CMDB success advisor
description: CMDB success advisor can automatically configure the Data Foundations advisor dashboard on installation or upgrade, giving you immediate access to pre-configured CMDB health insights without manual setup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-auto-setup.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 2
breadcrumb: [Get started with dashboard setup, Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Automatic dashboard setup in CMDB success advisor

CMDB success advisor can automatically configure the Data Foundations advisor dashboard on installation or upgrade, giving you immediate access to pre-configured CMDB health insights without manual setup.

## Auto-setup process

When you install or upgrade CMDB success advisor, the **CMDB Advisor - Auto Setup** on-demand scheduled job can automatically configure the Data Foundations advisor dashboard. The job checks eligibility conditions, applies the recommended principal class scope, creates the dashboard configuration, and triggers initial data collection.

After data collection completes, as a user with the sn\_cmdb\_admin role, you receive a notification with a link to the configured dashboard. You can review and modify the auto-selected scope at any time using the standard scope management options.

The dashboard card on the CMDB success advisor landing page displays a badge with the number of principal classes that auto-setup selected.

## Eligibility conditions

Auto-setup runs only when all of the following conditions are met. If any condition is not met, you can configure the Data Foundations advisor dashboard manually.

-   The instance has no existing Data Foundations dashboard.
-   The total number of CIs on the instance is fewer than 65 million.
-   No more than 200 principal classes are already marked on the instance.

## Scope selected by auto-setup

The following logic applies when auto-setup sets the principal class scope:

-   If no principal classes exist, the top five recommended classes form the scope. Rankings reflect recent incident, problem, and change \(IPC\) activity. For more information, see [CI class recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-recom.md).
-   If one to four principal classes already exist, those classes remain in scope and additional recommendations fill the scope to a total of five.
-   If five to 200 principal classes already exist, all existing classes form the scope.

## Data collection and notifications after auto-setup

After auto-setup completes, data collection begins automatically. Data collection starts at a monthly frequency and switches to a daily frequency the first time you interact with the dashboard.

The **CMDB Advisor - Check Job Completion and Notify** scheduled job checks whether data collection has completed. When collection completes, the job sends a notification to users with the sn\_cmdb\_admin role through two channels: a record in the CMDB success advisor notification table with a direct link to the configured dashboard, and a notification in the ServiceNow platform notification center \(bell icon\). The job deactivates itself after it sends all product notifications.

When you first open the advisor after auto-setup completes, a toast notification appears with a readiness confirmation and a summary of the auto-selected scope.

## Reviewing and modifying the auto-setup scope

You can review and update the scope selected by auto-setup at any time using the standard scope management options on the dashboard.

To modify the Data Foundations scope, see [Manage Data Foundations advisor scope in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-optimize-dashboard.md).


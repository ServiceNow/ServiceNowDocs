---
title: Automatic dashboard setup for Data Foundations in CMDB success advisor
description: CMDB success advisor can automatically configure the Data Foundations advisor dashboard on installation or upgrade, giving you immediate access to pre-configured CMDB health insights without manual setup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-auto-setup.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 2
keywords: [auto-setup, automatic dashboard setup, Data Foundations advisor dashboard, principal classes]
breadcrumb: [Get started with dashboard setup, Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Automatic dashboard setup for Data Foundations in CMDB success advisor

CMDB success advisor can automatically configure the Data Foundations advisor dashboard on installation or upgrade, giving you immediate access to pre-configured CMDB health insights without manual setup.

## Auto-setup process

When you install or upgrade CMDB success advisor, the **CMDB Advisor - Auto Setup** on-demand scheduled job configures the Data Foundations advisor dashboard automatically. The job checks eligibility conditions, applies the recommended principal class scope, creates the Data Foundations content template, and triggers initial data collection.

After data collection completes, users with the sn\_cmdb\_admin role receive a notification with a link to the configured dashboard.

The dashboard card on the CMDB success advisor landing page displays a badge with the number of principal classes that auto-setup selected.

## Eligibility conditions

Auto-setup runs only when all the following conditions are met. If any condition is not met, you can configure the Data Foundations advisor dashboard manually.

-   The instance has no existing Data Foundations dashboard.
-   The total number of CIs on the instance is fewer than 65 million.
-   No more than 200 principal classes are already marked on the instance.

## Scope selected by auto-setup

The following logic applies when auto-setup selects the principal class scope:

-   If no principal classes exist, the top five recommended classes form the scope. Rankings reflect recent incident, problem, and change \(IPC\) activity. For more information, see [CI class recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-recom.md).
-   If one to four principal classes already exist, those classes remain in scope and additional recommendations fill the scope to a total of five.
-   If five to 200 principal classes already exist, all existing classes form the scope.

## Data collection and notifications after auto-setup

After auto-setup completes, data collection begins automatically. Data collection runs monthly and changes to daily after you open the dashboard for the first time.

The **CMDB Advisor - Check Job Completion and Notify** scheduled job checks whether data collection has completed. When collection completes, the job sends a notification to users with the sn\_cmdb\_admin role that includes a link to the configured dashboard. After all notifications are sent, the job is deactivated.

When you first open the Data Foundations advisor after auto-setup completes, a notification indicates that the advisor is ready and shows the number of principal classes automatically selected based on incident, problem, and change \(IPC\) activity.

## Reviewing and modifying the auto-setup scope

You can review and update the model categories selected by auto-setup at any time.

To modify the Data Foundations scope, see [Manage Data Foundations advisor scope in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-optimize-dashboard.md).


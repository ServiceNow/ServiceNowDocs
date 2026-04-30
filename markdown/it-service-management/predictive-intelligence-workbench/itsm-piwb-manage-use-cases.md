---
title: Manage ITSM Predictive Intelligence Workbench use cases
description: View your ITSM Predictive Intelligence Workbench use cases to monitor model performance and reevaluate the associated models, if necessary. You can also continue setup of models you started, but did not complete.
locale: en-US
release: yokohama
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Manage ITSM Predictive Intelligence Workbench use cases

View your ITSM Predictive Intelligence Workbench use cases to monitor model performance and reevaluate the associated models, if necessary. You can also continue setup of models you started, but did not complete.

## Before you begin

Role required: piwb\_admin or piwb\_manager

## About this task

**Important:**

Starting with the yokohama release, the ITSM Predictive Intelligence Workbench will reach its end of life \(EOL\) as part of its deprecation process. It will be completely deprecated and no longer deployed, enhanced, or supported from the yokohama release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Via the Models detail page you can access the **Test** tab to perform the following actions:

-   Perform single or batch tests on model versions.
-   Export version test results as `.csv` files and mark versions as active.
-   Filter the number of versions based on date range.
-   Monitor testing progress with notifications via the guided process.

## Procedure

1.  Navigate to **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **All**.

    The **Use Cases - All** page opens displaying all use cases. The status of the use case is depicted on the card, for example, **In progress**. Other statuses include, **Completed** and **Monitoring**.

    ![Predictive Intelligence Workbench All Use Cases.](../image/piwb-all-use-cases.png)

2.  Click a use case to continue with implementation.

    Or you can evaluate performance if the use case is in the **Monitoring** state.

    **Note:** If a use case is under performing, the net automation is lower than the threshold configured in the Settings page. See [Configure ITSM Predictive Intelligence Workbench settings](itsm-piwb-config-settings.md).



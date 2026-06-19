---
title: Set up the Data Foundations advisor dashboard manually
description: If the Data Foundations advisor dashboard was not configured automatically, set it up manually by selecting the principal classes that define the Data Foundations scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-manual-setup.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Get started with dashboard setup, Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set up the Data Foundations advisor dashboard manually

If the Data Foundations advisor dashboard was not configured automatically, set it up manually by selecting the principal classes that define the Data Foundations scope.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  On the CMDB success advisor landing page, select **Set principal classes**.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-landing-page.md).

2.  On the Set principal classes dialog box, select a group to choose all its classes or expand a group to select individual classes, then move them from the **Available classes** column to the **Selected classes** column.

    Any CI classes added to an application-specific advisor dashboard such as for Hardware Asset Management \(HAM\) are automatically monitored as principal classes.

    The number of principal classes you can select is set in the CMDB Advisor Content Template \[sn\_cmdb\_advisor\_content\_template\] table. The default configuration enables you to select up to 200 principal classes. For more information, see [Components installed with CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-components-installed.md).

    **Tip:** The **Recommended** group, shown at the top of the Group list, includes CI classes based on the recent incident, problem, and change \(IPC\) activity, ranked by task volume. You can start with these recommended principal classes to improve foundational CMDB data and maximize operational value. To learn more, see [CI class recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-recom.md).

3.  To remove a CI class, select X icon next to the class in the **Selected classes** column.

4.  Select **Done** to build the CMDB success advisor for Data Foundations dashboard.


## Result

The selected classes are marked as principal classes and data collection begins. The Data Foundations advisor dashboard is populated after data collection completes. Initial data collection runs monthly. The frequency increases to daily after the first time you interact with the dashboard.

To update the scope after initial setup, select **Manage principal classes** on the Data Foundations advisor dashboard.


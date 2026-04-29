---
title: Get started with Data Foundations advisor dashboard setup
description: Set up your Data Foundations advisor dashboard by selecting principal classes to define the Data Foundations scope in CMDB success advisor.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up advisor, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Get started with Data Foundations advisor dashboard setup

Set up your Data Foundations advisor dashboard by selecting principal classes to define the Data Foundations scope in CMDB success advisor.

## Before you begin

Role required: sn\_cmdb\_admin

**Note:** In addition to the sn\_cmdb\_admin role, the pa\_data\_collector role is required to view the last updated data timestamp on the dashboard and pa\_viewer is required to filter data by principal classes.

## About this task

The Data Foundations scope defines which principal classes CMDB success advisor monitors. When a CI class is included in the Data Foundations advisor dashboard scope, the class is automatically marked as a principal class, which means it appears in CI selection filters on incident, change, and problem forms.

For guidance on choosing the right classes, see the [Guidance on designating principal classes in the CMDB \[KB2707240\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2707240) article in the Now Support Knowledge Base.

## Procedure

1.  On the CMDB success advisor landing page, select **Select principal classes**.

    See [Viewing the CMDB success advisor landing page](../concept/cmdb-sa-landing-page.md).

2.  On the Select principal classes dialog box, select a group to choose all its classes or expand a group to select individual classes, then move them from the **Available classes** column to the **Selected classes** column.

    Any CI classes added to an application-specific advisor dashboard such as for Hardware Asset Management \(HAM\) are automatically monitored as principal classes. You can select up to 50 classes.

    **Tip:** The **Recommended** group, shown at the top of the Group list, includes CI classes based on the recent incident, problem, and change \(IPC\) activity, ranked by task volume. You can start with these recommended principal classes to improve foundational CMDB data and maximize operational value. To learn more, see [CI class recommendations](../concept/cmdb-sa-df-class-recom.md).

3.  To remove a CI class, select the X icon next to the class in the **Selected classes** column.

4.  Select **Done** to build the CMDB success advisor for Data Foundations dashboard.


## Result

The selected classes are marked as principal classes and data collection begins. The Data Foundations advisor dashboard is populated after data collection completes.


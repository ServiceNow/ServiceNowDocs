---
title: Create a Process Mining project for a KPI group
description: Create Process Mining projects for each KPI group and its assignment groups. One project is created per KPI group per table.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Identifying bottlenecks using Process Mining integration with Workforce Optimization for ITSM, Integrating Process Mining with Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Create a Process Mining project for a KPI group

Create Process Mining projects for each KPI group and its assignment groups. One project is created per KPI group per table.

## Before you begin

Your administrator:

-   Must have created templates on tables that you want to create the process projects for. For information on creating templates, see [Create Process Mining templates](create-template-po-wfo-itsm.md).
-   Must run the **Process Mining - WFO Remine Projects** on-demand scheduled job when additional data is added to the projects so that you get the up-to-date process insights into your projects. The job is run on all projects that meet set criteria such as the frequency to remine that is set using the **promin.wfo.run\_frequency** system property. Also, the scheduled job updates the project and remine when there are any changes to the assignment groups.

    For more information, see [Workforce Optimization for ITSM integration with Process Mining](../reference/configurable-wfo-itsm-process-optimization.md).


Role required: sn\_process\_optimization\_analyst

The KPI assignment group manager must have this role to create process projects for their KPI groups.

## About this task

After you mine the project, the Project Definition for Process Minings \(sn\_team\_perf\_promin\_project\_groups\) project mapping table holds the reference for Workforce Optimization. Each project in the table has a unique source associated with each application. For example, the **Source** field in the table shows the assignment group associated with the Workforce Optimization project. The **Source** field is an identifier for the specific applications. The table also shows the KPI group associated with the project that you've mined.

## Procedure

1.  Mine the project to create process mining projects for each KPI group.

    1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Team Performance** &gt; **KPI Groups**.

    2.  Select a KPI group.

    3.  Select **Initiate Process Mining**.

        The process mining is run on active assignment groups. The project mining process is run on all leaf node automated or formula indicators in the KPI group.

        A corresponding project is created in the **All** &gt; **Workforce Optimization for ITSM** &gt; **Team Performance** &gt; **WFO Projects** module. When the mining is complete, the **Mining state** field changes to **Available**.

        A user with the role, sn\_wfo\_cfg\_itsm.manager, has a access to create or view the project, and can view the process insights and variation analysis in the **Process analysis** tab.

        **Note:**

        -   If a project process has been mined for a specific table in an assignment group, the projects are created for those assignment groups. Therefore, you can’t mine the table in that assignment group again.
        -   If you’re using a formula indicator for process mining, you can select any indicator source that is used in the formula.
2.  If you add additional assignment groups to the KPI group after you do process mining, you must remine the group again.

    1.  In the Assignment Group related list for the selected KPI group, select **Edit**.

    2.  Add the desired assignment group to the KPI group.

    A process is automatically created for the assignment group. If you add an assignment group to the KPI group, the assignment group will be updated in the filter condition, and if you remove any assignment group, it will be removed from the project filter condition. An informational message is displayed when an assignment group is added to the KPI group only if the KPI group is already mined.

    All the assignment groups associated with the KPI group for which you’ve created the project are updated in the filter condition of the table configuration.

    For more information on mining data, see [Generate a model](https://www.servicenow.com/docs/access?context=generate-process-map&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

    After any previous versions of Team Performance are upgraded to the latest version \(Team Performance App Version: 7.0.1\), all the previous projects will be removed for KPI groups that had multiple projects for assignment groups and new projects will be created for each of them.


**Parent Topic:**[Identifying bottlenecks using Process Mining integration with Workforce Optimization for ITSM](../concept/use-process-optimization-wfo-itsm.md)


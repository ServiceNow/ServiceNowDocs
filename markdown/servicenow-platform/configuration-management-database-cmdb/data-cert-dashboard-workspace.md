---
title: Data Certification Dashboard
description: Use the Data Certification Dashboard in CMDB Workspace as a central location to manage Data Certification instances and tasks, and to see counts, progress, state, and analytical insights. You can drill down past due certification tasks to examine and to reassign them, for example, so that they can be completed by an appropriate user.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-07"
reading_time_minutes: 3
breadcrumb: [Data Certification experience in CMDB Workspace, Data Certification, CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data Certification Dashboard

Use the Data Certification Dashboard in CMDB Workspace as a central location to manage Data Certification instances and tasks, and to see counts, progress, state, and analytical insights. You can drill down past due certification tasks to examine and to reassign them, for example, so that they can be completed by an appropriate user.

![Data Certification Dashboard.](../image/cmdb-data-certif-dashboard.jpg)

The Data Certification Dashboard gets populated by Data Certification execution records. For information about the archive rules that control the retention of those records, see 'Retention of Data Certification records' in [Data Certification experience in CMDB Workspace](data-cert-exp-cmdb-workspace.md).

## Role requirements

The user role determines which certification tasks are included in the dashboard, as follows:

-   data\_manager\_user: Minimum role required for access. Provides access to those certification tasks that are assigned to the user, to an assignment group that the user is a member of, or if the user is the manager of the assigned user or of the assignment group.
-   data\_manager\_admin: Provides access to all certification tasks.

## Reviewing certification tasks

The Data Certification Dashboard provides several ways for you to drill down to the certification tasks list, which can contain tasks requiring review. For information about reviewing \(and then certifying or failing\), reassigning, or canceling tasks, see [Review certification tasks in CMDB Workspace](../task/data-certific-review-tasks.md).

## Certification instances

The Certification instances tab shows counts and other details for certification instances. A certification instance is the collection of certification tasks for a policy execution identified by its unique policy execution number. For each certification instance, the dashboard shows progress indicators such as the overall percent complete, and a general state such as Not Started and Past Due. Each card shows the total number of associated tasks, and within that total, the number of tasks in a complete, open, and unassigned state.

You can:

-   Switch the type of view by selecting the List or the Cards icon.
-   Filter the list of certification instances that appear, by selecting the available filters such as State, Assignment group, or Assigned to filter and then selecting the specific items that you want to filter by.
-   Filter the list of certification instances that appear by searching for specific strings in certification policy names.
-   Sort the list of certification instances by various attributes such as instance state, percent complete, or policy execution number. Select ascending or descending sort order to apply along with any list filter.
-   Select the info icon next to a certification instance name, to show its respective policy execution number. For information about policy execution numbers, see table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] in [Components related to CMDB Data Manager](../reference/components-cmdb-data-manager.md).

Select a card to see more details about the certification instance, and all the tasks in that instance based on your user role. In the Certification tasks tab you can drill down the certification tasks list to access the tasks themselves for processing.

Select the Certification records tab to see all the certification records associated with all of the certification tasks in the certification instance. You can filter the certification records by **Certified** or **Failed** to show those records with at least one attribute in the selected state.

## Workload and Aging tasks

The Workload and Aging tasks tab contains two tabs showing the distribution of certification tasks workload and past-due tasks.

-   **Workload**

    Shows the distribution of work related to certification tasks, by user groups and by individual users. Select the Groups or the Individuals tab to see the distribution by percentage and by total number of tasks. Select any entry in a list to drill down to the certification tasks list which lets you then access the tasks themselves for processing.

-   **Aging**

    Shows bar charts with counts of data certification tasks that are past due. Past due state is determined by the setting of the **sn\_cmdb\_ws.glide.cmdb.data.manager.aging.policy.task.timeframe** system property \(by default, 61–90 and over 90 days old\). Select a chart to drill down to the certification tasks list which lets you then access the tasks themselves for processing.



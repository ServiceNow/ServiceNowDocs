---
title: Create a hierarchical filter
description: If a record hierarchy is defined for a table that is used as a filter source, you can create a single or multiple select filter that follows that hierarchy. The Manager hierarchy on User \[sys\_user\] is the typical use case.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Select or cascading filters, Filters, Platform Analytics experience, Platform Analytics]
---

# Create a hierarchical filter

If a record hierarchy is defined for a table that is used as a filter source, you can create a single or multiple select filter that follows that hierarchy. The Manager hierarchy on User \[sys\_user\] is the typical use case.

## Before you begin

This procedure requires you to have created a filter and started to configure it as a single or multiple select filter.

Role required: In the inline dashboard editor: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

In the Filter Designer \(**Library** &gt; **Filters** &gt; **New**\): analytics\_filter\_admin or higher

## About this task

A record hierarchy consists of a parent record and all child records where a reference field value defines parent-child relationships. For example, in the Manager hierarchy, this field is the Manager field on the User \[sys\_user\] table. One user is the parent, and all users who have that user specified in the Manager field are child records. The hierarchy is multi-generational, so to speak, so users with a Manager who have the parent as their Manager are also included in the hierarchy. In short, starting with one manager, that manager's entire downward reporting chain is included in the hierarchy.

When you filter through a record hierarchy, you select one value of the reference field to be the parent. You can then filter by that value and/or by any of its child values.

**Note:**

Hierarchical filters support only the hierarchies defined in the Record Hierarchy \[sys\_record\_hierarchy\] table and not those defined in other tables, such as Governance, Risk, and Compliance \(GRC\) tables. Hierarchical filters generally follow the same logic as hierarchical queries, as described in Building hierarchical queries.

To create a hierarchical dashboard filter, follow the procedure in [Configure a Single/Multiple select or cascading filter](../task/create-select-filter-workspace.md) to create a multi-select filter. When you reach the step where you define the filter source, specify the hierarchy.

## Procedure

1.  Create a filter and select the Single or Multiple Select filter type, as described in [Create or add a filter on an inline dashboard](../task/select-workspace-filter-type.md) or [Create a filter in the Filter Designer](../task/add-filter-library.md).

2.  Select a Table source.

    ![Filter source configuration pane showing filter hierarchy fields.](../image/filter-hierarchy.png)

3.  Select a table that has a record hierarchy, such as User \[sys\_user\].

4.  Do not select a table field.

5.  Select **Is in hierarchy**.

6.  In **Select record hierarchy**, select from among the record hierarchies defined for this table.

    Most tables have no more than one record hierarchy.

7.  In the **Select starting at** field, select the top-level value in the hierarchy for the purposes of this filter.

    The values to select in the filter will be this value and all its child values.

8.  Select **Apply**.

9.  When you select the data to filter, select a field in the same table as the filter source or a reference field that points to the same table as the filter source.

    **Note:** The filter also applies to visualizations of native Data snapshots indicators that have that table specified in their Data snapshots source. For more information, see [Create a Data snapshots source](../../performance-analytics/task/create-ds-source.md).

10. Complete configuring the filter as described in [Configure a Single/Multiple select or cascading filter](../task/create-select-filter-workspace.md).


## Filter on the Manager hierarchy

In your company, you have a manager named Fred Luddy. He has one direct report named Beth Anglin.

![Beth Anglin's User record showing Fred Luddy as manager.](../image/beth-anglin-fred-mgr.png)

Beth in turn has one direct report named Bradly Hasselvander.

![Bradly Hasselvander's user record showing Beth Anglin as manager.](../image/bradly-h-beth-as-mgr.png)

You want a dashboard where the viewer can choose to see the details of indicators owned by anyone in Fred Luddy's reporting chain. You design a dashboard with some relevant data visualizations, and then you add a Multiple Select filter. You select the User table as the source, turn on **Is in hierarchy**, and specify the Manager hierarchy starting with Fred Luddy.

![Filter source configuration pane showing filter hierarchy fields.](../image/filter-hierarchy.png)

For the data to filter, you select Incident.Assigned to, which is a reference field pointing to User.

![Data to filter set to the Assigned to reference field on the Incident table.](../image/filter-hierarchy-target.png)

The end result on the dashboard is a filter that can filter by Fred Luddy, Fred's direct report Beth Anglin, or Beth's direct report Bradly Hasselvander.

![Dashboard with a Incident by priority data visualization and a filter that can filter the data from a manager hierarchy starting from Fred Luddy.](../image/hierarchy-filter-tester-dboard.png)


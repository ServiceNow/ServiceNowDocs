---
title: Create a cascading filter
description: Cascading filters allow you to filter based on multiple values in a hierarchy, such as by region, country, and city. Lower-level choices are filtered by the values selected at higher levels.So that you do not have to clean up the filter panel, duplicate filters are removed automatically.
locale: en-US
release: yokohama
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2026-01-08"
reading_time_minutes: 5
breadcrumb: [Creating Interactive Filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a cascading filter

Cascading filters allow you to filter based on multiple values in a hierarchy, such as by region, country, and city. Lower-level choices are filtered by the values selected at higher levels.

## Before you begin

You can create a cascading filter that allows users to select from a list of managers, then select from groups that report to that manager. Report data is then filtered to show only records assigned to that group. Alternatively, you can leave lower levels of the filter unselected, such as by selecting only a manager but no group. Report data is then filtered to show records assigned to any group managed by that manager. Cascading filters retain the last elements selected on a dashboard.

Ensure that the structure of the data that you use to create the filter is consistent. For example, in a cascading filter based on location, ensure that the top-level choices are all regions, and the second-level choices are all countries. You can define filter conditions to ensure that only appropriate choices for each level are available.

Role required: hp\_publisher\_admin and report\_admin. The hp\_publisher\_admin role exists only for managing interactive filters in Core UI. By default, it contains the role analytics\_filter\_admin for managing Core UI filters that are migrated to Platform Analytics experience.

## About this task

This procedure includes examples based on a cascading interactive filter using managers and groups. In this example, the top-level choice allows users to select a manager and the second-level choice allows users to select a user group managed by that manager.

![Cascading filter example](../image/cascading-filter-example.png "Example cascading filter")

**Note:** You can filter reports based on the values in reference fields only. Cascading filters support only the **Single Select** **UI control type**.

## Procedure

1.  Navigate to **sys\_ui\_hp\_publisher.list**.

2.  Click **New**.

3.  In the **Filter based on** list, select **Cascading Filters**.

4.  Right-click the form header and select **Save**.

5.  Define the first level of the cascading filter.

    1.  In the **Cascading Filter** related list, click **New**.

    2.  Select the **Table** and the **Display field** from the table that contains the values you want to use as the top-level filter choices. The **Display Field** is limited to the types boolean, choice, reference, and string.

        To define the top level of a hierarchy based on managers and the groups they manage, select **Group \[sys\_user\_group\]** as the **Table** and **Manager** as the **Display field.**

    3.  Use the **Filters** field to limit which choices are available to users.

        Filter conditions are especially useful when you create a cascading filter based on a self-referencing table, such as Location \[cmn\_location\]. Filter the data to ensure that each level of the cascading filter only has options appropriate for that level.

    4.  Right-click the form header and select **Save**.

6.  Define the next level of the hierarchy.

    Cascading filters use a one-to-many relationship between higher-level filters and lower-level filters. One higher-level filter can affect the choices available in any number of lower-level filters.

    1.  From the manager filter, in the **Cascading Filter** related list, click **New**.

    2.  Select the **Table** and the **Display field** from the table that contains the values you want to use as the second-level filter choices. The **Display Field** is limited to the types boolean, choice, reference, and string.

        In the managers and groups example, select **Group \[sys\_user\_group\]** as the **Table** and **Name** as the **Display field.**

    3.  In the **Parent Reference Field** field, select the field that contains the value selected from the higher-level filter.

        For example, when you create the Group filter, the **Parent Reference Field** value is **Manager**. In this example, the manager selected in the first filter is used to filter the list of available groups based on the **Manager** field value of each group.

    4.  Right-click the form header and select **Save**.

    5.  Repeat these substeps for each additional filter you want to add.

        To add another level to the filter hierarchy, add a new record in the **Cascading Filter** related list of the lowest-level filter. For example, add the Group filter instead of a top-level filter such as the Manager filter.

7.  Define how each filter level applies the filter to reports on a dashboard.

    1.  In the **Target Tables** related list, click **New**.

    2.  Select the **Target table** that contains the data you want to filter, such as **Incident**.

    3.  Select the **Field** to filter on.

        The field must reference the table specified in the filter. For example when filtering incident data, the **Field** for the top-level manager filter is **Assignment group.Manager**. In this example, the **Field** for the second-level group filter is **Assignment group**.

    4.  Click **Submit**.

    5.  Repeat these substeps to add targets for each level of the filter.

        You can define multiple targets for each filter level. For example, filter incident data by assignment group or CMDB CIs by support group using the same Groups \[sys\_user\_group\] filter.

        **Note:** A cascading filter hierarchy must specify at least one target. You can define a cascading filter that skips levels in a hierarchy, or a cascading filter that only specifies targets for certain levels in a hierarchy. For example, define a target only for the Group-level filter and not the Manager-level filter. In this example, reports are filtered only when a user selects a specific group and not just a manager.

    The following images demonstrate the completed configuration for the example cascading filter. The **Cascading Filter** related list \(not shown\) in the top-level filter contains the second-level filter.

    |Top-level filter|Second-level filter|
    |----------------|-------------------|
    |![Cascading filter top-level filter example](../image/cascading-filter-form-1.png)|![Cascading filter second-level filter example](../image/cascading-filter-form-2.png)|


## What to do next

1.  After you create all levels of the filter, add it to a dashboard.
2.  On the dashboard, select the **Edit widget** icon \(![Edit columns icon](../image/icon-cogwheel-ac.png)\) on each visualization on the dashboard that should follow the filter and select **Follow interactive filter**.

**Parent Topic:**[Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md)

## Cascading filters deduplication

So that you do not have to clean up the filter panel, duplicate filters are removed automatically.

Duplicate filters are removed according to the following criteria:

-   If the configuration is the same, the last edited filter is retained.
-   If the configuration is the same, except that some filters have only one target and others have multiple targets, then only the last updated filter is retained.
-   If the configuration is the same, but some filters have multiple target columns in the same target table, then all the filters are considered as separate filters and retained. An example of multiple target columns in the same target table is the **Date opened** and **Date escalated** columns in the incident table.
-   If the configuration and the UI control are the same, but the base condition is different for any two filters, then they are considered separate filters and retained.


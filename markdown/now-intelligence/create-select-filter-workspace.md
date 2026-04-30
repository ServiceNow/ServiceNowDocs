---
title: Configure a Single/Multiple select or cascading filter
description: Let users filter a dashboard tab on one or more values from a set of choices, such as incident priority. You can have a single or multiple select filter follow another filter in a cascade.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Filters, Platform Analytics]
---

# Configure a Single/Multiple select or cascading filter

Let users filter a dashboard tab on one or more values from a set of choices, such as incident priority. You can have a single or multiple select filter follow another filter in a cascade.

## Before you begin

**Important:** This procedure assumes you’ve created a filter in the Filter designer or added a filter to your dashboard with the Single select or Multiple select filter type. See [Create or add a filter on an inline dashboard](select-workspace-filter-type.md) or [Create a filter in the Filter Designer](add-filter-library.md).

Role required: In the inline dashboard editor: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

In the Filter Designer \(**Library** &gt; **Filters** &gt; **New**\): analytics\_filter\_admin, admin

## About this task

Filters apply to data visualizations and simple lists. For the filter to apply to a specific data visualization, it must be based on the same table or indicator breakdown as that visualization. For it to apply to a list, it must filter a field in the list.

On a tabbed dashboard, a filter can apply either to the items in a single tab or to the entire dashboard. For the filter to apply to a single tab, add the filter to that tab. For the filter to apply to the entire dashboard, add it above the tabs.

A Single select filter lets users filter items by one value.

![Single select filter, showing one value being selected.](../image/paw-filter-single-select.gif)

A Multiple select filter lets users select multiple values of a field or breakdown.

![Multiple select filter, showing several values being selected.](../image/paw-filter-multi-select.gif)

## Procedure

1.  Create a filter and select the Single or Multiple Select filter type, as described in [Create or add a filter on an inline dashboard](select-workspace-filter-type.md) or [Create a filter in the Filter Designer](add-filter-library.md).

2.  In **Filter source type**, select either a Table or an Indicator breakdown.

    MetricBase tables are available under Tables.

3.  Specify the filter source, depending on source type.

    -   If you selected the Table type, select the table and the field.

        **Note:**

        -   You can select only reference fields and fields that have a Choice list. If the table has only non-reference string and numeric fields, you do not have any fields to select from.
        -   If you select no field, you can filter only data on that table or in reference fields that point to that table. For example, if you select the Company table as your filter source, you can only filter the Company table or reference fields pointing to Company, such as Incident.Caller.Company or Incident.Location.Company.
        -   If you select a MetricBase table, don’t select a field.
        -   If you select a field that is a reference field to another table, the filter source resets to refer to that table with no field selected. The data to filter is set automatically to the reference field that you originally selected. As additional data to filter, you can set only the table in the filter source or other reference fields pointing to that table.

            ![Changing the data source to a reference field, which in turn changes the table.](../image/paw-filter-ref-field-source.gif)

    -   If you selected the Indicator breakdown type, select an indicator breakdown.

        **Important:**

        -   You can only select a breakdown that is used by at least one indicator.
        -   Scripted breakdowns on data visualizations are not supported.
        -   Only two levels of breakdown can be applied to an indicator at the same time. On a dashboard, this could be two filters or one filter and a breakdown specified in the data visualization.
4.  To limit the values that the runtime user can choose to filter by, select **Configure values \(number\)**.

    A list of possible values opens. Clear a value to prevent runtime users from filtering by it.

    ![Checklist of possible table values.](../image/paw-filter-configure-values.png "Configure values list and resulting choices in runtime")

    ![Available values in runtime.](../image/paw-filter-restricted-runtime-values.png "Configure values list and resulting choices in runtime")

    **Note:** If the filter source is a reference to a table, you don’t have a list of values to configure. Instead, you can build a condition to set the values in the filter. You can also set a related list condition.

5.  Select the default value or values for the filter.

    The dashboard applies these values when a user opens the dashboard.

6.  Select the data to filter.

    Some data to filter is chosen automatically depending on the filter source. For example, if you select the Category indicator breakdown from the Incident.Category breakdown source, the filter automatically filters the Category field on the Incident table and any indicators with the Category breakdown. You can edit the automatic data selection or add more data to filter.

    **Note:** Your selection of filter source can impact which data you can filter. For more information, see Step [3](create-select-filter-workspace.md#step_filter-source).

7.  Under **Other filters to follow**, if the conditions are met, you can select another filter for the current filter to follow in a hierarchy, creating a cascade.

    **Note:** You can only set **Other filters to follow** when you are configuring filters on a dashboard, not from the filter designer.

    When you set the filter to follow another filter, the choices available in the following filter are limited by the choices made in the followed filter. For more information, see the example [Cascading filters for Manager and Assignment Group](create-select-filter-workspace.md#example_pnj_s4m_4xb).

    Conditions:

    -   You can follow a filter only if Pill is the UI element for that filter.
    -   Only Table and Indicator Breakdown filters support cascading filters.
    -   The filter to be followed must filter data on the same table as the filter source of the following filter.
    **Note:**

    -   Some filters have a many-to-many relationship, where values on both filters can match multiple values on the other filter. One such filter can follow another only through a connecting table. Only admins can set up these cascading filters. For more information, see [Set a filter to follow another filter in a many-to-many relationship](set-filter-to-follow-filter.md).
    -   Two filters can follow each other, but there are additional requirements. For more information, see [Conditions for two filters to follow each other](../concept/filters-follow-each-other.md).
8.  Select the **Sort direction**.

    If you select **Ascending**, the lowest filtered values are shown first. If you select **Descending**, the highest values are shown first. The user can change this value.

9.  To let users clear the values they selected for the filter, enable **Allow filter clearance**.

10. Set the maximum number of elements that are loaded initially and at each page refresh.

    The default value is 500.

11. Select **Save**.


## Result

The filter is ready to use when you exit editing mode.

## Cascading filters for Manager and Assignment Group

In this example, you want your users to filter incidents by manager or by assignment group. Also, you want to limit the assignment groups that are available in the second filter to those with the manager selected in the first filter.

1.  You create data visualizations of incidents, such as a single score data visualization of the number of incidents on the Incident \[incident\] table.
2.  You create a filter to filter incidents by assignment group manager.

    1.  First, you create a Single select filter labeled Manager.

        ![New single select filter with Manager label.](../image/filter-ex-inc-ass-man-label.png)

    2.  You select the User \[sys\_user\] table as the data source. The Manager field is in that table.

        ![User table selected as the filter source for the Manager filter.](../image/filter-ex-inc-ass-man-source.png)

    3.  Because you want to apply this filter to a data visualization of Incident table data, you edit the **Data to filter** field to point to the Incident table and the dotwalked reference field Assignment group.Manager.

        ![The dotwalked field Incident.Assignment Group.Manager selected as data to filter.](../image/filter-inc-ass-man-data-2-filter-1.png)

    4.  Still under **Data to filter**, you select **Add+** and add the Manager field on the Group \[sys\_user\_group\] table. You will need this field later when you set up a cascading filter.

        ![The Manager field on the Group table selected as a second set of data to filter.](../image/filter-inc-ass-man-data-2-filter-2.png)

    ![Completed filter on the User table data source filtering the dot walked incident - assignment group - manager field.](../image/filter-ex-inc-ass-man.png "Completed configuration for the Manager filter")

3.  You create a filter to filter incident data by assignment group.

    1.  First, you create a multiple select filter labeled Group.
    2.  Then you select the Assignment Group field of the Incident \[incident\] table as the filter source.
    Because Assignment Group is a reference field that refers to the Group \[sys\_user\_group\] table, the filter source resets automatically to the Group table. The data to filter remains Incident.Assignment Group.

    ![Filter with the Group table as filter source that filters the Assignment Group field on the Incident table.](../image/paw-group-filter.png)

4.  Scroll down the Group filter's configuration panel to **Other filters to follow**.

5.  Under **Directly connected filters**, you select **Follow Manager**.

    ![Other Filters to Follow section of the configuration panel for the Group filter, with a toggle to follow the Manager filter.](../image/paw-follow-filter.png)

    This choice appears because you configured the Manager filter to filter data on the Group table and not only on the Incident table. Remember that to have a cascading filter, the filter that will be followed \(in this case Manager\) must filter data on the same table as the filter that does the following \(in this case Group, on the table sys\_user\_group\).

6.  Save and exit editing mode.

Later, a dashboard viewer selects Beth Anglin in the Manager filter. Then, when selecting assignment groups in the Group filter, only those groups with Beth Anglin as the manager are available.

![Dashboard filtered by Beth Anglin as manager, showing only those assignment groups they manage as available to filter by.](../image/paw-cascading-filters.png)

## What to do next

If you have the required roles, add the filter to the filter library. You can also reconfigure, delete, or duplicate the filter. For more information, see [Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md).

-   **[Set a filter to follow another filter in a many-to-many relationship](set-filter-to-follow-filter.md)**  
In some cases, values on a pair of filters can refer to multiple values on each other. For one such filter to follow another, it must go through a connecting table.
-   **[Conditions for two filters to follow each other](../concept/filters-follow-each-other.md)**  
It is possible to set up two filters to follow each other mutually. However, several technical limitations apply.

**Parent Topic:**[Filters in Platform Analytics](../concept/interactive-filters-workspace.md)

**Related topics**  


[Create or add a filter on an inline dashboard](select-workspace-filter-type.md)

[Create a filter in the Filter Designer](add-filter-library.md)

[Create a filter on a technical dashboard in UI Builder](add-filter-tech-dashboard.md)

[Make a data visualization act as a filter](make-dv-act-as-filter.md)

[Configure a True/False filter](create-boolean-filter-workspace.md)

[Configure a Date filter in the inline editor](create-date-filter-workspace.md)

[Create a domain filter](create-domain-filter.md#)

[Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md)

[Troubleshoot breakdown filters](troubleshoot-breakdown-filters.md)

[Applying filters to Process Mining maps](../concept/applying-filters-to-process-optimization-maps.md)


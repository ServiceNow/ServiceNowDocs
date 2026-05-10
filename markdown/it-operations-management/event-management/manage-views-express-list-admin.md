---
title: Create a predefined Express List view for users
description: Configure an Express List view for users to make sure that they focus on specific services, priorities, or alerts. You can set the filters, column order, and filter attributes for this view and assign it to individual users or user groups.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Express List views for users and user groups, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create a predefined Express List view for users

Configure an Express List view for users to make sure that they focus on specific services, priorities, or alerts. You can set the filters, column order, and filter attributes for this view and assign it to individual users or user groups.

## Before you begin

For more information about predefined Express List views, see [Configuring Express List views for users and user groups](../../service-operations-workspace-itom/concept/manage-views-express-list.md).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Express List Views**.

2.  Select **New**.

3.  On the **Express List View** form, fill in the fields.

<table id="table_q5z_5vb_k1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the Express List view.

</td></tr><tr><td>

Primary Sort By Field

</td><td>

The field by which to sort the Express List. Default: Initial event generation time.

</td></tr><tr><td>

Secondary Sort By Field

</td><td>

Optional field by which to sort the results of the primary sort-by field.

</td></tr><tr><td>

Order

</td><td>

The order of this Express List view, if multiple views exist.

</td></tr><tr><td>

Order of Primary Sort By Field

</td><td>

The sorting order of the Primary Sort By Field: Ascending or Descending.

</td></tr><tr><td>

Order of Secondary Sort By Field

</td><td>

The sorting order of the Secondary Sort By Field, if set: Ascending or Descending.

</td></tr><tr><td>

Default

</td><td>

Option to set this Express List view as the default view for the assigned user or group.If multiple default views exist, the value set in the Order field determines their order.

</td></tr></tbody>
</table>4.  Set filter conditions for the Express List view.

    1.  In the **Filter** tab, select a field, an operator, and one or more values for a condition.

        **Note:** The default field is State. When selecting fields for filter conditions, use only direct reference fields or single-level references and not nested references. Nested references in filter conditions aren’t supported. For example,  **Configuration item.Class**  uses a reference field, **Configuration item**, that  contains  another reference field, **Class**.

    2.  Add a filter condition or alert tag filter condition.

<table id="table_bfk_45j_k1c"><thead><tr><th>

Task

</th><th>

Actions

</th></tr></thead><tbody><tr><td>

Add a filter condition

</td><td>

1.  Select either the AND or the OR operator.
2.  Select a field, an operator, and one or more values for the condition.


</td></tr><tr><td>

Add an alert tag filter condition

</td><td>

1.  In the Alert Tags Filter section, select **Insert a new row**.
2.  Select the required tag, operator, and value for each tag filter.
3.  Optionally add additional filter conditions by selecting **New criteria** and adding the tag filter condition.


</td></tr></tbody>
</table>    3.  View the number of results a query with the configured conditions would return by selecting **Preview**.

5.  Assign users and groups to the Express List view.

<table id="choicetable_lyp_4hp_k1c"><thead><tr><th align="left" id="d651453e355">

Task

</th><th align="left" id="d651453e358">

Procedure

</th></tr></thead><tbody><tr><td id="d651453e364">

**Assign a user to the selected Express List view**

</td><td>

1.  In the **Users** tab, select **Insert a new row**.
2.  Select the search icon ![Search icon](../image/search-icon.png)and search for the relevant user in the **Users** table.
3.  Select the user.
4.  Select the save icon ![Save icon.](../../itom-cloud-accelerate/image/save-icon.png).


</td></tr><tr><td id="d651453e408">

**Assign a user group to the selected Express List view**

</td><td>

1.  In the **Groups** tab, select **Insert a new row**.
2.  Select the search icon ![Search icon](../image/search-icon.png) and search for the relevant group in the **Groups** table.
3.  Select the group.
4.  Select the save icon ![Save icon.](../../itom-cloud-accelerate/image/save-icon.png).
 **Note:** Users who belong to a group can only see the views that you assigned to that group. If a user belongs to multiple groups, they can see the views you configured for all of these groups.

</td></tr></tbody>
</table>6.  From the form menu, select **Save**.

    The following tabs display:

    -   The **Express List Table Fields** tab shows the fields to be displayed as table columns in Express List.
    -   The **Express List View Field Attributes** tab shows the filter attributes for the open alerts in Express List.
7.  Add columns to the Express List.

    1.  In the **Express List Table Fields** tab, select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Field|The column to add.|
        |Express List View|Name of the view to which to add the column.|
        |Minimum width|Minimum width of the column in pixels.|
        |Order|Position of the column in the table.|
        |Active|Option to display the column.|

    3.  Select **Submit**.

8.  Add filter attributes to customize this view for assigned users.

    These filters are automatically applied to the Filters pane in Express List when users select this view.

    1.  In the **Express List View Field Attributes** tab, select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Field|Attribute to add to the Filter pane.|
        |Express List View|Name of the view to which to add the attribute.|
        |Order|Position of the attribute in the pane.|
        |Active|Option to activate the attribute.|

9.  Exclude fields from the Express List view by deactivating them.

    1.  In the **Express List Table Fields** tab, select the information icon ![](../image/information_icon.png) for the relevant field record.

    2.  Select **Open Record**.

    3.  On the field form, clear the **Active** check box.

    4.  Select **Update**

10. Exclude field attributes from the Express List view by deactivating them.

    1.  In the **Express List View Field Attributes** tab, select the information icon ![](../image/information_icon.png) for the relevant field attribute record.

    2.  Select **Open Record**.

    3.  On the field form, clear the **Active** check box.

    4.  Select **Update**.

    **Note:** You can view the updated state of a field or a field attribute in the table by selecting the list controls icon ![List control button](../../service-mapping/image/list-controls-button.png) and then selecting **Refresh List**.

11. When you're satisfied with the Express List view, select **Update**.


**Parent Topic:**[Configuring Express List views for users and user groups](../../service-operations-workspace-itom/concept/manage-views-express-list.md)


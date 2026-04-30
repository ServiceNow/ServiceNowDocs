---
title: Create a predefined Express List view for users
description: Configure an Express List view for users to make sure that they focus on specific services, priorities, or alerts. You can set the filters, column order, and filter attributes for this view and assign it to individual users or user groups.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Express List Configuring Express List views for users and user groups, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Create a predefined Express List view for users

Configure an Express List view for users to make sure that they focus on specific services, priorities, or alerts. You can set the filters, column order, and filter attributes for this view and assign it to individual users or user groups.

## Before you begin

For more information about predefined Express List views, see [Express List Configuring Express List views for users and user groups](../../service-operations-workspace-itom/concept/manage-views-express-list.md).

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

The field by which to sort the results of the primary sort-by field. This field is optional.

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

    **Note:** When you include even a single unsupported filter in your Express List view, it prevents the Event Management operator from modifying the settings of any filters in this view, including those that are supported. If you want to allow operators to adjust their personal view, make sure to only include supported filters.

    1.  In the **Filter** tab, select a field, an operator, and one or more values for a condition.

        **Note:** The default field is State.

    2.  Perform the following tasks:

<table id="table_bfk_45j_k1c"><thead><tr><th>

Task

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Add a filter condition

</td><td>

1.  Select either the AND or the OR operator.
2.  Select a field, an operator, and one or more values for the condition.


</td></tr><tr><td>

Add an alert tag filter condition

</td><td>

1.  In the Alert Tags Filter section, select **Insert a new row...**.
2.  Select the required tag, operator, and value for each tag filter.


</td></tr><tr><td>

Add an additional set of alert tag filter conditions

</td><td>

1.  In the Alert Tags Filter section, select **New Criteria**.
2.  Add the required tag filter conditions.


</td></tr><tr><td>

View the number of results a query with the configured conditions would return

</td><td>

Select **Preview**.

</td></tr></tbody>
</table>5.  Assign users and groups to the Express List view.

<table id="choicetable_lyp_4hp_k1c"><thead><tr><th align="left" id="d542704e384">

Task

</th><th align="left" id="d542704e387">

Procedure

</th></tr></thead><tbody><tr><td id="d542704e393">

**Assign a user to the selected Express List view**

</td><td>

1.  In the **Users** tab, select **Insert a new row...**.
2.  Select the search icon \(![Search icon.](../image/search-icon.png)\) and search for the relevant user in the **Users** table.
3.  Select the user and then select the save icon \(![Save icon.](../../itom-governance/image/save-icon.png)\).


</td></tr><tr><td id="d542704e438">

**Assign a user group to the selected Express List view**

</td><td>

1.  In the **Groups** tab, select **Insert a new row...**.
2.  Select the search icon \(![Search icon.](../image/search-icon.png)\) and search for the relevant group in the **Groups** table.
3.  Select the group and then select the save icon \(![Save icon.](../../itom-governance/image/save-icon.png)\).
 **Note:** Users who belong to a group can only see the views that you assigned to that group. If a user belongs to multiple groups, they can see the views you configured for all of these groups.

</td></tr></tbody>
</table>6.  From the form menu, select **Save**.

    The following tabs display:

    -   The **Express List Table Fields** tab shows the fields to be displayed as table columns in Express List.
    -   The **Express List View Field Attributes** tab shows the filter attributes for the open alerts in Express List.
7.  Add table fields and field attributes to the Express List view.

<table id="choicetable_s15_jxj_k1c"><thead><tr><th align="left" id="d542704e535">

Task

</th><th align="left" id="d542704e538">

Procedure

</th></tr></thead><tbody><tr><td id="d542704e544">

**Add a column to the Express List table**

</td><td>

1.  In the **Express List Table Fields** tab, select **New**.
2.  On the form, fill in the fields:
    -   Field: The column to add.
    -   Express List View: The name of the view to which to add the column.
    -   Minimum Width: Minimum width of the column.
    -   Order: The position of the column in the table.
    -   Active: Option to activate the column.
3.  Select **Submit**.


</td></tr><tr><td id="d542704e598">

**Add an attribute to the Filter pane in Express List**

</td><td>

1.  In the **Express List View Field Attributes** tab, select **New**.
2.  On the form, fill in the fields:
    1.  Field: The attribute to add to the Filter pane.
    2.  Express List View: The name of the view to which to add the attribute.
    3.  Order: The position of the attribute in the pane.
    4.  Active: Option to activate the attribute.
3.  Select **Submit**.


</td></tr></tbody>
</table>8.  Exclude fields or field attributes from the Express List view by deactivating them.

<table id="choicetable_ng2_jkc_k1c"><thead><tr><th align="left" id="d542704e660">

Task

</th><th align="left" id="d542704e663">

Procedure

</th></tr></thead><tbody><tr><td id="d542704e669">

**Deactivate a field**

</td><td>

1.  In the **Express List Table Fields** tab, select the information icon \(![Information icon](../image/information_icon.png)\) to the left of a field record.
2.  On the field form, clear **Active**.
3.  Select **Update**.


</td></tr><tr><td id="d542704e707">

**Deactivate a field attribute**

</td><td>

1.  In the **Express List View Field Attributes** tab, select the information icon \(![Information icon](../image/information_icon.png)\) to the left of a field attribute record.
2.  On the field form, clear **Active**.
3.  Select **Update**.


</td></tr></tbody>
</table>    **Note:** You can view the updated state of a field or a field attribute in the table by selecting the list controls icon \(![List controls icon.](../../service-mapping/image/list-controls-button.png) \) and then selecting **Refresh List**.

9.  When you're satisfied with the Express List view, select **Update**.


**Parent Topic:**[Express List Configuring Express List views for users and user groups](../../service-operations-workspace-itom/concept/manage-views-express-list.md)


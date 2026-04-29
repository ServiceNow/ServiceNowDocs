---
title: Configure an encoded query data item for chart screens
description: Configure an encoded query data item to query data for chart screens. An encoded query data item is a parametrized data item that is the basis for a chart screen to be passed to a list screen. When tapped it enables users to drill-down to a list of items that the chart is created from.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data items, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an encoded query data item for chart screens

Configure an encoded query data item to query data for chart screens. An encoded query data item is a parametrized data item that is the basis for a chart screen to be passed to a list screen. When tapped it enables users to drill-down to a list of items that the chart is created from.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Data** category, and then select **New**.

4.  From the Create a data item dialog box, select the type of data item you want to create, and then select **Continue**.

    You can select either a standard **Data item** or a **Relationship data item**.

5.  Complete the following fields as needed.

<table id="table_cbg_pzm_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A title for the data item. You can have multiple data items with the same name. Make sure that this name is unique so that you can find it easily.

</td></tr><tr><td>

Description

</td><td>

Optional additional details about the data item

</td></tr><tr><td>

Table

</td><td>

The name of the table you want the data item to pull information from.**Note:** Custom tables are not available by default. You can change this behavior by modifying the **subscription.custom\_table.enforce\_entitlement** system property. For details on making this change, see [Allow or restrict access to custom tables in mobile data items](sg-allow-custom-tables.md).

</td></tr><tr><td>

Condition type

</td><td>

Determines what type of condition your data item uses. For an encoded query data item, select **Append Encoded Query**.

</td></tr><tr><td>

Append Encoded Query

</td><td>

This field only appears after you select **Append Encoded Query** in the **Condition type** field. Leave this field empty. You use this field in later steps.

</td></tr></tbody>
</table>6.  In the Parameters section, select **New**.

    The Data Parameter form appears.

7.  In the **Name** field, enter a name for your parameter. For example, `URL`.

8.  In the **Type** field, select **String**.

9.  Select the data item record in the configuration tree to navigate back to the data item record.

10. In the **Append Encoded Query** field, select the parameter you created in the previous steps.

11. Select **Save**.


## What to do next

For more information on how parameters pass values between screens, see [Parametrized list screens](../concept/list-applet-parameters.md).


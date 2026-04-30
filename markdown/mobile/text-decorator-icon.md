---
title: Create text decorator icon
description: Use a text decorator icon to selectively highlight list elements that need your users attention.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile UI styles, Mobile styles, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create text decorator icon

Use a text decorator icon to selectively highlight list elements that need your users attention.

## Before you begin

Role required: admin

## Procedure

1.  On your instance, navigate to **System Mobile** &gt; **Mobile UI Styles**.

2.  In the **UI Styles** list, click the **New** button.

3.  In the **UI Style** form, fill in the fields as needed.

<table id="table_fzr_g5q_slb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your UI style

</td></tr><tr><td>

Table

</td><td>

Table to which the UI style applies. Use the same table as the screen where you apply your style.

</td></tr><tr><td>

Condition

</td><td>

Condition under which the icon is visible. Leave the condition field blank to apply the icon to all records.

</td></tr><tr><td>

Use Item View elements

</td><td>

Whether the item view elements are used. Enable this checkbox to create a text decorator icon.

</td></tr><tr><td>

Item view

</td><td>

The item view where the icon appears. Use the same item view as the screen where you want to see your icon.

</td></tr><tr><td>

Item view element

</td><td>

The element of the item view where you want to see your icon.

</td></tr><tr><td>

Style

</td><td>

The style where you define your icon. For a text decorator icon, use `text_decorator_icon` in the first box, and the **Sys\_id** of the icon in the second box.**Note:** You can find your available icons on the **Icon** \[sys\_sg\_icon\] table. You can right-click any icon on this list and select **Copy sys\_id** from the context menu to copy the sys\_id.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Example

This example demonstrates how to apply a text decorator icon to all records on an incident list in the **New** state.

![UI style configuration for a text decorator icon.](../image/text-decor-ui-style.png)

This example applies to the **State** element of the **Incident List Screen Item View** UI style. The condition field has been set, so the icon only appears for records in the **New** state. The icon is located on the **Icon** \[sys\_sg\_icon\] table.

![List of incidents displaying an icon for records in the New state.](../image/text-decor-result.png)


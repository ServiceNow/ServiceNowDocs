---
title: Edit page variant settings
description: Edit page variant settings to add additional criteria to determine when the page variant displays to users.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a page variant, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Edit page variant settings

Edit page variant settings to add additional criteria to determine when the page variant displays to users.

## Before you begin

Role required: admin

## About this task

Customize page variant settings to set who sees the page variant. You can add and remove audiences as well as edit conditions to determine when a page variant is shown. Conditions can only evaluate the listed parameters. Conditions are based on setting an order and adding a query string that sets the criteria that must be met for the page variant to display. If you have multiple page variants that all have the same conditions, then the variants go by the order setting. The following task shows how to set the variant conditions and order.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open the experience with the page variant that you want to edit.

3.  Select **Settings** next to the page that you want to edit.

    ![Arrow pointing to settings link to edit variant settings.](../image/variant-edit-settings.png)

4.  On the form, fill in the fields.

<table id="table_zgj_fwf_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the page variant.

</td></tr><tr><td>

Availability

</td><td>

Select **Active** to make the page variant viewable to the selected audience.

</td></tr><tr><td>

Order

</td><td>

Add an order for the condition in the **Order** field. You may want certain conditions to have a higher priority than others. The lower the number, the higher the priority.

</td></tr><tr><td>

Conditions

</td><td>

Set the rules for when your pages are shown. For more information, see [Control the conditions for a page variant](control-conditions-for-your-variant.md).

</td></tr><tr><td>

Audiences

</td><td>

Add or remove audiences for the page variant. For more information, see [Learn about audiences](../concept/add-audiences.md).

</td></tr></tbody>
</table>    ![Edit page variant settings screen.](../image/variant-edit-settings-screen.png)

5.  Click **Save**.


**Parent Topic:**[Create a page variant](create-variant.md)


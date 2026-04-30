---
title: Configure sorting display options for mobile filters
description: Customize the way sorting options are displayed in your mobile filter and override the default behavior.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure sorting capabilities, Mobile list screen filters, List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure sorting display options for mobile filters

Customize the way sorting options are displayed in your mobile filter and override the default behavior.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  In the web-based UI, enter `sys_sg_item_sorting_attribute.list` in the filter navigator.

2.  Select **New**.

3.  From the **Item Sorting** field, select the reference lookup icon \(![Reference lookup icon](../image/reference-lookup-icon.png)\) and select the item sorting entry to configure.

4.  Define attributes to configure for the selected item sorting.

<table id="choicetable_cl5_cp2_1qb"><thead><tr><th align="left" id="d33198e91">

Attribute option

</th><th align="left" id="d33198e94">

Action

</th></tr></thead><tbody><tr><td id="d33198e100">

**Define the ascending label**

</td><td>

1.  From the **Name** field, select the reference lookup and select `Ascending Label`.
2.  Enter a custom label in the **Translatable Value** field. The entered value takes priority over the value in the item sorting **Label** field in the Item sorting form.
3.  Right-click in the header and select **Save**.


</td></tr><tr><td id="d33198e136">

**Define the descending label**

</td><td>

1.  From the **Name** field, select the reference lookup and select `Descending Label`.
2.  Enter a custom label in the **Translatable Value** field. The entered value takes priority over the value in the item sorting **Label** field in the Item sorting form.
3.  Right-click in the header and select **Save**.


</td></tr><tr><td id="d33198e172">

**Hide the ascending/descending suffix**

</td><td>

**Note:** Use this option when the ascending or descending suffix is not needed, for example, "Recently added".

 1.  From the **Name** field, select the reference lookup and select `Hide Direction Label`.
2.  Enter the value `true` in the **Value** field. The instance does not display the `(ascending)` and `(descending)` suffix name next to the item sorting name.
3.  Right-click in the header and select **Save**.


</td></tr><tr><td id="d33198e217">

**Display either ascending/descending option**

</td><td>

1.  From the **Name** field, select the reference lookup and select `Order Options`.
2.  Perform one of the following:
    -   Enter the value `ascending` in the **Value** field to display only the ascending sorting option.
    -   Enter the value `descending` in the **Value** field to display only the descending sorting option.
3.  Right-click in the header and select **Save**.


</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

After configuring various sorting display options, your filter sorting configuration may look like the one in the image.

![Filter things](../image/mobile-filter-sort-customize.png)


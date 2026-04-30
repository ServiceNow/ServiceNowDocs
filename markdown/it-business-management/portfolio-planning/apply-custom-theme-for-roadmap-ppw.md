---
title: Apply a custom theme to roadmap
description: Apply your custom theme to ensure roadmap bar colors align with your organization’s style.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [Configuring roadmap in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Apply a custom theme to roadmap

Apply your custom theme to ensure roadmap bar colors align with your organization’s style.

## Before you begin

-   You have created and published a custom theme to apply to the roadmap.
-   Ensure the application scope in your instance is set to **Portfolio Planning**.

Role required: admin

## About this task

To update the color theme for your roadmap bars, you must copy the sys\_id of your custom theme, and then create a system property and set its value to the copied sys\_id.

The colors configured in the custom theme will be applied to the roadmap bars. However, these colors won’t affect the colors of roadmap milestones or planning item milestones.

## Procedure

1.  Copy the sys\_id of the custom theme.

    1.  Navigate to **Now Experience Framework** &gt; **Theme Management** &gt; **Themes**.

    2.  Search for the custom theme that you want to apply to the roadmap.

    3.  Right-click the name of your custom theme and select **Copy sys\_id**.

    The sys\_id of your custom theme is copied.

2.  Create a system property and enter the copied sys\_id in the form.

    1.  Navigate to **All** &gt; **System properties** &gt; **All properties**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_ffy_qlw_mhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the system property.Enter the name as `sn_align_ws.spw_custom_theme`

</td></tr><tr><td>

Application

</td><td>

Application scope for the system property.Ensure the scope is set to **Portfolio Planning**.

</td></tr><tr><td>

Type

</td><td>

System property type.Set the type to **string**.

</td></tr><tr><td>

Value

</td><td>

Sys\_id of the custom theme you created for roadmap bar colors.Enter the copied sys\_id.

</td></tr></tbody>
</table>    4.  Select **Submit**.

    The system property is created and updated to include the custom theme information.


## Result

The roadmap bars now display the colors configured in the custom theme.


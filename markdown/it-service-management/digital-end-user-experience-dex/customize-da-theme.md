---
title: Customize themes for Desktop Assistant
description: Customize themes for the Desktop Assistant application by applying available themes or modifying specific theme CSS variables to align with your organization's branding.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Customize themes for Desktop Assistant

Customize themes for the Desktop Assistant application by applying available themes or modifying specific theme CSS variables to align with your organization's branding.

## Before you begin

Confirm that the DEX Desktop Assistant \[sn\_dex\_desktop\] application has been installed. For more information, see [Install Application and Device Health](install-app-device-health.md) and [Download and install Desktop Assistant](download-desktop-experience.md).

Role required: sn\_dex\_desktop.admin

## Procedure

1.  Navigate to **All** &gt; **Desktop Assistant** &gt; **Configuration** &gt; **Application**.

2.  Customize the Desktop Assistant theme.

    **Note:** Employee Center \(EC\) Theme is the default theme applied for Desktop Assistant.

<table id="choicetable_eqs_cbd_phc"><thead><tr><th align="left" id="d159703e168">

Method

</th><th align="left" id="d159703e171">

Steps

</th></tr></thead><tbody><tr><td id="d159703e177">

**Apply another available theme**

</td><td>

1.  In the Desktop Assistant form, select the Lookup using list icon ![](../image/icon-magnifying-glass-blue.png) in the **Theme** field.
2.  On the Themes page, select a theme from the themes list.

The selected theme is updated in the **Theme** field of the Desktop Assistant form.

3.  Select **Update**.


</td></tr><tr><td id="d159703e222">

**Customize the default theme by modifying specific CSS variables**

</td><td>

1.  In the Desktop Assistant form, select the Preview this record icon ![](../../service-operations-workspace/image/inc-preview-record.png) near the **Theme** field.
2.  In the preview dialog box, select **Open Record**.
3.  In the **CSS variables** section, modify the predefined variables in one of the following ways:
    -   Direct value assignment: Assign values directly to the variables. For example, `$sp-space—xl: 4px;`
    -   Indirect value assignment: Create a reference to an existing variable by assigning to a variable the value of another variable. For example, `$badge-color: $text-white;`
    -   Using the ceil \(\) function: Calculate a variable value and use the ceil \(\) function to round up the value to the nearest whole number. For example, `ceil(($font-size-base * 1.125)) // 18px;`
4.  Select **Update**.


</td></tr><tr><td id="d159703e292">

**Customize a theme other than the default theme**

</td><td>

1.  In the Desktop Assistant form, select the Lookup using list icon ![](../image/icon-magnifying-glass-blue.png) in the **Theme** field.
2.  On the Themes page, select a theme from the themes list.

The selected theme is updated in the **Theme** field of the Desktop Assistant form.

3.  Select the Preview this record icon ![](../../service-operations-workspace/image/inc-preview-record.png) near the **Theme** field.
4.  In the preview dialog box, select **Open Record**.
5.  In the **CSS variables** section, modify the predefined variables in one of the following ways:
    -   Direct value assignment: Assign values directly to the variables. For example, `$sp-space—xl: 4px;`
    -   Indirect value assignment: Create a reference to an existing variable by assigning to a variable the value of another variable. For example, `$badge-color: $text-white;`
    -   Using the ceil \(\) function: Calculate a variable value and use the ceil \(\) function to round up the value to the nearest whole number. For example, `ceil(($font-size-base * 1.125)) // 18px;`
6.  Select **Update**.


</td></tr></tbody>
</table>    For more information, see [Variables to customize a theme for Desktop Assistant](../reference/da-theme-variables.md).



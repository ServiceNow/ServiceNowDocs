---
title: Publish multiple themes in Next Experience
description: Publish multiple themes and set the order of your Next Experience custom and Theme Builder themes to configure how they’re displayed in the user's Theme preferences.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multi-theme management, Configuring Next Experience themes and preferences, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Publish multiple themes in Next Experience

Publish multiple themes and set the order of your Next Experience custom and Theme Builder themes to configure how they’re displayed in the user's Theme preferences.

## Before you begin

Role required: admin

## About this task

Publishing multiple themes applies to web instances only.

## Procedure

1.  In the filter navigator, enter `m2m_app_theme.list` and press **Enter**.

    The UX Parent App Theme table appears. This table is used to store the association between multiple themes and a parent application.

2.  Select **New**.

3.  On the form, fill in the fields.

    **Note:** Themes created with Theme Builder are automatically added to the UX Parent App Theme table during publishing and don’t require a new record form. To create a theme with Theme Builder see [Create a theme with Theme Builder](tb-create-theme.md).

    ![UX Parent App Theme record.](../image/ux-parent-app-theme-record.png)

<table id="table_fry_v31_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applicability

</td><td>

Audience that the theme should apply to. For example, you might want to specify that the theme appears only for those users with an admin role.**Note:** Leaving the **Applicability** field empty applies the theme to all users.

</td></tr><tr><td>

Theme

</td><td>

Theme that you want to add to the table.

</td></tr><tr><td>

Order

</td><td>

Order in which the theme is displayed in the Next Experience Theme user preference.**Note:** The applicable theme with the lowest order is considered as the default and appears first in the Next Experience Theme user preference. If the user has not made a selection from their Theme user preference, the theme with the lowest order in the UX Parent App Theme table is set as the default theme.

</td></tr><tr><td>

Application

</td><td>

Application scope.

</td></tr><tr><td>

UX App

</td><td>

Parent application that you want the theme to apply to.

</td></tr></tbody>
</table>4.  Select **Submit**.

    After the record has been added to the UX Parent App Themes table, you’re able to change the **Applicability**, **Order**, and **UX App** fields, as needed. If no records are listed in the table and the **glide.ui.polaris.theme.custom** value is empty, the Unified Navigation base theme is displayed.


**Parent Topic:**[Multi-theme management](../concept/multi-theme-management.md)


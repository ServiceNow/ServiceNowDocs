---
title: Configure a background color for unsaved fields
description: Configure a background color to display on unsaved fields across the entire workspace experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a background color for unsaved fields

Configure a background color to display on unsaved fields across the entire workspace experience.

## Before you begin

Configure a UX page property to enable the unsaved field indicator. For instructions, see [Configure the unsaved indicator](configure-unsaved-field-indicator.md).

Role required: admin

## About this task

The unsaved field indicator displays a dot on unsaved fields. You can configure the indicator and background color for unsaved fields on individual workspace pages in UI Builder.

If you want to display a background color for unsaved fields across the entire workspace experience, configure a UX page property.

The following fields don't support a background color on unsaved fields:

-   `boolean`
-   `conditions`
-   `days_of_week`
-   `email_script`
-   `field_list`
-   `field_name`
-   `file_attachment`
-   `glide_time`
-   `glide_utc_time`
-   `integer_time`
-   `slush_bucket`
-   `time_worked`
-   `timer`
-   `user_image`
-   `css`
-   `json`
-   `percent_complete`
-   `radio`

## Procedure

1.  Navigate to `sys_ux_page_property.list`.

    The entire list of page properties in the UX Page Properties \[sys\_ux\_page\_property\] table opens.

2.  Select **New**.

    A new UX Page Property record opens.

3.  Complete the following fields:

    -   **Page**

        Select the workspace where you want to enable a background color for unsaved fields.

    -   **Name**

        Enter `enableBgColorForUnsavedFieldIndicator`.

    -   **Type**

        Select **true \| false**.

    -   **Value**

        Enter `true`.

4.  Select **Submit**.


## Result

Unsaved field display both an indicator and a background color across the entire workspace experience.

![Unsaved field with a background color and indicator](../image/form-unsaved-background-color.png)


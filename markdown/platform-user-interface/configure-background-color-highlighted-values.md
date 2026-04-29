---
title: Configure a background color for highlighted values
description: Configure a background color for fields with highlighted values.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a background color for highlighted values

Configure a background color for fields with highlighted values.

## Before you begin

Configure a highlighted value for a form header. For instructions, see [Configure a highlighted value](config-ws-highlight-value.md).

Role required: admin

## About this task

The following fields don't support a background color for highlighted values:

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

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Highlighted Value Configurations**.

2.  From the UX Highlighted Value Configurations list, select the configuration for your workspace.

    A UX Highlighted Value Configuration record opens.

3.  Select **Enable Background Color**.

4.  Select **Update**.


## Result

Fields with highlighted values display a background color.

![Highlighted value with a background color](../image/form-highlighted-values-background-color.png)


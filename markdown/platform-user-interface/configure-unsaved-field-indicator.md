---
title: Configure the unsaved field indicator
description: Configure the unsaved field indicator for an entire workspace experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure the unsaved field indicator

Configure the unsaved field indicator for an entire workspace experience.

## Before you begin

Role required: admin

## About this task

The unsaved field indicator displays a dot on unsaved fields. You can configure the unsaved field indicator for individual workspace pages in UI Builder.

If you want to display the unsaved field indicator for the entire workspace experience, configure a UX page property.

The following fields don't support the unsaved field indicator:

-   `time_worked`
-   `password`
-   `domain_path`

## Procedure

1.  Navigate to `sys_ux_page_property.list`.

    The entire list of page properties in the UX Page Properties \[sys\_ux\_page\_property\] table opens.

2.  Select **New**.

    A new UX Page Property record opens.

3.  Complete the following fields:

    -   **Page**

        Select the workspace where you want to enable the unsaved field indicator.

    -   **Name**

        Enter `enableUnsavedFieldIndicator`.

    -   **Type**

        Select **true \| false**.

    -   **Value**

        Enter `true`.

4.  Select **Submit**.


## Result

Unsaved fields display an indicator across the entire workspace experience.

![Field with the unsaved indicator](../image/form-unsaved-indicator.png)

## What to do next

-   **[Configure a background color for unsaved fields](configure-background-color-unsaved-indicator.md)**

    Configure a background color for unsaved fields in addition to the unsaved field indicator.



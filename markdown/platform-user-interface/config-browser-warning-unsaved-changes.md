---
title: Configure a browser warning for unsaved changes
description: Configure a browser warning to display when you navigate away from a Configurable Workspace page with unsaved changes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a browser warning for unsaved changes

Configure a browser warning to display when you navigate away from a Configurable Workspace page with unsaved changes.

## Before you begin

Role required: admin

## About this task

When you navigate away from a Configurable Workspace page using back or forward buttons, a browser warning can display to alert you of unsaved changes.

This browser warning relies on popstate event handling to detect browser navigation actions. It applies to the entire page, not only the form. For example, even if all form fields are saved, the warning would still appear if other components such as the email composer or Activity stream contain unsaved data.

## Procedure

1.  Navigate to `sys_ux_page_property.list`.

    The entire list of page properties from the UX Page Property \[sys\_ux\_page\_property\] table opens.

2.  Select **New**.

3.  Complete the following fields:

    -   **Page**

        Select your workspace.

    -   **Name**

        Enter `confirmPopStateNavigationWhenDirty`.

    -   **Type**

        Select **true \| false**.

    -   **Value**

        Enter `true`.

4.  Select **Submit**.



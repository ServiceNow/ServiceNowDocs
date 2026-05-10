---
title: Configure role-based access to the Personalize Form menu
description: Configure which roles can access the Personalize Form menu.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure role-based access to the Personalize Form menu

Configure which roles can access the Personalize Form menu.

## Before you begin

Role required: admin

## About this task

The Personalize Form menu \(![](../image/icon-personalize-form.png)\) in the form header enables you to customize which fields display on the form. You can use the **glide.ui.personalize\_form\_role** system property to define which roles can access the Personalize Form menu.

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add a system property named **glide.ui.personalize\_form\_role**.

    For more information on adding a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

3.  In the Value field, enter a list of roles that can access the Personalize Form menu.

4.  Select **Submit**.



---
title: Hide the Personalize Form menu
description: Disable the Personalize Form menu by using the glide.ui.personalize\_form system property.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Hide the Personalize Form menu

Disable the Personalize Form menu by using the **glide.ui.personalize\_form** system property.

## Before you begin

Role required: admin

## About this task

The Personalize Form menu \(![](../image/icon-personalize-form.png)\) in the form header enables you to customize which fields display on the form. You can use the **glide.ui.personalize\_form** system property to disable the Personalize Form menu.

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add a system property named **glide.ui.personalize\_form**.

    For more information on adding a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

3.  Set the Value to **false**.

4.  Select **Submit**.



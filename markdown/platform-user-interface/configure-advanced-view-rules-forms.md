---
title: Configure advanced view rules for forms
description: Use client scripts to determine who can view a form variant in your workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure advanced view rules for forms

Use client scripts to determine who can view a form variant in your workspace.

## Before you begin

Role required: admin

## About this task

You can create page variants in UI Builder to display different versions of a page based on roles. If you need to switch views dynamically based on custom logic, then you can configure advanced view rules.

Advanced view rules enable you to define a client script that determines dynamically which variant to show at runtime. This configuration provides you with more flexibility than static, role-based access in UI Builder, enabling for complex conditions evaluated directly in your session.

## Procedure

1.  Navigate to `sysrule_view_workspace.list`.

    The entire list of view rules in the View Rules \[sysrule\_view\_workspace\] table opens.

2.  Select a workspace page variant.

3.  Select the **Advanced** check box.

4.  Toggle **Turn on ECMAScript 2021 \(ES12\) mode** to use the latest supported JavaScript features.

5.  In the Script field, enter a client script to define the conditions for switching views.

6.  Select **Update**.



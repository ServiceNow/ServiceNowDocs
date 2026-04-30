---
title: Enabling HTML sanitizer
description: The HTML sanitizer provides a property to enable or disable the sanitizer for all HTML fields in the system.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HTML sanitizer, Platform Security]
---

# Enabling HTML sanitizer

The HTML sanitizer provides a property to enable or disable the sanitizer for all HTML fields in the system.

## Before you begin

Role required: admin

## About this task

By default, the property is set to true for new instances.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Set the properties **glide.html.sanitize\_all\_fields** and **glide.translated\_html.sanitize\_all\_fields** to **true**.

    **Note:** To learn more about this property, see  in Instance Security Hardening Settings.

    If the properties do not exist in the System Properties table, you can add them.



---
title: Enable sanitization on individual fields
description: You can use field attributes to enable or disable the sanitizer on individual fields.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enabling HTML sanitizer, HTML sanitizer]
---

# Enable sanitization on individual fields

You can use field attributes to enable or disable the sanitizer on individual fields.

## Before you begin

Role required: admin

## About this task

You need to first set the sanitizer property to false, and then enable the sanitizer on a per-field basis for any form.

## Procedure

1.  Navigate to the sys\_properties table and set the **glide.html.sanitize\_all\_fields** to **false**.

    This disables the sanitizer for all HTML fields in the system.

2.  Navigate to the form that contains the HTML field.

3.  Right-click the HTML field label, and select **Configure Dictionary**.

    The Dictionary Entry form opens for the HTML field.

4.  Enter one of the following in the Attributes field:

    -   To disable sanitization enter `html_sanitize=false`
    -   To enable sanitization enter `html_sanitize=true`
5.  Click **Update**.

6.  To enable the HTML sanitizer for translated HTML fields, set the **glide.translated\_html.sanitize\_all\_fields** property is **true**.



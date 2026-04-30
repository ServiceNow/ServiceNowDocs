---
title: Validate HTML in journal fields
description: Prevent users from saving invalid HTML in a journal field.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Render journal field entries as HTML, Journal field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Validate HTML in journal fields

Prevent users from saving invalid HTML in a journal field.

## Before you begin

Role required: admin

## Procedure

1.  Add the property **glide.ui.allow\_deep\_html\_validation**.

    For instructions, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

2.  Set the **Value** to **true**.

3.  Click **Save**.

    Users now see a warning in the activity formatter when they enter invalid HTML code in a journal field.

    ![Invalid HTML message](../image/InvalidHTML.png)



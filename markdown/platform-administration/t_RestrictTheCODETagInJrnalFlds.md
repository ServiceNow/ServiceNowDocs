---
title: Restrict the CODE tag in journal fields
description: You can prevent journal fields from rendering HTML code by disabling support for the \[code\] tag.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Render journal field entries as HTML, Journal field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Restrict the CODE tag in journal fields

You can prevent journal fields from rendering HTML code by disabling support for the `[code]` tag.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Clear the check box for **Allow support for embedding HTML code by using the \[code\] tag** \(the **glide.ui.security.allow\_codetag** property\).

    **Note:** To learn more about this property, see Allow embedded HTML code \(instance security hardening\) in the Instance Security Hardening Settings.

3.  Click **Save**.



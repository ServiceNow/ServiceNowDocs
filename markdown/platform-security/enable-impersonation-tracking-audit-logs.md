---
title: Enable impersonation tracking in audit logs
description: Track users who perform actions through impersonation in audit logs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring auditing for a table, Auditing]
---

# Enable impersonation tracking in audit logs

Track users who perform actions through impersonation in audit logs.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  Select **New** on the form header.

3.  In the **Name** field, enter `glide.audit.track_impersonation`.

4.  In the **Value** field, enter `true`.

5.  Select **Submit**.


## Result

Impersonation tracking is enabled. The Sys Audits \[sys\_audit\] table will record both the impersonated user and the user ID of the user who actually performed the actions.

## What to do next

For information about converting the user ID to the actual user name, see [Map user IDs to user names in audit records](https://support.servicenow.com/kb?sys_kb_id=e77c760797ecba9024a7739c1253af4f&id=kb_article_view).


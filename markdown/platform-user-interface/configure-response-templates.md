---
title: Disable response templates
description: Disable response templates for journal fields.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Emails, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Disable response templates

Disable response templates for journal fields.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add a system property named **glide.ui.enable\_response\_templates**.

    For instructions on adding a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

3.  Set the Value to **false**.

4.  Select **Submit**.



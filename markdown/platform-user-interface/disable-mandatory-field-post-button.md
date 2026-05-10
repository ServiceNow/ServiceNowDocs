---
title: Configure the Post button to display continuously
description: Configure the Post button in the Activity stream to display and function continuously.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activity stream, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure the Post button to display continuously

Configure the **Post** button in the Activity stream to display and function continuously.

## Before you begin

The **Post** button disappears by default when the Comments or Work Notes fields are made mandatory by a UI Policy on the incident\_task table. You can configure the **Post** button to appear and function even when mandatory fields aren't filled.

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add the **glide.activity.compose.can\_post\_mandatory\_fields** system property.

    For more information on adding a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

3.  Set the Value to **true**.

4.  Select **Submit**.



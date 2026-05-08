---
title: Configure list record count to load in the background
description: Configure lists created from large tables to load the list record count in the background.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lists, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure list record count to load in the background

Configure lists created from large tables to load the list record count in the background.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add a system property named **glide.ui.fetch.list.record.count.asynchronously**.

    For more information on adding system property, see Add a system property.

3.  Set the Value to **true**.

4.  Select **Submit**.



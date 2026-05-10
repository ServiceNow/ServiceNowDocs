---
title: Configure global system properties to edit members in Healthcare Operations Core
description: A global system property must be configured to properly use the Edit Members functionality in Healthcare Operations Core.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add or remove members, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Configure global system properties to edit members in Healthcare Operations Core

A global system property must be configured to properly use the Edit Members functionality in Healthcare Operations Core.

## Before you begin

On occasion, newly added members won’t appear within the Selected panel when editing members in Healthcare Operations Core.

This issue is often caused by the limited number of items that are shown in the list collector.

To fix this issue, create a global system property with the name glide.xmlhttp.excessive, a type of integer, and a large number for the value limit based on the total number of users in the application.

Role required: admin

## Procedure

1.  Set your scope to **Global**.

2.  Navigate to **All** &gt; **System Properties**.

3.  Select **New**.

4.  Fill in the following fields:

    1.  Name - glide.xmlhttp.excessive
    2.  Type - integer
    3.  Value - Enter a high value here that represents the total potential number of users. For example, 10000.
5.  Select **Submit**.


## Result

The "Available" and "Selected" fields on the Edit Member table displays all available selections.


---
title: Configure pagination size for search lists
description: To configure the amount of search list results that load to the screen as the user scrolls down, add the system property glide.sg.choice\_list.window\_size.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure pagination size for search lists

To configure the amount of search list results that load to the screen as the user scrolls down, add the system property **glide.sg.choice\_list.window\_size**.

## Before you begin

Role required: admin

## About this task

By default, the mobile app returns 50 results at a time in a search list. Increasing the pagination size may cause the search request to take longer.

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Open the record for **glide.sg.choice\_list.window\_size** or create a new property if it does not exist.

3.  In the form, match the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.sg.choice\_list.window\_size**|
    |Type|integer|
    |Value|&lt;pagination-size&gt;|


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)


---
title: Configure time intervals for user presence
description: User presence shows that users are viewing a record sometimes after they have already left. The system only checks for user presence every two minutes by default. You can allow the system to check more frequently by configuring some system properties.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User presence, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure time intervals for user presence

User presence shows that users are viewing a record sometimes after they have already left. The system only checks for user presence every two minutes by default. You can allow the system to check more frequently by configuring some system properties.

## Before you begin

Role required: admin

## About this task

These properties control how often the system checks for updates or caches user presence.

-   glide.ui.presence.cache\_seconds
-   glide.ui.presence.time\_back\_minutes

You can configure each property to check more or less frequently. Checking more frequently might slow performance.

## Procedure

1.  Navigate to the system properties list by typing `sys_properties.list` in the navigation filter.

2.  Search for each of the properties to make sure they do not already exist in the list.

3.  Click **New**.

4.  To control how often the system checks for updates, configure the following property.

    |Field|Description|
    |-----|-----------|
    |Name|glide.ui.presence.time\_back\_minutes|
    |Type|integer|
    |Value|How often in minutes you want the system to check for user presence. The default number is 2.|

5.  To control how often the system caches logged in user information, configure the following property.

    |Field|Description|
    |-----|-----------|
    |Name|glide.ui.presence.cache\_seconds|
    |Type|integer|
    |Value|How often in seconds, the system caches the user presence information. The default number is 5.|

6.  Click **Submit**.


**Parent Topic:**[User presence](../concept/c_UserPresence.md)


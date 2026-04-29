---
title: Create the image search system property
description: Create and enable a system property to control access to image search on your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure photo search, Mobile photo search, Global search, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create the image search system property

Create and enable a system property to control access to image search on your instance.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator, type `sys_properties.list` to display the list of system properties for your instance.

2.  Click **New**.

3.  Fill in the system property form as needed.

    |Field|Value|
    |-----|-----|
    |Name|glide.sg.image\_recognition.search.enable|
    |Type|true \| false|
    |Value|true|

4.  Click **Submit**.

    Your instance is configured to use photo search. You can disable photo search on your instance at any time by deleting the property record or by setting the **Value** field to `false`.

    **Note:** Enabling this system property grants access to image search for all users.


## What to do next

Enable global search in your screen launcher to begin using photo search on your mobile applications. For details on enabling search on your screen launchers see [Enable global search in your screen launcher](sg-configure-alp-search.md).

**Parent Topic:**[Configure photo search](sg-configure-image-search.md)


---
title: Enable voice search
description: Enable your users to search for items, articles, and people using native speech recognition from an app on their mobile device.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Global search for mobile, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Enable voice search

Enable your users to search for items, articles, and people using native speech recognition from an app on their mobile device.

## Before you begin

Role required: admin

## About this task

**Warning:** Voice search uses native speech recognition and relies on your operating system's cloud server to transcribe voice into text search. If you have data privacy concerns about search queries moving to the operating system cloud server, do not turn on voice search.

## Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  Click **New** to add a new system property.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|Enter `glide.sg.voice_search.enabled`.|
    |Type|Select **true \| false**.|
    |Value|Enter `True`.|

4.  Click **Submit**.


## Result

The global search bar in the Now Mobile app includes a microphone icon. Users must select this icon and allow the app to access speech recognition on their mobile device to use voice search.


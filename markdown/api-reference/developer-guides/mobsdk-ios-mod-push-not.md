---
title: Modify the push notification
description: Modify the Virtual Agent Message Push Notification record to include your application. This record is used to trigger notifications to the Virtual Agent. All applications that will push notifications to the Virtual Agent must be configured in this record.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up push notifications on your ServiceNow instance, Configure push notifications, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Modify the push notification

Modify the Virtual Agent Message Push Notification record to include your application. This record is used to trigger notifications to the Virtual Agent. All applications that will push notifications to the Virtual Agent must be configured in this record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Notification** &gt; **Push** &gt; **Push Notifications**.

2.  Locate and open the push notification "Virtual Agent Message Push Notification".

    Ensure that the layout is set to the Advanced view. If not, switch to the Advanced view by selecting the associated link under **Related Links**.

3.  Select the **What it will contain** tab.

4.  In **Push Messages**, add the name of the push message record created in "Add a push notification message".

    ![Push Notification screen shot](../../image/mob_sdk-push-notification-screen.png)

5.  Select **Update**.



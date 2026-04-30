---
title: Retrieve the Firebase push server key
description: You must retrieve your unique Google Firebase push server key from your Firebase account so that you can associate it to your Mobile SDK applications that leverage push notifications.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up push notifications on your ServiceNow instance, Configure push notifications, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Retrieve the Firebase push server key

You must retrieve your unique Google Firebase push server key from your Firebase account so that you can associate it to your Mobile SDK applications that leverage push notifications.

## Before you begin

Role required: admin

You must already have a Firebase account set up. For information on how to create a Firebase account and download the corresponding SDK, refer to the [Google Firebase](https://firebase.google.com/) website.

## Procedure

1.  From your Firebase account, select the configuration gear next to the **Project Overview** link on the left navigation bar, and then select **Project settings.**

    ![Google Firebase configuration screen](../../image/mobsdk-firebase-config-screen.png)

2.  From the Project settings page, select the **Cloud Messaging** tab.

    ![Firebase Project setting - server key copy](../image/mobsdk-and-firebase_project_settings.png)

3.  Select and copy the Server key token.

    **Note:** For security purposes, this key has been blocked from view in the screen shot above; covered with "Key here".



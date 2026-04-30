---
title: Add a push application record
description: You must enter your Google Firebase Cloud Messaging server key in your push application record to use push notifications in a Mobile SDK application that leverages Virtual Agent and push notifications.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up push notifications on your ServiceNow instance, Configure push notifications, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Add a push application record

You must enter your Google Firebase Cloud Messaging server key in your push application record to use push notifications in a Mobile SDK application that leverages Virtual Agent and push notifications.

## Before you begin

Role required: admin

This record is stored in the Push Application \[sys\_push\_application\] table.

## Procedure

1.  Navigate to **System Notification** &gt; **Push** &gt; **Push Application**.

2.  Select **New** to add a new record.

3.  In the **Display Name** and **Name** fields, enter the name of your application.

4.  In the **Push** field, change the value from **REST API** to **Direct**.

5.  In the **Google** tab, paste your Google Firebase server key in the **API Key** field.

6.  Select **Submit**.



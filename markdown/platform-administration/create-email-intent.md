---
title: Create email intents
description: Create and define an email intent for analyzing and identifying the primary purpose for an inbound email. Understanding the email's intent helps guide the tone, context, and call-to-action for effective responses.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Configure email agentic workflows, Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create email intents

Create and define an email intent for analyzing and identifying the primary purpose for an inbound email. Understanding the email's intent helps guide the tone, context, and call-to-action for effective responses.

## Before you begin

Role required: sn\_notif\_agents.notification\_ai\_admin

## About this task

Follow the [General guidelines for creating and mapping an intent](../reference/guidelines-creating-intent.md)

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Email Intents**.

2.  Select **New**.

3.  On the form, fill in the fields.

    | | |
    |---|---|
    |Name|Name of the intent.|
    |Description|Brief description of the intent along with the goal of the intent.|
    |Active|Option that indicates that the configuration is active. The configuration is active by default.|
    |Conditions|The conditions on the inbound record that will be evaluated to fetch the list of intents available for an inbound email.|

    **Note:** The default action is executed if an email's intent cannot be matched to any specific custom intent, ensuring no request goes unaddressed.

4.  Select **Submit**.


## What to do next

[Create and associate actions for intent](create-actions-for-intent.md)


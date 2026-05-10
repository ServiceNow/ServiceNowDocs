---
title: Create a topic subscription
description: Subscribe to the topic in the ServiceNow AI Platform that you want respond to the incoming notification from the external system. By subscribing to the topic, the subscriber receives the notifications based on the topics that you subscribe to.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure API notifications, Configure, Telecommunications Service Operations Management]
---

# Create a topic subscription

Subscribe to the topic in the ServiceNow AI Platform that you want respond to the incoming notification from the external system. By subscribing to the topic, the subscriber receives the notifications based on the topics that you subscribe to.

## Before you begin

-   Make sure that the Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) application is installed with the ServiceNow AI Platform.
-   Create topics for the incoming notifications.

Role required: admin, sn\_api\_notif\_mgmt.subscription\_creator

## About this task

You subscribe to the available topics for the incoming notifications from the external system, based on the customer preference. You generate the callback URL to share with the customers. When a request from an external system hits the callback URL, it initiates the creation of an event in the Event Management application.

Additionally, you register the topic subscription to start receiving the incoming notifications. When you create a topic subscription, it creates a record in the Topic Subscription \[sn\_api\_notif\_mgmt\_subscription\] table. To learn more about the methods to query and manipulate records in the Topic Subscription, see [TopicSubscriptionUtilOOB - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/TopicSubscriptionUtilAPIScoped.md).

## Procedure

1.  **All** &gt; **Telecom API Notification** &gt; **Subscription**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_gcm_h11_5vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Topic

</td><td>

Topic that you want to subscribe.

</td></tr><tr><td>

CallbackURL

</td><td>

The callback URL that you’re sharing with the external system to capture the incoming notification. The URL is generated automatically when you select **Generate CallbackURL**.

</td></tr><tr><td>

Filter query

</td><td>

Encoded content query parameters from the topic. You can also modify the filter query. To learn more about the query parameters that follow the TMF 688 standards, see [TM Forum](https://www.tmforum.org/).

</td></tr><tr><td>

Registration status

</td><td>

Status of the Topic registration with the external system. By default, it’s **Unregistered**. If the process is successful, the field value changes to **Registered**. Otherwise it’s **Error**.

</td></tr><tr><td>

Registration message

</td><td>

Registration status message from the external system.

</td></tr><tr><td>

Subscription id

</td><td>

Unique subscription id from the external system.

</td></tr></tbody>
</table>4.  Get the callback URL by selecting **Generate CallbackURL**.

5.  Register the subscription by selecting **Register**.


## Result

A trigger definition is created for the callback URL and the topic is registered to the external system.

## What to do next

In the Workflow Studio, you activate the endpoints of the Telecommunications Alarm Management Open API connection. For more information, see [Activate the endpoint of the Telecommunications Alarm Management Open API connection](activate-endpoint-in-the-telecommunications-alarm-management-open-api.md).


---
title: Create a topic
description: Create a topic and publish the incoming notifications from the external system to the topic. By creating the topics, subscribers can select the topics to which they want to subscribe.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure API notifications, Configure, Telecommunications Service Operations Management]
---

# Create a topic

Create a topic and publish the incoming notifications from the external system to the topic. By creating the topics, subscribers can select the topics to which they want to subscribe.

## Before you begin

Make sure that the Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) application is installed with the ServiceNow AI Platform.

Role required: admin, sn\_api\_notif\_ mgmt.topic\_creator

## About this task

You can create topics either by manually typing the external message details or automatically collecting the available topics from the external system. When you create a topic, it creates a record in the Topic \[sn\_api\_notif\_mgmt\_topic\] table.

## Procedure

1.  **All** &gt; **Telecom API Notification** &gt; **Topics**.

2.  Select **New**.

    If you’ve integrated with an external system, you can select **Get Topics** to get the available topics automatically. This action triggers the Event Alarm Notification API subflow. To learn more about the functions that enable you to query and manipulate records in the topic, see TopicUtilOOB - Scoped.

3.  On the form, fill in the fields.

<table id="table_gcm_h11_5vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Topic id

</td><td>

Unique topic id.

</td></tr><tr><td>

Topic name

</td><td>

Name of the topic.

</td></tr><tr><td>

Type

</td><td>

Type of topic. Select one from the following:-   Ingress: Option for inbound notification.
-   Egress: Option for outbound notification.


</td></tr><tr><td>

Header query

</td><td>

Encoded header query parameters. To learn more about the query parameters that follow the TMF 688 standards, see the [TM Forum](https://www.tmforum.org/).

</td></tr><tr><td>

Content query

</td><td>

Encoded content query parameters. To learn more about the query parameters that follow the TMF 688 standards, see [TM Forum](https://www.tmforum.org/).

</td></tr><tr><td>

Description

</td><td>

A brief description about the topic.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

A topic is created.

## What to do next

You can create the topic subscription according to the customer requirement. For more information, see [.](create-subscription-api-notification.md)


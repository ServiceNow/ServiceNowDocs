---
title: Duplicate and publish Virtual Agent Lite topics
description: Copy and publish a pre-built ITSM Virtual Agent Lite topic to deploy it to your users.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-12"
reading_time_minutes: 1
keywords: [Duplicate, copy, publish, Virtual Agent, Lite, topic, ITSM, IT Service Management]
breadcrumb: [Virtual Agent Lite, Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Duplicate and publish Virtual Agent Lite topics

Copy and publish a pre-built ITSM Virtual Agent Lite topic to deploy it to your users.

## Before you begin

[Preview \(test\) the pre-built ITSM Virtual Agent Lite topics](test-valite-topic.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  In the topic that you've tested, select **Duplicate** in the triple-dot icon on the Virtual Agent Designer header bar.

    1.  In the pop-up window, enter the name of your duplicated topic.

    2.  Select **Save**.

    The **Topic Properties** page \(**Properties** tab\) for your duplicated topic opens.

    **Note:** You can duplicate a pre-built topic but you can't duplicate a copy of a pre-built topic.

2.  Change these property fields as needed:

    |Property|Description|
    |--------|-----------|
    |Description|A brief explanation of the topic.|
    |Keywords|A word or phrase that is associated with and activates the topic. You can add, change, or delete keywords.|
    |Roles|Roles that an end user must have to view and run the topic. If a topic is public \(available to users, including guest users, who are not authenticated in ServiceNow\), select only the Public role.|

3.  Select **Save**, and then select the triple-dot icon followed by **Publish**, to make the topic active and available in your chat clients.


## Result

When your users run Virtual Agent, the chat client displays the published topics in the topic selection menu. If there are three or fewer topics available to the user, the menu items \(topics\) are displayed as buttons.

For example, in the Microsoft Teams integration, the topic selection menu displays these three topics as buttons.

![Microsoft Teams conversation showing a welcome message with topic choices and asking to type hi to if you need further help.](../images/va-lite-msteams.png "Topic choices in the Microsoft Teams channel")


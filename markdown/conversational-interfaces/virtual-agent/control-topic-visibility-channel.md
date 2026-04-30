---
title: Control topic visibility in Virtual Agent messaging channels
description: Suppress the display of a topic in a Virtual Agent messaging channel by using a condition script that excludes the topic from a channel.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-10-24"
reading_time_minutes: 1
breadcrumb: [Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Control topic visibility in Virtual Agent messaging channels

Suppress the display of a topic in a Virtual Agent messaging channel by using a condition script that excludes the topic from a channel.

## Before you begin

Roles required:

-   virtual\_agent\_admin or admin
-   Administrator for third-party applications

## About this task

In your condition script for the topic, use a context variable to identify the messaging channel that excludes this topic.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the home page, select the topic for updating or create a new topic.

3.  In the **Condition** field on the Topic Properties page, enter a condition script that identifies the messaging channel \(Slack, Microsoft Teams, Workplace from Facebook, or Facebook Messenger\) from which the topic will be excluded.

    You can use the following example script, which contains the **vaContext.deviceType** variable, to identify the messaging channel that excludes the topic: Slack, Microsoft Teams, Workplace, and Facebook Messenger.

    ```
    (function execute()
    { if(vaContext.deviceType === 'Slack' || vaContext.deviceType === 'Teams' || vaContext.deviceType=='Facebook' || vaContext.deviceType=='Messenger'){
    return false;
    }
    return true;
    })()
    ```

4.  To save the topic properties, click **Save**.


## Result

Publishing the topic deploys it to the Virtual Agent messaging channels, except for the Virtual Agent channels that you specified in the topic condition script. A keyword or an intent \(if using NLU\) does not trigger the topic.

**Parent Topic:**[Virtual Agent integration with messaging apps](../concept/va-integration-messaging-apps.md)


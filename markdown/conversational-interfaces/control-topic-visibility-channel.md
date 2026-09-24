---
title: Control topic visibility in Virtual Agent messaging channels
description: Suppress the display of a topic in a Virtual Agent messaging channel by using a condition script that excludes the topic from a channel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/control-topic-visibility-channel.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Integrate VA with messaging apps, Conversational Integration apps for Virtual Agent, Conversational Interfaces]
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

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  Select the topic for updating or create a new topic.

4.  Navigate to the **Properties** page, and open **Who can access this topic** under Advanced properties.

5.  In the Context section, select **Condition** followed by **Add Condition**.

6.  Enter a condition script that identifies the messaging channel \(Slack or Microsoft Teams\) from which the topic will be excluded.

    You can use the following example script, which contains the **vaContext.deviceType** variable, to identify the messaging channel that excludes the topic:

    ```
    (function execute()
    { if(vaContext.deviceType === 'Slack' || vaContext.deviceType === 'Teams'){
    return false;
    }
    return true;
    })()
    ```

7.  To save the topic properties, click **Save**.


## Result

Publishing the topic deploys it to the Virtual Agent messaging channels, except for the Virtual Agent channels that you specified in the topic condition script.

**Parent Topic:**[Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integration-messaging-apps.md)


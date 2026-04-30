---
title: Customize a default callback topic
description: Customize the default callback topics as per your requirements.
locale: en-US
release: xanadu
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Omnichannel Callback, Omnichannel Callback, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Customize a default callback topic

Customize the default callback topics as per your requirements.

## Before you begin

Role required: admin

## About this task

You can customize one of the following default callback topics: Callback-Phone for voice channels and Callback-General for messaging or chat channels. The following procedure explains how to customize the Callback-Phone topic.

## Procedure

1.  Duplicate the Callback-Phone topic from the Virtual Agent Designer.

    For more information on how to duplicate a topic, see [Duplicate a Virtual Agent topic](https://www.servicenow.com/docs/access?context=duplicate-virtual-agent-topic&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

2.  In the Advanced properties section of the **Properties** tab, select the voice channel that you want to associate with the custom callback topic.

3.  On the **Flow** tab, modify the default callback flow and set the following properties in the Script action utility, if required.

    1.  Set Global Callback Executed \(vaVars.global\_callback\_executed\) to **true**.

    2.  Set No Agent Available \(vaVars.global\_show\_no\_agent\_available\_msg\) to **false**.

    3.  Set the following properties in the Create Callback Task node.

        -   Set Global Callback Executed \(vaVars.global\_callback\_executed\) to **true**.
        -   Set No Agent Available \(vaVars.global\_show\_no\_agent\_available\_msg\) to **false**.
        -   Callback Number \(callback\_number\): Required field to be populated with the number on which the user requested a callback. This number may be the number that the user is calling from or the dialed number.
        -   Short description \(short\_description\): User issue description.
        -   Initial Interaction \(initial\_interaction\): Interaction detail from which the callback task has been initiated.
        -   Max Retry Attempts \(max\_retry\_Attempts\): Maximum retry attempts after which the callback task is closed.
        -   Expire Time \(expire\_time\): Callback timeout after which the callback task is closed.
        -   Messaging Channel \(messaging\_channel\): Messaging channels configured for use. If not provided, the default callback channel is used.
        -   Scheduled \(scheduled\): Set to **true** to make the callback task eligible for auto callback.
4.  Save and publish your custom callback topic by clicking **Save** and **Publish**.

5.  Map the custom callback topic to the voice service provider.

    1.  Fetch the sys\_id of your custom callback topic from the Topics \[sys\_cs\_topic\] table.

    2.  Select your voice service provider from the Provider Channel Identities \[sys\_cs\_provider\_application\] table.

    3.  On the **Provider Identity Properties** tab, update the value of the **callback\_topic\_id** property with the sys\_id of your custom callback topic and click **Update**.



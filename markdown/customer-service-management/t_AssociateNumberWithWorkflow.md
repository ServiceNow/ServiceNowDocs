---
title: Associate a phone number with a workflow
description: You can associate a Notify phone number with a workflow.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CTI demo implementation, Integrating with Computer Telephony Integration \(CTI\), Integrating Customer Service Management with other applications, Customer Service Management]
---

# Associate a phone number with a workflow

You can associate a Notify phone number with a workflow.

## Before you begin

You must create a Twilio Voice account and configure Notify with Twilio Voice before you can associate a phone number with a number group and workflow.

A number group allows you to group Notify phone numbers and then share workflows across grouped numbers. For each number group, you can specify a workflow for incoming and outgoing calls.

The CTI Softphone demo data includes these sample workflows:

-   Call Center, for use with the Customer Service Management application
-   Call Center for Incident Management

The Call Center workflow uses several Notify workflow activities that determine workflow functionality. Each activity performs a different task, such as playing a message greeting or creating a list of user input options. Activities can succeed or fail, which can result in actions performed by other activities.

You can use the default Call Center workflow or modify this work flow as needed.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Numbers**.

2.  From the Notify Phone Numbers list, click the phone number that you want to edit.

3.  Select a **Notify Group** that uses the incoming call workflow that you want to handle this phone number.

    The CTIDemo group uses the Call Center workflow for incoming calls.

4.  Click **Update**.


**Related topics**  


[Numbers and number groups](https://www.servicenow.com/docs/access?context=c_NumberGroups&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Configure Notify with\\n Twilio](https://www.servicenow.com/docs/access?context=t_ConfigureNotifyWithTwilio&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)


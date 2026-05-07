---
title: Associate Amazon Connect queues for CSM to a ServiceNow instance
description: Set up phone queues for Amazon Connect to gain visibility into the queues using Workforce Optimization for Customer Service.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Voice, Channel Management, Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Associate Amazon Connect queues for CSM to a ServiceNow instance

Set up phone queues for Amazon Connect to gain visibility into the queues using Workforce Optimization for Customer Service.

## Before you begin

Enable the Advanced Work Assignment plugin \(com.glide.awa\) to create the Amazon Connect queues. You must activate this plugin before you activate the Cloud Call Center Core \(sn\_cti\_core\) plugin so that you can successfully integrate the two applications.

After you [Install ServiceNow Voice applications](https://www.servicenow.com/docs/access?context=install-ccc-apps&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US), when you enable the Advanced Work Assignment plugin \(com.glide.awa\), the Amazon Connect \(phone\) service channel appears in the Workforce Optimization for Customer Service.

Role required: sn\_csm\_wfo\_workspa.admin and sn\_cti\_amzn\_cct.admin

## About this task

After an agent completes a call, using Workforce Optimization for Customer Service, you can learn:

-   Who was on hold and how long they were on hold
-   How long calls are taking
-   Which agents are available and when
-   How many agents are available and what is their current utilization

You can see the Basic queue when you install the demo data with the sample contact flow:

|Calls get routed to this queue|When|
|------------------------------|----|
|Basic Queue|An utterance is generic, such as, "I want to talk to an agent."|
|VIP Queue|A user who has the VIP field enabled calls Support.|
|IT Equipment Support|An utterance includes IT equipment support or hardware issues.|
|Application Support|An utterance includes application support.|

For example, the Basic queue is available when you install the demo data to get the calls routed to this queue when an utterance is generic, such as, "I want to talk to an agent".

A routing profile links queues to agents. Every agent must have a routing profile in the Amazon Connect instance that is integrated with the ServiceNow instance. For more information, see [create a routing profile](https://docs.aws.amazon.com/connect/latest/adminguide/routing-profiles.html).

**Note:**

-   You can associate each profile with multiple Amazon Connect agent queues.
-   You must [associate](https://docs.aws.amazon.com/connect/latest/adminguide/transfer-to-agent.html) each of these agent queues with the corresponding agent queue in your ServiceNow instance using an Amazon Connect ARN number. This association enables you to report on queue statistics and call metrics within Workforce Optimization for Customer Service.

## Procedure

1.  Create placeholder queues for an Amazon Connect \(phone\) service channel if you need additional queues.

    For more information on creating the queue, refer to [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

    **Note:** Do not add work item routing conditions when you create the placeholder queues.

2.  Associate the ServiceNow Advanced Work Assignment \(AWA\) queue record with the Amazon Web Services \(AWS\) queue ARN.

    1.  In the Amazon Connect instance, navigate to **Routing** &gt; **Queues**.
    2.  Select a queue.
    3.  Copy the ARN for the queue.
    4.  In the ServiceNow instance, navigate to **Advanced Work Assignment** &gt; **Queues** and select the corresponding queue.
    5.  In the **Cloud Call Center Source ID** field, enter the ARN number.
    6.  Click **Update**.
    7.  Repeat these steps for each queue.
3.  Add assignment groups to a queue.

    1.  Select a work item queue.
    2.  Click **Group Queue Priorities** related list.

        **Note:** You must configure the form to display this related list.

    3.  Click **New**.
    4.  In the **Group** field, add an assignment group that include agents who can handle this queue.
    5.  In the **Order** field, select the order number for the assignment group. This is the order of assignment group priority in which the incoming calls are handled.
    6.  Click **Submit**.

**Parent Topic:**[Using Voice with Workforce Optimization for Customer Service](../concept/configurable-servicenow-voice-cs.md)


---
title: Claim a Phone number
description: Claim a Phone number to set up IVR \(Interactive Voice Response\).
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring your AWS account for use with Conversational IVR, Integrating Virtual Agent with Conversational IVR, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Claim a Phone number

Claim a Phone number to set up IVR \(Interactive Voice Response\).

## Before you begin

Role required: admin

## Procedure

1.  Log into your AWS Console and look for the Amazon Connect Instance you created.

2.  Log in as an administrator into your Amazon Connect instance.

3.  Navigate to **Channels** &gt; **Phone numbers** and click **Claim a number**.

4.  On the Claim Phone number form, select either the **Toll free** Country or the **DID \(Direct Inward Dialing\)** Prefix and select the number.

5.  Claim a phone number to the SN\_CI\_CC\_Inbound\_Contact\_Flow from the Phone numbers section in the navigator.

6.  Provide a description of your choice in the **Description** field, select SN\_CI\_CC\_Inbound\_Contact\_Flow from the **Contact flow / IVR** drop-down, and click **Save**.

    After the number is published, customers can make a call and start conversations with the Virtual Agent.

7.  Navigate to **Routing** &gt; **Queues** and select **BasicQueue**.

8.  On the Edit BasicQueue page, under Settings, specify a name for **Default caller ID name**.

9.  For the **Outbound caller ID number**, select the Phone number you claimed in Step 4.

10. Select **SN\_CI\_CC\_Outbound\_Contact\_Flow** for the **Outbound whisper flow**.

11. Click **Save**.


## What to do next

Invoke an automated caller interaction with bots to fulfill the caller's request within the ServiceNow instance. For more information, see [Configure a contact flow for an automated caller interaction](https://www.servicenow.com/docs/access?context=establish-automated-bot-interactions&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).


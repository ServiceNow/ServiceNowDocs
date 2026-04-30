---
title: Generate Webhook URL
description: Define a Webhook registry for generating the Webhook URL. Urjanet uses the Webhook URL to send real time data to the ESG Management application when an Urjanet statement data is either generated or modified.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Urjanet, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Generate Webhook URL

Define a Webhook registry for generating the Webhook URL. Urjanet uses the Webhook URL to send real time data to the ESG Management application when an Urjanet statement data is either generated or modified.

## Before you begin

Role required: sn\_esg.admin

## About this task

A statement in Urjanet refers to a bill. Whenever a new statement is generated in Urjanet, using the defined Webhook, the ESG Management application is notified about the new statement generation and the data is fetched into the ESG Management application without any manual intervention.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Urjanet** &gt; **Webhook Registry**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the registry.|
    |Path|Resource path of the Scripted REST API to be used for inbound Urjanet API calls. This field is automatically set to **api/sn\_esg\_urjanet/webhook**.|

4.  Select **Submit**.

5.  Open the record that you created and select **Generate Webhook URL**.

6.  To copy the Webhook URL, right-click the information message that appears on the screen and select **Copy Link Address**.![Copying the Webhook URL.](../images/webhook-url.png)


## What to do next

Paste the URL that is generated in the Urjanet console to get real-time Urjanet statement data. For more information, contact your system administrator.

**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with Urjanet](../concept/integrating-esg-management-with-urjanet.md)


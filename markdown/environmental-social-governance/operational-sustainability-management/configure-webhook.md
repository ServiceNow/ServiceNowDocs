---
title: Generate Webhook URL
description: Define a Webhook registry for generating the Webhook URL. Urjanet uses the Webhook URL to send real time data to the Operational Sustainability Management application when an Urjanet statement data is either generated or modified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/operational-sustainability-management/configure-webhook.html
release: australia
product: Operational Sustainability Management
classification: operational-sustainability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with Urjanet, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Generate Webhook URL

Define a Webhook registry for generating the Webhook URL. Urjanet uses the Webhook URL to send real time data to the Operational Sustainability Management application when an Urjanet statement data is either generated or modified.

## Before you begin

Role required: sn\_esg.admin

## About this task

A statement in Urjanet refers to a bill. Whenever a new statement is generated in Urjanet, using the defined Webhook, the Operational Sustainability Management application is notified about the new statement generation and the data is fetched into the Operational Sustainability Management application without any manual intervention.

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

6.  To copy the Webhook URL, select and hold \(or right-click\) the information message that appears on the screen and select **Copy Link Address**.\[Omitted image "webhook-url.png"\] Alt text: Copying the Webhook URL.


## What to do next

Paste the URL that is generated in the Urjanet console to get real-time Urjanet statement data. For more information, contact your system administrator.

**Parent Topic:**[Integrating Operational Sustainability Management \(formerly ESG\) with Urjanet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/integrating-esg-management-with-urjanet.md)


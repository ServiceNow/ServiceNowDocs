---
title: Create a SAP Concur webhook registry
description: Create a webhook registry to be notified whenever a trip is either created or modified in SAP Concur.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with SAP Concur, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a SAP Concur webhook registry

Create a webhook registry to be notified whenever a trip is either created or modified in SAP Concur.

## Before you begin

Role required: sys\_admin

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **SAP Concur** &gt; **Webhook Registry**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the registry. For example, `ESG integration`.|
    |Path|This field is automatically set.|
    |Token|Select a token.|

4.  Right click the form header and select **Save**.

5.  Select **Callback URL**.

6.  Copy the URL that is generated.

7.  Select **Submit**.


-   **[Create a webhook subscription](create-webhook-subscription.md)**  
Webhooks are used to simplify communication between two applications. Create a webhook subscription to connect to Concur through webhook.

**Parent Topic:**[Integrating Operational Sustainability Management \(formerly ESG\) with SAP Concur](../concept/integrate-esg-with-concur.md)


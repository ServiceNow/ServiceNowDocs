---
title: Add an Agent Client Collector \(ACC\) connection
description: Block and unblock AI usage on managed devices by configuring Agent Client Collector \(ACC\) as a control enforcement point.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configure-acc-cep.html
release: zurich
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Agent Client Collector, ACC, control enforcement point, Policies]
breadcrumb: [Configuring security connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add an Agent Client Collector \(ACC\) connection

Block and unblock AI usage on managed devices by configuring Agent Client Collector \(ACC\) as a control enforcement point.

## Before you begin

Confirm the following:

-   The Agent Client Collector \(ACC\) agent is deployed to the devices you want covered. For details, see [Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/acc-landing-page.md).
-   Devices with the deployed ACC agent can connect to your ServiceNow instance through a MID server or a proxy.
-   If ACC is already installed and in use, confirm agents are reporting data on the **ACC Agent health dashboard**.

Role required: sn\_ai\_governance.ai\_steward

## About this task

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Control enforcement points**.

2.  On the **Available connectors** tab, select **ACC**.

3.  Enter a name for this connection.

4.  Confirm the **Domain** field.

5.  Select a **Connection Alias**.

6.  Activate the connector by selecting **Active**.

7.  Select **Submit**.


## Result

The connection is created and appears on the **Established connections** tab.

## What to do next

ACC is configured as an control enforcement point for explicit block policies. For details, see [Create an Explicit Block policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-create-explicit-block-policy.md).

**Parent Topic:**[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-security-connections.md)


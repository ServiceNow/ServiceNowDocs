---
title: Connect Agent Client Collector to detect AI use
description: View the full content of AI requests sent from managed devices, including prompts and attachments by configuring the Agent Client Collector \(ACC\) Shadow AI connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/sh-ai-connect-acc.html
release: zurich
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [Agent Client Collector, ACC, connector, Shadow AI]
breadcrumb: [Configure, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Connect Agent Client Collector to detect AI use

View the full content of AI requests sent from managed devices, including prompts and attachments by configuring the Agent Client Collector \(ACC\) Shadow AI connector.

## Before you begin

Confirm the following:

-   The Agent Client Collector \(ACC\) agent is deployed to the devices you want covered. For details, see [Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/acc-landing-page.md).
-   Devices with the deployed ACC agent can connect to your ServiceNow instance through a MID server or a proxy.
-   If ACC is already installed and in use, confirm agents are reporting data on the **ACC Agent health dashboard**.

Role required: sn\_ai\_governance.ai\_steward

## About this task

ACC runs on the device itself, so it can see the full content of an AI request, including prompts and attachments, before that content is encrypted for transmission. For details on detection methods, see [How Shadow AI detects unsanctioned AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-how-detection-works.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Connectors**.

2.  Select the **Agent Client Collector** connector.

3.  Review the getting started details.

4.  Select the **Active** check box.

5.  Select **Save**.

    ACC appears under **Established connections**, with its connection state and processing state.


## What to do next

The ACC connection appears on the **Established connections** tab. If the connection is active but no detections appear, view the processing state to determine whether data is actually flowing. Start reviewing services and traffic detected by ACC in the Shadow AI overview. For details, see [Shadow AI overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-overview.md).


---
title: Connect Armis to detect AI use
description: Detect AI-related network traffic without requiring software on employee devices by configuring the Armis Shadow AI connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/sh-ai-connect-armis.html
release: zurich
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [Armis, connector, Shadow AI]
breadcrumb: [Configure, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Connect Armis to detect AI use

Detect AI-related network traffic without requiring software on employee devices by configuring the Armis Shadow AI connector.

## Before you begin

Confirm the following requirements are active or already in place:

-   An active Armis Centrix instance
-   An Armis API secret key
-   Armis ServiceNow \(Pull\) integration
-   Active Traffic-Inspection integration \(SPAN/TAP\)
-   Outbound HTTPS access \(port 443\)

If you're new to Armis, see [Shadow AI: Add Armis Connector for AI Control Tower \[KB3151375\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3151375).

If you already have Armis, see [Shadow AI: Add Armis Connector for AI Control Tower \[KB3144073\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144073).

Role required: sn\_ai\_governance.ai\_steward

## About this task

Armis identifies AI-related network traffic without requiring an agent on the endpoint, which gives it reach across any device that touches your network, including devices your organization doesn't manage. For each detection it reports the device, the correlated user, the destination, and the volume of traffic that moved. For details on detection methods, see [How Shadow AI detects unsanctioned AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-how-detection-works.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Connectors**.

2.  Select the **Armis** connector.

3.  Review the getting started details.

4.  Create an Armis connection alias.

    1.  Select the link to create a connection alias.

    2.  In the form that appears, enter your Armis tenant URL and the API secrets key you generated in Armis.

    3.  Select **Save**.

5.  Return to the Add Armis page in AI Control Tower, and select your **Armis connection alias** from the dropdown.

6.  Select the **Active** check box.

7.  Select **Save**.

    Armis appears under **Established connections**, with its connection state and processing state.


## What to do next

The Armis connection appears on the **Established connections** tab. If the connection is active but no detections appear, view the processing state to determine whether data is actually flowing. Start reviewing services and traffic detected by Armis in the Shadow AI overview. For details, see [Shadow AI overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-overview.md).


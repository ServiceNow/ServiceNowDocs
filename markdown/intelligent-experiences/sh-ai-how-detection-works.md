---
title: How Shadow AI detects unsanctioned AI use
description: Learn how each detection method observes AI usage, so you know which signals to expect on a detected AI service's record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-how-detection-works.html
release: australia
topic_type: concept
last_updated: "2026-08-20"
reading_time_minutes: 4
keywords: [Armis, Agent Client Collector, detection methods]
breadcrumb: [Explore, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# How Shadow AI detects unsanctioned AI use

Learn how each detection method observes AI usage, so you know which signals to expect on a detected AI service's record.

Shadow AI relies on multiple independent detection methods, including Armis and Agent Client Collector \(ACC\), and each observes AI usage from a different vantage point. Knowing which method detected a service tells you which signals are available on the service record. See [Detected AI service overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-service-overview.md) and [Detected AI service details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-service-details.md).

## Network-based detection with Armis

Armis observes traffic across your network, identifying AI-related domains and API calls without requiring any software on the endpoint device. This gives Armis the widest reach of any detection method: it detects AI use on any device that touches your network, including contractor laptops, personal devices, and other endpoints your organization doesn't manage and can't deploy an agent to. For each detection, Armis reports the device, the user it correlates to, the destination, and the volume of traffic that moved.

Armis refreshes its data hourly, but it counts usage once per device per AI service per day: if a device visits the same service multiple times in one day, Armis still reports a single event for that device. Repeated visits from the same device on the same day aren't reflected in the event count.

## Endpoint-based detection with ACC

ACC runs as an agent on the device itself, inspecting application traffic before that traffic is encrypted for transmission. On each device where the agent is deployed, this lets ACC report the content of a request alongside its usage signals: the prompt sent, any attachments included, and the model called.

For details, see [Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/acc-landing-page.md).

## What each method reports

Each method observes from a different point in the path a request takes, contributing signals that vary by method. Connecting more than one gives you the widest coverage and the most detailed signals together.

<table id="table_sh_ai_detection_comparison"><thead><tr><th>

Detection method attributes

</th><th>

Armis

</th><th>

ACC

</th></tr></thead><tbody><tr><td>

How you get it

</td><td>

Tenant creation required for new installs, and a connection to your ServiceNow instance is required to gather user data

</td><td>

Agent push installation required on each endpoint

</td></tr><tr><td>

How it's deployed

</td><td>

Physical appliance deployed in-network, or a virtual machine

</td><td>

Deployed on end-user managed devices

</td></tr><tr><td>

Data source

</td><td>

Direct network traffic

</td><td>

Direct traffic from the endpoint

</td></tr><tr><td>

Device coverage

</td><td>

Any device that connects to your network, including devices your organization doesn't manage

</td><td>

Each device where the agent is deployed

</td></tr><tr><td>

Endpoint requirement

</td><td>

None

</td><td>

Agent deployed to each device you want covered

</td></tr><tr><td>

Common signals collected

</td><td>

-   Users and departments
-   Devices
-   AI service category, such as conversation, software development, direct API or developer integration, or content creation
-   MCPs and APIs
-   Models used by the AI service
-   Sources, such as browsers, extensions or plugins, software, or the command line
-   Data volume sent by users, based on output payload size

</td><td>

-   Users and departments
-   Devices
-   AI service category, such as conversation, software development, direct API or developer integration, or content creation
-   MCPs and APIs
-   Models used by the AI service
-   Sources, such as browsers, extensions or plugins, software, or the command line
-   Data volume sent by users, based on output payload size

</td></tr><tr><td>

Traffic signals

</td><td>

Destination and traffic volume, observed at the network layer

</td><td>

Request size and the model called, read on the device

</td></tr><tr><td>

Request content

</td><td>

Observed as encrypted traffic in transit

</td><td>

Prompt text and attachments, read before encryption

</td></tr><tr><td>

Unique collected

</td><td>

Events aggregated by day

</td><td>

-   Individual events, not daily aggregates
-   Attachment types sent by end users
-   User inputs \(prompts\), grouped by conversation

</td></tr><tr><td>

Can't collect

</td><td>

-   Whether AI use is for cloud or on-premises code, general work, or personal desktop use
-   Whether an account is a corporate account or a personal account
-   Use of local models

</td><td>

-   Whether AI use is for cloud or on-premises code, general work, or personal desktop use
-   Whether an account is a corporate account or a personal account
-   Use of local models

</td></tr><tr><td>

Reporting cadence

</td><td>

Hourly, at the device and host level

</td><td>

Per request, as it happens

</td></tr><tr><td>

Policies

</td><td>

Not yet an enforcement point; no policies can be created

</td><td>

Can block specific end users, or block the service entirely

</td></tr></tbody>
</table>When more than one method detects the same service, Shadow AI treats it as a single entry, and its record combines the signals each method contributes.

Connecting more than one method fills in what any single method can't see on its own.

-   Connect Armis to catch a service running on devices that don't have an agent installed. See [Connect Armis to detect AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-connect-armis.md).
-   Deploy the ACC agent to the devices using a service to see its content: the prompts, attachments, and model called. See [Connect Agent Client Collector to detect AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-connect-acc.md).


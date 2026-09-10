---
title: Exploring Shadow AI in AI Control Tower
description: Learn how AI Control Tower detects unsanctioned AI use through Shadow AI connectors, and how detected AI services sit alongside your governed AI asset inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/sh-ai-exploring.html
release: zurich
topic_type: concept
last_updated: "2026-08-20"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI, explore]
breadcrumb: [Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Exploring Shadow AI in AI Control Tower

Learn how AI Control Tower detects unsanctioned AI use through Shadow AI connectors, and how detected AI services sit alongside your governed AI asset inventory.

## Shadow AI overview

Employees adopt AI faster than IT and security operations can evaluate and approve it. For example, ChatGPT use in a browser or desktop software, a new AI feature in an approved app, or a developer-built agent calling an LLM API directly can each result in data leaving your organization through a channel that nobody reviewed.

Shadow AI addresses this by detecting AI-related traffic across your network and managed devices, before it becomes a security incident or a compliance finding. Detected services appear in a dedicated staging area for Shadow AI, separate from your governed AI asset inventory, where you can take action to clear or block usage.

-   Get visibility into AI use your organization never approved, without waiting for it to show up as an incident.
-   Detect AI usage through multiple independent methods, from network traffic to endpoint activity.
-   See who's using a detected service and how heavily, before deciding whether it's actually a risk.
-   Triage a detection by clearing it, blocking access, or leaving it running while you investigate further.

## Shadow AI users

|User|Description|
|----|-----------|
|AI steward|Connects detection sources, reviews detected AI traffic, and decides how to respond: clearing a low-risk finding, blocking access, or leaving a service under review while investigating further. Manages which domains the AI services registry treats as AI-related.|
|System administrator|Activates the Shadow AI plugin as part of AI Control Tower setup, before an AI steward can connect a detection source.|

## How Shadow AI works

Detecting and triaging unsanctioned AI use happens in three stages.

-   **Configuration**

    An AI steward connects one or more detection sources, such as Armis or Agent Client Collector \(ACC\).

-   **Discovery**

    Each connected source reports AI-related activity into a shared staging area. The same service detected by more than one method is deduplicated and appears once, not twice.

-   **Staging and triage**

    Detected services surface on the Shadow AI overview and on their own individual records, where an AI steward reviews activity and takes action.


See [How Shadow AI detects unsanctioned AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-how-detection-works.md) for details on what each detection method reports.

## Shadow AI workflow

The following infographic shows how an AI steward and a system administrator work together to detect and act on unsanctioned AI use.

\[Omitted image "mmasset0022395-shadow-ai-in-ai-control-tower-vertical.svg"\] Alt text: Infographic showing Shadow AI configuration, review, and actions taken by the AI steward. For details, refer to the following description.

In this workflow:

1.  The system administrator activates the Shadow AI plugin.
2.  The AI steward configures one or more Shadow AI connectors to detect AI traffic, such as Armis or ACC.
3.  Each detection method gathers AI-related traffic and reports it in the Shadow AI staging area in AI Control Tower.
4.  The AI steward reviews detected traffic in the Shadow AI overview, by service, user, or department.
5.  The AI steward opens a specific service's record to see who's using it and how.
6.  Based on what the record shows, the AI steward clears the detection, blocks access for all users or only specific ones, or leaves it under review.
7.  The AI steward manages the registry to keep detection focused on what the organization actually wants tracked.

## Where Shadow AI fits in the inventory

Shadow AI is a discovery capability inside its own separate triage area, distinct from your governed AI asset inventory. Shadow AI traffic doesn't populate your AI asset inventory. Instead, it uses separate tables so your AI asset inventory remains the clear source of truth.

-   The AI asset inventory holds AI systems your organization has deliberately onboarded through a governed connector.
-   Shadow AI surfaces AI usage and detected services that nobody has onboarded.

See [How Shadow AI fits with your AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-relationship-to-inventory.md) for how the two lists differ and what you can do with a detected service.

## Shadow AI benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Detect AI usage your organization never approved, across network traffic and managed devices.|[How Shadow AI detects unsanctioned AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-how-detection-works.md)|AI steward|
|View potential exposure including services, users, and whether a policy already applies.|[Shadow AI overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-overview.md)|AI steward|
|Learn how a specific service is being used and by whom.|[Detected AI service overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-service-overview.md) and [Detected AI service details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-service-details.md)|AI steward|
|View prompts and conversation details to further understand usage \(ACC only\).|[Detected AI service conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-service-conversations.md)|AI steward|
|Triage a detection: clear a low-risk finding, or block access outright.|[Triage a detected AI service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-respond-to-service.md)|AI steward|
|Keep detection focused on what actually matters to your organization by curating the AI services registry.|[Manage the AI services registry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-manage-registry.md)|AI steward|

## What to explore next

To learn more about configuring and using Shadow AI, see:

-   [Configuring Shadow AI in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-configuring.md)
-   [Assessing AI exposure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-assessing-ai-exposure.md)
-   [Investigating a detected AI service in Shadow AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-investigating-detected-services.md)


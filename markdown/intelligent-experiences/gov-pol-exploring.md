---
title: Exploring policies in AI Control Tower
description: Learn how policies let you automatically respond to detected AI threats or block AI usage outright, and where policies are enforced across AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-pol-exploring.html
release: zurich
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI, explore]
breadcrumb: [Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Exploring policies in AI Control Tower

Learn how policies let you automatically respond to detected AI threats or block AI usage outright, and where policies are enforced across AI Control Tower.

## Policies overview

Blocking a rogue AI agent or containing a detected threat typically involves writing custom scripts, or reacting to an issue that's often discovered well after it has occurred. These approaches don't scale past a handful of one-off exceptions, and they don't hold up consistently across every platform your organization runs AI on.

Policies address this by letting you define that governance once, as a reusable rule, instead of reacting case by case.

-   Respond automatically when a detected threat, such as a prompt injection or excessive data exposure, crosses a threshold you define.
-   Stop a specific AI agent, model, or domain from being used, without writing a flow.
-   Preview which requests a policy would affect before publishing it.
-   See exactly which policy blocked or allowed a given request, and why.

## Policy users

|User|Description|
|----|-----------|
|AI steward|Creates, clones, and deactivates Threat Response and Explicit Block policies, and reviews policy enforcement activity to confirm policies are working as expected.|

## Policy types

Policies come in two types, each suited to a different governance need.

-   **Threat Response**

    Watches for a specific threat category, such as sensitive data disclosure or prompt injection, crossing a threshold you define \(for example, more than 50 detections in 10 minutes\). When triggered, deactivates the affected agent, and can create a ticket for a team or notify a group. The affected agent stays offline until it's reinstated. For details, see [Threat Response policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-threat-response.md).

-   **Explicit Block**

    Stops a group, user, or everyone from using a specific AI agent, model, or domain. Once initiated, the block stays in effect until the policy is deactivated. For details, see [Explicit Block policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-explicit-block.md).


## Policy enforcement points

Policies are evaluated and enforced at points throughout your organization.

-   **Agent Client Collector \(ACC\)**

    Blocks and unblocks AI agents by model or domain, through ACC's AI governance policy.

-   **Cloud-hosted agent platforms**

    Amazon Bedrock, Amazon Bedrock AgentCore, Azure AI Foundry, and Gemini Enterprise Agent Platform agents. Each platform is enforced through its own native access control, so the same rule reaches an agent no matter which of these it runs on.

-   **Okta**

    Blocks and unblocks a person's access through their Okta-managed identity.

-   **ServiceNow agents**

    Blocks and unblocks AI agents hosted by ServiceNow.


For a complete list, see [Control enforcement points](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-enforcement-points.md).

## Policies workflow

This infographic shows a sample end-to-end workflow of the AI steward sets up policy enforcement points, creates policies, and reviews enforcement activity.

\[Omitted image "mmasset0022400-policies-workflow-ai-control-tower-vertical.svg"\] Alt text: Infographic showing policy enforcement configuration and actions taken by the AI steward. For details, refer to the following description.

In this workflow:

1.  The AI steward configures one or more control enforcement points.
2.  The AI steward creates a Threat Response policy and defines the threat category, its scope, and the threshold that triggers a response.
3.  The AI steward creates an Explicit Block policy and defines who is blocked and what they're blocked from using.
4.  Once published, the policy is enforced at whichever connected points apply.
5.  The AI steward reviews enforcement activity to confirm the policy is working as expected.

## Policies benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Respond automatically to a detected threat before it spreads further.|[Create a Threat Response policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-create-threat-response-policy.md)|AI steward|
|Stop specific AI usage outright, without writing a flow.|[Create an Explicit Block policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-create-explicit-block-policy.md)|AI steward|
|Confirm a policy is working as expected.|[Reviewing policy enforcement in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-reviewing-enforcement-activity.md)|AI steward|

## What to explore next

To learn more about configuring and using Policies, see:

-   [Configuring policies in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-configuring.md)
-   [Managing policies in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-managing-policies.md)
-   [Reviewing policy enforcement in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-reviewing-enforcement-activity.md)
-   [AI Control Tower policies reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-pol-reference.md)


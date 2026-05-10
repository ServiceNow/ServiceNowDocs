---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection Product release email communication agentic workflow
description: Use the product release email communication agentic workflow to automatically draft, refine, and distribute the release announcement emails to designated recipients by retrieving the most recent product release information.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Success Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection Product release email communication agentic workflow

Use the product release email communication agentic workflow to automatically draft, refine, and distribute the release announcement emails to designated recipients by retrieving the most recent product release information.

## Prerequisites

To access the agentic workflow and product release content generator skill, install the plugin AI Agents for Customer Success Management \(sn\_cust\_succ\_ai\_ag\) in your instance.

**Important:** In the Now Assist skills page, make sure to Activate the product release content generator skill to trigger the agentic workflow. See [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/activate-skill.md) for more details.

## Product release email communication agentic workflow overview

The agentic workflow automatically drafts, refine, and publish release announcement emails to the multiple customers regarding the product changes and features adoption. The agentic workflow invokes the AI agent to fetch the latest released product information and creates a draft email. With this agentic workflow a customer can:

-   Timely communicate customers about product changes, enhancements, new feature releases, and feature adoption.
-   Identify the stakeholders, ensures consistent messaging, and streamline distribution.
-   Focus on driving adoption and customer value instead of repetitive communication tasks.

This agentic workflow is delivered as part of the out-of-the-box \(OOB\) product offering and is preconfigured to operate with the Digital Product Release \(DPR\) application. This enables customers to get started quickly using the default setup. However, the workflow is designed with flexibility in mind and isn’t limited to DPR. Organizations using alternative release management or related systems can seamlessly adopt this capability by integrating their existing applications with minimal customization. That ensures the workflow can be adapted to diverse system landscapes and specific business requirements.

When the DPR \(sn\_dpr\_model\_release\) record moves to the completed state, the agentic workflow triggers automatically. For more information about DPR, see [Digital Product Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-landing-page.md).

To modify the Product release email communication agentic workflow, [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

The CSM can trigger this agentic workflow manually only for assigned product releases.

The customer success manager can access this agentic workflow with these roles: sn\_acct\_Ic.customer\_success\_agent and sn\_dpr\_model.release\_user.

## Product release email communication agentic workflow

To access the use case:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Product Release Email Communication**.

To create a new use case, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

## AI agent used in the Product release email communication

The following AI agent is used to execute the instructions for the agentic workflow.

<table id="table_o3k_x3b_23c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Email communication manager AI agent

</td><td>

AI agent automates product release communications by retrieving the latest updates, generating personalized email drafts, and also giving CSMs the capability to edit the subject, introduction, and closing information in the email before sending it out. The agent handles the complete workflow from draft creation to delivery accurately, timely, and appropriately toned messages reach the recipients with minimal manual effort.

The AI agent is invoked only when the product release is marked completed by release manager.

</td></tr></tbody>
</table>To create an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).


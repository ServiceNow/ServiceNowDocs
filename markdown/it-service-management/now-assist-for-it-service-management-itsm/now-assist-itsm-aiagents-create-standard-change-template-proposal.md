---
title: IT Service Management AI agent collection create standard change template proposal
description: Use the create standard change template proposal agentic workflow to help users quickly create a change template proposal record based on similar change requests.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Change Management, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection create standard change template proposal

Use the create standard change template proposal agentic workflow to help users quickly create a change template proposal record based on similar change requests.

## Create standard change template proposal agentic workflow overview

The create standard change template proposal agentic workflow lets users quickly create a change template proposal record from the Now Assist panel. The workflow analyzes similar change requests and lists them to the user. The user can select the preferred change request and the content for template generation, and the workflow then creates a proposal record with the specified values.

Using this agentic workflow, you can quickly propose a change template for a change request that you frequently create. This template is later sent for approval to the change management team, which reviews the request and approves the template as part of the approval process.

To modify the Create standard change template proposal agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements. The Create standard change template proposal agentic workflow doesn’t have a trigger and is invoked manually.

**Note:** The workflow can be accessed by the change\_manager and itil role.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Create standard change template proposal**.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## AI agent used in the create standard change template proposal agentic workflow

You can access the standard change template proposal AI agent in the Define key requirements screen by scrolling to the Add AI agents that can perform these steps section. When a change is provided, this agent finds similar changes and lists them. The user can then select the preferred change request and the content for template generation, and the agent then creates a proposal record with the specified content.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Use the create standard change template proposal agentic workflow

1.  Review the information in the Define key requirements screen and make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen, turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

    The agent executes the request for the workflow.

    ![Create standard change template proposal agentic workflow output in ServiceNowAI Agent Studio.](../image/now-assist-itsm-change-template-proposal-agent-studio.png "Example of the create standard change template proposal agentic workflow output in ServiceNowAI Agent Studio")

4.  Access and use the create standard change template proposal agentic workflow from the Now Assist panel.

    You can query in the Now Assist panel with the change request number. For the query instructions, read the steps specified in the **List of steps** field of the corresponding AI agent \(standard change template proposal AI\).

    ![Create standard change template proposal agentic workflow output in the Now Assist panel.](../image/now-assist-itsm-change-template-proposal-nap.png "Example of the create standard change template proposal agentic workflow output in the Now Assist panel")



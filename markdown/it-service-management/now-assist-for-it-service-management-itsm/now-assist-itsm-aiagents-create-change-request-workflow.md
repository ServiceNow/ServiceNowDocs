---
title: IT Service Management AI agent collection create standard change request
description: Use the create standard change request agentic workflow to help users create a standard, normal, or emergency change request in a conversational and intuitive way.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Change Management, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection create standard change request

Use the create standard change request agentic workflow to help users create a standard, normal, or emergency change request in a conversational and intuitive way.

## Create standard change request agentic workflow overview

The create standard change request agentic workflow assists users in creating change requests quickly and efficiently. On initiation, the workflow prompts users to select the specific type of change they want to request - standard, normal, or emergency.

-   If the user selects standard, they’re prompted to provide additional information about the change request. On receiving this information, the workflow first retrieves historical template data from previous change requests. It analyzes the data, and recommends suitable templates that closely match the user’s current scenario. The workflow also generates direct links for users to create change records based on the suggested templates.
-   If the user selects normal or emergency, the workflow directly generates a link for users to create a normal or emergency change request record.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Create standard change request**.

**Note:** The workflow can be accessed by the sn\_change\_write and itil role.

To modify the create standard change request agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements. The create standard change request agentic workflow doesn’t have a trigger and is invoked manually.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## AI agent used in the create standard change request agentic workflow

You can access the standard change template recommender AI agent in the Define key requirements screen by scrolling to the Add AI agents that can perform these steps section. When a user asks for help in the Now Assist panel to create a change request of type standard, the agent retrieves historical template data from previous change requests. By analyzing this data, it suggests suitable templates that closely match the user’s current scenario. Then, it generates links for users to create change records based on these suggested templates. If a user asks for help with creating a normal or emergency change request, then the agent generates a link directly to create a normal or emergency change request.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Use the create standard change request agentic workflow

1.  Review the information in the Define key requirements screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen, turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

    The agent executes the request for the workflow.

    ![Create standard change request agentic workflow output in ServiceNowAI Agent Studio.](../image/now-assist-create-change-agent-studio.png "Example of the create standard change request agentic workflow output in the ServiceNowAI Agent Studio")

4.  Access and use the create standard change request agentic workflow from the Now Assist panel.

    You can query in the Now Assist panel to create a change request. For the query instructions, read the steps specified in the **List of steps** field of the corresponding AI agent \(standard change template recommender AI agent\).

    ![Create standard change request agentic workflow output in the Now Assist panel.](../image/now-assist-create-change-nap.png "Example of the create standard change request agentic workflow output in the Now Assist panel")



---
title: IT Service Management AI agent collection Suggest configuration items for a change request
description: Use the Suggest configuration items for a change request agentic workflow to make the process of selecting configuration items during change creation conversational, intuitive, and efficient for users.
locale: en-US
release: yokohama
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-09-10"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Agentic AI in the Change Management application, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Suggest configuration items for a change request

Use the Suggest configuration items for a change request agentic workflow to make the process of selecting configuration items during change creation conversational, intuitive, and efficient for users.

## Suggest configuration items for a change request overview

The Suggest configuration items for a change request agentic workflow lets users quickly find and link relevant configuration items \(CIs\) to a change request from the Now Assist panel. The workflow analyzes change request content and suggests appropriate CIs.

To modify the Suggest configuration items for a change request agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Note:** The workflow can be accessed by the itil role.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Suggest configuration items for a change request**.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## AI agent used in the Suggest configuration items for a change request agentic workflow

You can access the Change CI suggestion AI agent in the Define key requirements screen by scrolling to the Add AI agents that can perform these steps section. The Change CI suggestion AI agent assists users in identifying and associating appropriate configuration items \(CIs\) with specific change requests. This agent analyzes the content of the change request and suggests relevant configuration items to the user.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Use the Suggest configuration items for a change request agentic workflow

1.  Review the information in the Define key requirements screen and make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen, turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

    The agent executes the request for the workflow.

    ![Suggest configuration items for a change request workflow output in ServiceNowAI Agent Studio](../image/now-assist-change-management-suggest-ci-item.png "Example of the Suggest configuration items for a change request agentic workflow output in ServiceNowAI Agent Studio")

4.  Access and use the Suggest configuration items for a change request agentic workflow from the Now Assist panel.

    You can query in the Now Assist panel with the change request number. For the query instructions, read the steps specified in the **List of steps** field of the corresponding AI agent \(Change CI suggestion AI agent\).

    ![Suggest configuration items for a change request workflow output in the Now Assist panel](../image/now-assist-suggest-ci-change-request-nap.png "Example of the Suggest configuration items for a change request agentic workflow output in the Now Assist panel")



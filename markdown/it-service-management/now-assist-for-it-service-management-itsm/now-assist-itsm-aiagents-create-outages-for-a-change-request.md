---
title: IT Service Management AI agent collection Create outages for a change request
description: Use the Create outages for a change request agentic workflow so users can associate outages with a change request easily in a conversational and intuitive way.
locale: en-US
release: yokohama
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-10-10"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Agentic AI in the Change Management application, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Create outages for a change request

Use the Create outages for a change request agentic workflow so users can associate outages with a change request easily in a conversational and intuitive way.

## Create outages for a change request overview

The Create outages for a change request agentic workflow lets users quickly create outages for a change request from the Now Assist panel.

The workflow first examines the current change record to determine if any outages are already linked to it. If no outages are found, it retrieves the planned start and end dates from the change request. In cases where these dates aren’t specified in the change request, the workflow prompts the user to input the necessary dates. Next, the workflow creates an outage record for the change request. If a configuration item \(CI\) is present, it attaches the affected CIs to the outage record. The workflow then checks whether there’s an impacted service associated with the change record. If a service exists, it asks the user if the impacted service should be linked to the affected configuration items within the outage record. This conversational and automated approach helps streamline the process, enabling users to associate outages with change requests while recording relevant data.

To modify the Create outages for a change request agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Note:** The workflow can be accessed by the itil role.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Create outages for a change request**.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## AI agent used in the Create outages for a change request agentic workflow

You can access the Change outage assistant AI agent in the Define key requirements screen by scrolling to the Add AI agents that can perform these steps section. The Change outage assistant AI agent assists users in creating outages for change records. The agent creates outage records for the change request based on the CIs that are as being impacted by the change request.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Use the Create outages for a change request agentic workflow

1.  Review the information in the Define key requirements screen and make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen, turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

    The agent executes the request for the workflow.

    ![Create outages for a change request agentic workflow output in ServiceNowAI Agent Studio](../image/now-assist-change-outage-agent-studio.png "Example of the Create outages for a change request agentic workflow output in ServiceNowAI Agent Studio")

4.  Access and use the Create outages for a change request agentic workflow from the Now Assist panel.

    You can query in the Now Assist panel with the change request number. For the query instructions, read the steps specified in the **List of steps** field of the corresponding AI agent \(Change outage assistant AI agent\).

    ![Create outages for a change request agentic workflow output in the Now Assist panel](../image/now-assist-change-outage-nap.png "Example of the Create outages for a change request agentic workflow output in the Now Assist panel")



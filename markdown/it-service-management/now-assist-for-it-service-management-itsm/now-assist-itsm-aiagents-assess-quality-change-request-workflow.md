---
title: IT Service Management AI agent collection assess quality of a change request agentic workflow
description: Use the assess quality of a change request agentic workflow to assess the quality of a change request, analyze the information available in the fields, and generate suggestions to improve the information in the fields.
locale: en-US
release: yokohama
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-08-22"
reading_time_minutes: 4
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Agentic AI in the Change Management application, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection assess quality of a change request agentic workflow

Use the assess quality of a change request agentic workflow to assess the quality of a change request, analyze the information available in the fields, and generate suggestions to improve the information in the fields.

## Assess quality of a change request agentic workflow overview

Using the assess quality of a change request agentic workflow, you can assess the quality of a change request based on the information available in the fields. You can also simultaneously generate suggestions for good quality, holistic information that can be provided in the fields to improve the quality of a change request. You can use the workflow to assess the quality of a new change request, or improve the information available for an existing change request that is not in the closed state.

To evaluate the quality of information in a change request, the workflow finds similar closed change requests with matching descriptions, and the close code marked as successful. On the basis of the matching change request, the workflow generates a quality report of the descriptions, planning, risk, and impact information. The generated quality assessment contains the assessed fields, the justification for the quality marking, and the suggestions to improve the existing information.

**Note:** The assess quality of a change request agentic workflow doesn’t have a trigger and is invoked manually.

To modify the assess quality of a change request agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements. To clone an agentic workflow that is available by default, you must execute the semantic index for similarChangeRequests. The Business Rule \(\[Chg Quality\] Trigger semantic index\) that is available by default that activates this workflow doesn’t run automatically for cloned cases, so you must activate it manually or execute the script in the business rule to confirm that the index is performed.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Assess the quality of a change request

Autonomously assess the quality of change requests, and generate suggestions to improve information in fields.

**Note:** The workflow can be accessed by the sn\_uxc\_gen\_ai.sn\_aia\_chg\_quality role that is available as a part of the itil or sn\_change\_write role.

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Assess quality of a Change Request**.

## AI agent used in the assess quality of a change request agentic workflow

When provided with the details of a change request, the change quality assessor AI agent automatically analyzes the quality of the information available in a closed change request containing matching descriptions, and provides suggested values.

The quality assessment using the agent can provide information and suggested values regarding the following areas:

-   Short description
-   Description
-   Implementation plan
-   Backout plan
-   Test plan
-   Risk and impact analysis
-   Justification

The assessment report is generated for the overall change request and all the areas mentioned. The quality assessment categorizes the information under the Excellent, Very good, Good, Fair, Poor, Very Poor, or Incomplete categories. If the quality of the change request and all of its fields are assessed to be Excellent, no suggestions are provided. The work notes field for the change request is updated with the quality assessment report generated using the agent.

## Assess the quality of information using the assess quality of a change request workflow

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select a UI display screen turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

The agent executes the request for the agentic workflow.

## Example of the assess quality of a change request agentic workflow output in the ServiceNow® AI Agent Studio

![Assess quality of a change request agentic workflow output in AI Agent Studio.](../image/now-assist-itsm-assess-quality-of-change-request-workflow.png)

Access and use assess quality of a change request agentic workflow from the Now Assist panel.

You can add a query using the change request number to use the AI agent. You can enter the number of the field from the list of suggestions, add relevant keywords, or provide custom responses to the agent to update the field values. The agent asks for a confirmation before updating the fields.

For the query instruction, follow the steps specified in the **List of steps** field of the Define key requirements screen of the agentic workflow record.

In the AI Agent Studio, the human agent gets notified as soon as a text message is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).


---
title: Resolve noncritical HR cases agentic workflow
description: Use the Resolve noncritical HR cases agentic workflow to assess the criticality of HR cases and automatically respond to noncritical inquiries without human intervention. Human agents must intervene when requests are marked critical.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [AI agents, agentic AI]
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Resolve noncritical HR cases agentic workflow

Use the Resolve noncritical HR cases agentic workflow to assess the criticality of HR cases and automatically respond to noncritical inquiries without human intervention. Human agents must intervene when requests are marked critical.

## Resolve noncritical HR cases agentic workflow overview

The Resolve noncritical HR cases agentic workflow can evaluate HR requests submitted by employees of both critical and non-critical nature. The workflow:

-   checks criticality
-   generates recommendations for a non-critical request fulfillment
-   requests for a human agent intervention when a case is identified as critical

The agents, tools, and triggers that are associated with the Resolve HR cases agentic workflow are provided by Now Assist applications. You can activate the agentic workflow template by making triggers active. If you want to change this agentic workflow's instructions, you must duplicate it, adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

You must have HRSD Pro plus for Now Assist installed for the HR Service Delivery AI Agent Collection. When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Accessing the Resolve noncritical HR cases agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Resolve noncritical HR cases**.

![Accessing Resolve noncritical HR cases agentic workflow](../image/set-up-nc-case.png)

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools, and information.

## Resolve noncritical HR cases agentic AI agents

The following table lists the agents that are used in the Resolve noncritical HR cases agentic workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|HR search and notify AI agent|Performs search to find relevant HR knowledge articles and catalog items related to the given query and raise notification if relevant information is found.|
|HR criticality detection AI agent|Performs criticality detection on an HR case and acts based on the criticality level.|

In the Resolve noncritical HR cases agentic workflow, review the information in the Describe and connect section, make the necessary updates to ensure the agentic workflow adapts to your requirements, and then select **Save and Continue**.

## Trigger

Business rule: The **Trigger non critical use case** business rule serves as a trigger that executes following the completion of the Predict service and Transfer HR cases use case. This business rule contains conditions that determine when the Resolve noncritical HR cases use case should be initiated. Modify the conditions to align with your specific business requirements. ![Activating business rule](../image/trigger-nc-br1.png)![Activating business rule](../image/trigger-nc-br.png)

## Executing a test scenario

You can run this workflow on the Testing page of AI Agent Studio with the following utterance in the Task field:

"Resolve HRC000XXX"

The AI agent decision log displays the AI agents that are working to resolve the case, and you can watch their interactions, decisions, and thought processes as they happen in real time.

**Note:** The AI agent decision log is available in the **Testing** section in AI Agent Studio and is intended for testing purposes only.

.![Testing input for the agentic workflow.](../image/resolve-nc-workflow.png)![Testing output for the agentic workflow.](../image/resolve-noncritical-workflow.png)

The AI agent assesses each HR case to determine its criticality.

-   For non-critical cases, it retrieves and recommends relevant articles, then notifies the employee via Now Assist Virtual Agent or email. Employee can review the recommendations, provide feedback, or close the case.
-   For critical cases, Human agents intervention is requested.

## Example of event creation on Agent Workspace for HR Case Management

This is an example of how the Resolve noncritical HR cases agentic workflow generates recommendations for a non-critical case, and sends email notifications to the requester.![Event creation on Agent Workspace for HR Case Management](../image/nc-request.png)![Event creation on Agent Workspace for HR Case Management](../image/nc-request1.png)


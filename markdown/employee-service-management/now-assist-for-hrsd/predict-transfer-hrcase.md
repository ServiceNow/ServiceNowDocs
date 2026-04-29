---
title: Predict service and transfer HR cases agentic workflow
description: Analyze an HR case and automatically route it to the most appropriate HR service with the predict service and transfer HR cases agentic workflow. Optimize HR Case Management, ensuring that cases are handled by the most appropriate teams.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Predict service and transfer HR cases agentic workflow

Analyze an HR case and automatically route it to the most appropriate HR service with the predict service and transfer HR cases agentic workflow. Optimize HR Case Management, ensuring that cases are handled by the most appropriate teams.

## Overview of Predict service and transfer HR cases agentic workflow

The agents, tools, and triggers that are associated with the Predict service and transfer HR cases agentic workflow are provided by Now Assist applications. You can activate the agentic workflow template by making triggers active. If you want to change this agentic workflow's instructions, you must duplicate it, adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

You must have HRSD Pro plus for Now Assist installed for the HR Service Delivery AI Agent Collection. When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

Perform the following steps after you [Configure Group Action Framework](https://www.servicenow.com/docs/access?context=configure-gaf&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.
2.  Run **HR service GAF grouping job** with an admin role. This generates **GAF - Run Offline Flow** in the Global scope.
3.  Run **GAF - Run Offline Flow** and monitor its progress.

## Accessing the Predict service and transfer HR cases agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Predict service and transfer HR cases agentic workflow**.

![Accessing the Predict service and transfer HR cases agentic workflow](../image/set-up-hr-predict.png)

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, agent instructions/prompts, and tools. Tools are displayed in the second step of the AI agent-guided setup, Add tools, and information.

## Predict service and transfer HR cases agentic workflow AI agents

The following table lists the agents that are used in the Predict service and transfer HR cases agentic workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|Record field value prediction AI agent|Predicts the HR service of an incoming case. It can also provide a summary and justification of prediction.|
|HR Case Transfer AI Agent|Automatically transfers the case to the predicted service.|

## Triggers

Activate triggers according to your organization's requirements, and enable/disable the required COEs.

![Activating the triggers for the Predict service and transfer HR cases agentic workflow.](../image/trigger-predict-hr.png)

In the Predict service and transfer HR cases agentic workflow, review the information in the Describe and connect section, make the necessary updates to ensure the agentic workflow adapts to your requirements, and then select **Save and Continue**.

## Executing a test scenario

You can run this workflow on the Testing page of AI Agent Studio with the following utterance in the Task field: "Help me predict and transfer HR case with number "HRC000XXX" with "sys\_id " and table "sn\_hr\_core\_case".

The AI agent decision log displays the AI agents that are working to predict and transfer the case, and you can watch their interactions, decisions, and thought processes as they happen in real time.![Testing input for the agentic workflow.](../image/test-predict-service.png)![Testing output for the agentic workflow.](../image/test-predict-service1.png)

## Prediction and transfer results on Agent Workspace for HR Case Management

This is an example of how the Predict service and transfer HR cases agentic workflow automatically identifies the appropriate HR service for a case, and transfers the case to the identified service.

![Prediction and transfer results on Agent Workspace for HR Case Management](../image/hr-predicted-service.png)


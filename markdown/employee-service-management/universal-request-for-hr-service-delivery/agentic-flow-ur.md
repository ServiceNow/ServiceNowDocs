---
title: Universal Request Router agentic workflow
description: Enables employees to request a department agnostic ticket to avail services that are not readily accessible/understandable via the catalog listings or the services that require collaboration across multiple departments.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using agentic flows in Universal Request AI agent collection, Universal Request, Employee Service Management]
---

# Universal Request Router agentic workflow

Enables employees to request a department agnostic ticket to avail services that are not readily accessible/understandable via the catalog listings or the services that require collaboration across multiple departments.

## Overview of Universal Request Router agentic workflow

The agents, tools, and triggers that are associated with the Universal Request Router agentic workflow are provided by Now Assist applications. You can activate the agentic workflow template by making triggers active. If you want to change this agentic workflow's instructions, you must duplicate it, adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

Verify that the Universal Request AI agent collection Plugin \(com.sn\_ur\_ai\_agents\) is installed.

## Accessing the Universal Request Router agentic workflow

![](../images/ur-access.png)

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Universal Request Router** agentic workflow.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, agent instructions/prompts, and tools. Tools are displayed in the second step of the AI agent-guided setup, Add tools, and information.

## Universal Request Router agentic workflow AI agents

![](../images/ur-ai-agents.png)

The following table lists the agents that are used in the Universal Request Router agentic workflow.

**Note:** In the Define availability screen for the AI agent, make sure that the Status toggle is enabled to activate the AI agent.

Agents used in the Universal Request Router agentic workflow:

<table id="table_v4x_1ml_c3c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Universal Request departmental ticket creator

</td><td>

Automates the routing of universal requests to appropriate departmental ticketing systems by analyzing department predictions and creating properly configured HR cases or IT incidents with all necessary field mappings and reference tracking.

</td></tr><tr><td>

Record field value prediction AI agent

</td><td>

Predict fields of an incoming task/record by gathering incoming task sys\_id. It can also provide a summary and justification of the field predictions.

</td></tr></tbody>
</table>## Triggers

Activate the triggers according to your organization's requirements.

![](../images/ur-triggers.png)

## Executing a test scenario

You can run this workflow on the Testing page of AI Agent Studio with the following utterance in the Task field: Help me resolve &lt;UR case&gt;.

The AI agent decision log displays the AI agents that are working to predict the department for the ticket, and create a primary ticket for the identified department. You can also watch their interactions, decisions, and thought processes as they happen in real time.

![](../images/ur-testing.png)![](../images/ur-testing-output.png)

## Predict and create a primary ticket in Universal Request page

This is an example of how the Universal Request Router agentic workflow automatically predicts the department for the ticket, and creates a primary ticket for the identified department.![](../images/ur-predict.png)![](../images/ur-predict-service.png)

**Parent Topic:**[Using agentic flows in Universal Request AI agent collection](ur-ai-agent-collection.md)


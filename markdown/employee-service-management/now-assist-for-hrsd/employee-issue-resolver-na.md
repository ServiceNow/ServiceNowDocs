---
title: Resolve HR cases agentic workflow
description: Use the Resolve HR cases agentic workflow to evaluate case criticality and retrieve relevant knowledge articles to resolve HR cases, and generate a fulfillment plan for an HR case, minimizing the need for agent intervention.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-04-07"
reading_time_minutes: 3
keywords: [AI agents, agentic AI]
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Resolve HR cases agentic workflow

Use the Resolve HR cases agentic workflow to evaluate case criticality and retrieve relevant knowledge articles to resolve HR cases, and generate a fulfillment plan for an HR case, minimizing the need for agent intervention.

## Resolve HR cases overview

Use the Resolve HR cases AI agent team to:

-   Automate the resolution of routine employee queries that are submitted via any channel that logs an HR case such as email, catalog, or Virtual Agent. Assess criticality, retrieve relevant knowledge base responses, and detect sensitive topics that relate to your employee relation cases to route to live agents when necessary.
-   Generate an ordered step-wise fulfillment/execution plan for an HR case, thus helping in faster resolution of the HR case.

**Note:** You must have HRSD Pro plus for Now Assist installed for the HR Service Delivery AI Agent Collection. When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Resolve HR cases agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Resolve HR cases**.

## Resolve HR cases AI agents

The following table lists the agents that are used in the Resolve noncritical HR cases agentic workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|HR criticality detection AI agent|Determines the criticality of the request based on the urgency, impact, escalation scenarios, and keywords.|
|HR search retrieval AI agent|Fetches information about the relevant knowledge articles and catalogs that are related to the request.|
|Record management AI agent|Populates work notes with case details for critical cases or when no relevant recommendations are available for non-critical cases.|
|HR notification AI agent|Notifies users of the recommendations and collects feedback via email and chat.|
|HR Case Planner AI Agent|Creates an ordered step-wise HR case fulfillment /execution plan.|

The AI agent decision log displays the AI agents that are working to resolve the case, and you can watch their interactions, decisions, and thought processes as they happen in real time.

**Note:** The AI agent decision log is available in the **Testing** section in AI Agent Studio and is intended for testing purposes only.

## Resolving an HR case

In the Resolve HR cases agentic workflow, review the information in the Describe and connect section, make the necessary updates to confirm the agentic workflow adapts to your requirements, and then select **Save and Continue**.

The agent executes the test scenario in AI Agent Studio for the agentic workflow.

![In AI Agent Studio where it shows the testing output for Resolving HRcase agentic workflow.](../image/resolve-noncritical-workflow.png "Example of resolving a noncritical case")

The employee is notified via the Now Assist Virtual Agent or email when the recommendation is generated. They can provide feedback on the recommendation or close the case.

![Generation of a fulfillment plan for an HR case](../image/case-planner-1.png "Example of generating a fulfillment plan for an HR case")

![Generation of a fulfillment plan for an HR case](../image/case-planner-2.png)

![Generation of a fulfillment plan for an HR case](../image/case-planner-3.png)

![Generation of a fulfillment plan for an HR case](../image/case-planner-4.png)

The AI agent creates a fulfillment plan for a given HR case by fetching HR case details, relevant KB articles, and fulfillment instructions. HR agents can add prompts for refining the fulfillment plan. Once approved, the fulfillment plan is added to the work notes of the case.

**Note:** The option to generate a resolution plan appears only for the HR service of Fulfillment type: **Manual**. It does not appear for the Employee Relations and Life Cycle Events cases.

-   **[Generate a fulfillment plan](../task/generate-rp.md)**  
Auto-generate a fulfillment/execution plan for a case, helping in faster resolution of the HR case.

**Parent Topic:**[Using agentic workflows in Now Assist for HRSD](now-assist-hrsd-ai-agents-use-cases.md)


---
title: Resolve critical HR case agentic workflow
description: Resolve critical HR requests efficiently with the Resolve critical HR case agentic workflow. This workflow generates a tailored fulfillment plan for an HR case using fulfillment instructions, KB articles, or resolution notes of similar past cases. It helps accelerate the resolution process by providing planning support to HR agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-hrsd/employee-issue-resolve-critical.html
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-11-03"
reading_time_minutes: 4
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Resolve critical HR case agentic workflow

Resolve critical HR requests efficiently with the Resolve critical HR case agentic workflow. This workflow generates a tailored fulfillment plan for an HR case using fulfillment instructions, KB articles, or resolution notes of similar past cases. It helps accelerate the resolution process by providing planning support to HR agents.

## Resolve critical HR case agentic workflow overview

The agents, tools, and triggers that are associated with the Resolve critical HR case agentic workflow are provided by Now Assist applications. You can activate the agentic workflow template by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must duplicate it, adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

You must have HRSD Pro plus for Now Assist installed for the HR Service Delivery AI Agent Collection. When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

Perform the following steps after you .

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.
2.  Run **HR service GAF grouping job** with an admin role. This generates **GAF - Run Offline Flow** in the Global scope.
3.  Run **GAF - Run Offline Flow** and monitor its progress.

## Accessing the Resolve critical HR case agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Agentic workflows** &gt; **Resolve critical HR case**.

\[Omitted image "set-up-critical-case.png"\] Alt text: Accessing the Resolve critical HR case agentic workflowThe first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## Resolve critical HR case AI agents

The following table lists the agents that are used in the Resolve noncritical HR cases agentic workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the Status toggle is enabled to activate the AI agent.

<table id="table_bpl_31s_y2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

HR Case Planner AI Agent

</td><td>

Creates an ordered step-wise fulfillment/execution plan for an HR case based on specific COE or HR service. **Note:** This AI agent is invoked when fulfillment instructions are present for an HR case.

</td></tr><tr><td>

Next action recommended AI agent

</td><td>

Identifies the optimal steps for resolving tasks by referencing similar case details, reviewing relevant knowledge articles and web search results. It summarizes and presents to the user a step-by-step summarized resolution plan and derived action plan. Implements the feedback flow only when asked for it.**Note:** This AI agent is invoked when fulfillment instructions aren't present for a case.

</td></tr></tbody>
</table>In the Resolve HR cases agentic workflow, review the information in the Describe and connect section, make the necessary updates to confirm the agentic workflow adapts to your requirements, and then select **Save and Continue**.

## Trigger

UI action: To make Generate plan available to users on the HR case form in UI16 and Agent Workspace for HR Case Management, you must activate the UI action. When activated, a button appears that says **Generate Plan** when users are looking at active records on the HR case table.

1.  Navigate to **All** &gt; **System UI** &gt; **UI actions**.
2.  Search in the Name field for **Generate plan**.
3.  Open the record.
4.  Set Active to true.
5.  Save or update the record.

## Executing a test scenario

After the workflow has been activated in AI Agent Studio, you can run this workflow on the Testing page of AI Agent Studio with the following utterance Plan in the in the Task field: HRC000XXX.

The AI agent decision log displays the AI agents that are working to resolve the case, and you can watch their interactions, decisions, and thought processes as they happen in real time.

**Note:** The AI agent decision log is available in the **Testing** section in AI Agent Studio and is intended for testing purposes only.

\[Omitted image "case-planner-1.png"\] Alt text: Testing input for the agentic workflow.\[Omitted image "case-planner-2.png"\] Alt text: Testing output for the agentic workflow.

The AI agent creates fulfillment plans by analyzing HR case details, employee information \(location and designation\), relevant KB articles, fulfillment instructions, and resolution notes from similar cases. HR agents can refine the plan through prompts before approving it. Approved plans are automatically added to the case work notes.

**Note:** The option to generate a resolution plan appears only:

-   For the HR service of Fulfillment type: **Manual**. It does not appear for the Employee Relations and Life Cycle Events cases.
-   When a case is move to Ready state.

## Generating a resolution plan for an HR case

For more information, see [Generate a fulfillment plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/generate-rp.md)


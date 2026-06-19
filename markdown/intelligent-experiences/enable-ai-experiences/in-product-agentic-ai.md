---
title: In-product experience for agentic workflows
description: Dedicated spaces in workspaces and in the Core UI enable you to use agentic workflows directly in record forms. You can view agentic workflow progress and previous executions, and you can answer follow-up questions for ones that require human supervision.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/in-product-agentic-ai.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 4
breadcrumb: [Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# In-product experience for agentic workflows

Dedicated spaces in workspaces and in the Core UI enable you to use agentic workflows directly in record forms. You can view agentic workflow progress and previous executions, and you can answer follow-up questions for ones that require human supervision.

## Agentic AI in the Core UI and workspaces

Agentic workflows can help you accomplish complex tasks, such as generating resolution notes for cases and incidents or investigating problems and root causes. You can view agentic workflows running on a record in the AI Workflows panel, available in both the Core UI form and in workspaces. For agentic workflows that require human supervision, you can answer questions, approve next steps, or provide other input. In addition to monitoring current progress, you can review historical runs to compare results.

To create UI actions for your agentic workflows, open the agentic workflow in AI Agent Studio, navigate to the [Select channels and access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/channels-access-aw.md) step in the guided setup, and create a UI action.

If the AI Workflows panel is not visible, check the following:

-   Ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`.
-   Check whether the Workspace user preferences have **Show the sidebar** toggled on. If this setting is not enabled, the AI Workflows panel will not display. To access this setting, select the profile icon at the top right of the screen, then select **Preferences**. The setting is located on the Workspace tab.

\[Omitted image "inproduct-ai.png"\] Alt text: Service Operations Workspace with the AI Workflows open

## Agentic workflow execution list

The list of agentic workflow cards can be filtered by execution state, and you can change the active filters at any time.

**Note:** The **Ready for review** state differs from the **Completed** state in that the former indicates the workflow has generated some output. Agentic workflows without an output are marked only as **Completed**.

The **Supervised by** field identifies the user responsible for answering follow-up questions. Only the specified user can provide answers to progress the agentic workflow, though others can view the questions asked.

\[Omitted image "inproduct-ai-filter.png"\] Alt text: Filter dropdown for agentic workflow executions

Each card displays the current or final processing message. To view the full list of processing messages, select the agentic workflow card to open the details.

For currently running workflows, time estimates based on previous executions are displayed. For completed workflows, the cards show the total time taken.

The execution list also displays the results of any workflows triggered in the Now Assist panel or triggered automatically by events, once they are complete.

## Agentic workflow execution details

When you select a specific agentic workflow, you can view its processing messages and history. Processing messages indicate which steps the agentic workflow has already completed and which are still in progress.

You can modify the processing messages for an AI agent or tool in AI Agent Studio. For an AI agent, open the AI agent and go to the [Select channels and access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/channels-access-aia.md) step. For a tool, open the AI agent, go to the [Add tools and information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/add-tool-aia.md) step, and select the tool to open the form modal.

\[Omitted image "inproduct-ai-processing.png"\] Alt text: Processing messages in the AI Workflows panel

The history section of the card can display previous answers to follow-up questions. For completed agentic workflows, you can review the final output in the history if one exists. When an output is available, you can view the sources behind the AI's reasoning by selecting the information icon. Citations can include Knowledge Base articles and lists of records.

To copy the text of the final output of an agentic workflow, select the copy icon.

\[Omitted image "inproduct-ai-output.png"\] Alt text: Output of an agentic workflow

## Fields updated with agentic AI

When an agentic workflow changes the value of a field, Now Assist displays a label beneath the field value indicating that the value was modified by AI.

## AI presence indicator

While an agentic workflow is in progress on a record, an icon \[Omitted image "inproduct-ai-indicator.png"\] Alt text: AI workflow indicator appears at the top of the record form alongside other UI actions. Selecting it shows how many agentic workflows are running on the record and the general status of each.

To cancel an agentic workflow that is in progress, select the more options icon on the agentic workflow card, and then select **Cancel**.

## Alerts for agentic workflow status changes and required input

When an agentic workflow changes states, such as when it completes or has a follow-up question, an alert appears at the top of the screen. If the workflow generates an output, you can select the **Review** button to view the final result.


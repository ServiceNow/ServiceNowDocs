---
title: In-product experience for agentic workflows
description: Dedicated spaces in workspaces and in the Core UI enable you to use agentic workflows directly in record forms. You can view agentic workflow progress and previous executions, and you can answer follow-up questions for ones that require human supervision.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/in-product-agentic-ai.html
release: zurich
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 3
breadcrumb: [Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# In-product experience for agentic workflows

Dedicated spaces in workspaces and in the Core UI enable you to use agentic workflows directly in record forms. You can view agentic workflow progress and previous executions, and you can answer follow-up questions for ones that require human supervision.

## Agentic AI in the Core UI and workspaces

Agentic workflows can help accomplish complex tasks for you, such as generating resolution notes for cases and incidents or investigating problems and root causes. You can view agentic workflows running on a record in the AI Workflows panel in the Core UI form or in workspaces. For agentic workflows that require human supervision, you can answer questions, approve next steps, or provide other input. Along with current progress, you can also review historical runs to compare results.

You can create UI actions for your agentic workflows in AI Agent Studio. Open the agentic workflow, navigate to the [Select channels and access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/channels-access-aw.md) step in the guided setup, and create a UI action.

If you don't see this panel, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`.

\[Omitted image "inproduct-ai.png"\] Alt text: Service Operations Workspace with the AI Workflows open

## Agentic workflow execution list

The list of agentic workflow cards can be filtered by execution state. You can change which states to filter by at any time.

**Note:** The difference between the **Ready for review** state and the **Completed** state is that the former has generated some output. Agentic workflows without an output are marked only as **Completed**.

The user responsible for answering follow-up questions is identified by the **Supervised by** field. Only the user specified can answer questions to progress the agentic workflow, but others can see the questions asked.

\[Omitted image "inproduct-ai-filter.png"\] Alt text: Filter dropdown for agentic workflow executions

Each card displays the current or final processing message. You can see the full list of processing messages by selecting the agentic workflow card to open the details.

Time estimates based on previous executions are provided for currently running workflows. For completed workflows, the cards show the total time taken.

The execution list also displays the results of any workflows triggered in the Now Assist panel or triggered automatically by events once they are complete.

## Agentic workflow execution details

When you select a specific agentic workflow, you can view the processing messages and history. Processing messages show you what steps the agentic workflow has taken already and which ones are still being completed.

You can change the processing messages for an AI agent or tool in AI Agent Studio. For an AI agent, open the AI agent and go to the [Select channels and access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/channels-access-aia.md) step. For a tool, open the AI agent, go to the [Add tools and information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/add-tool-aia.md) step, and select the tool to open the form modal.

\[Omitted image "inproduct-ai-processing.png"\] Alt text: Processing messages in the AI Workflows panel

The history space on the card can show previous answers to follow-up questions. For completed agentic workflows, you can review the final output in the history if there is any. If there’s an output, you can see the sources for the AI's reasoning by selecting the information icon. Citations can include Knowledge Base articles and lists of records.

You can copy the text of the final output of an agentic workflow by selecting the copy icon.

\[Omitted image "inproduct-ai-output.png"\] Alt text: Output of an agentic workflow

## Fields updated with agentic AI

If an agentic workflow changes the value of a field, Now Assist displays a label under the field value stating that the value was modified by AI.

## AI presence indicator

When an agentic workflow is in progress on the record, an icon \[Omitted image "inproduct-ai-indicator.png"\] Alt text: AI workflow indicator is displayed at the top of the record form along with other UI actions. If selected, you can see how many agentic workflows are running on the record and the general status of each one.

If there’s an agentic workflow in progress that you don't want to complete, you can cancel it. Select the more options icon on the agentic workflow card, and then select **Cancel**.

## Alerts for agentic workflow status changes and required input

When an agentic workflow changes states, such as when it completes or has a follow-up question, an alert appears at the top of the screen. If the workflow generates an output, you can select the **Review** button to see the final result.


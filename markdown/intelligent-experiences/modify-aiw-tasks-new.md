---
title: Edit the tasks of an AI specialist in AI Agent Studio
description: Select tasks that an AI specialist can perform in the new AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/modify-aiw-tasks-new.html
release: zurich
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 5
breadcrumb: [Configure in AI Agent Studio, Configure, Autonomous Workforce, AI Agent Studio, Enable AI experiences]
---

# Edit the tasks of an AI specialist in AI Agent Studio

Select tasks that an AI specialist can perform in the new AI Agent Studio.

## Before you begin

Role required: sn\_aia.admin

## About this task

AI specialist tasks determine what they can do. Choosing the correct tasks provides your AI specialist with the tools required to complete complex goals autonomously.

To learn how to modify the roles and capabilities that an AI specialist has, see [Edit the profile of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/modify-aiw-tasks.md).

## Procedure

1.  Navigate to the **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI specialist you want to modify.

3.  In the node view, select the first node of the AI specialist.

    The first node contains the main configuration settings for the AI specialist. The other nodes represent the individual agents that comprise the underlying architecture and don't require modification for task configuration.

4.  Scroll down to the **Tasks** section in the AI specialist guided setup to view the full list of tasks that the AI specialist can perform.

5.  Select the card of a task to review, select the pencil icon, and make changes to the specific details of the task configuration.

    The following tasks are available to the [L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/l1-service-desk-ai-specialist.md). These are presented as examples. Different AI specialists may have different tasks.

    -   **Classify and assign: Configure how the AI specialist identifies incidents, classifies them, and assigns a specific incident type for follow-up.**
        -   **Table**: Select the table in which the AI specialist operates and resolution workflows are executed.
        -   **Fields to predict**: Enter the fields that the AI specialist should classify if empty.
        -   **Similar records search profile**: Select the AI Search profile that should be used for gathering records similar to the assigned record.
        -   **Override existing field values with predictions**: Enable this setting to let the AI specialist use predictions from similar records to replace existing values. Fields that can potentially be overridden are **Service**, **Offering**, and **CI**. Turn off if you only want the AI specialist to fill in empty fields.
    -   **Triage and diagnose: Configure the details for how the AI specialist analyzes incidents for accurate handling.**
        -   **Field to use as Task objective**: Select the record fields which the AI specialist uses to analyze and determine the next steps.
        -   **Use attachment content**: Enable the option for the AI specialist to review the content of attached files as part of incident triage and diagnosis.
        -   **Map AI specialist states to record states**: Map the states of the AI specialist's execution to the states of the incident record. For example, the AI specialist's **Awaiting information** state can be mapped to the incident record **On Hold** state. If you have customized state values for your Incident table, you can map them to the AI specialist's states here.
        -   **Default routing decision**: Determine whether an AI specialist should attempt to resolve a case outside of the assignment group's scope or reassign it to another assignment group. You can also specify in the following routing criteria section different categories of tasks for the AI specialist to attempt or reassign.
        -   **Routing criteria**: Categories of task specifying whether they should attempt resolution or reassign.
    -   **Investigate and resolve: Configure the following details on how the AI specialist investigates to find relevant solutions and resolve the issue.**
        -   **Knowledge sources**: Select search profiles and knowledge base **sys\_ids** to define how the AI specialist retrieves knowledge articles. AI search profiles can include sources such as knowledge articles, ServiceNow documentation, or specific tables. You can create AI Search profiles specifically for your AI specialists. To customize what information your AI specialist accesses, add search profiles with the pre-installed ones or remove the pre-installed ones. You must have at least one search profile selected for the AI specialist to complete the **Investigate and resolve** task.

            **Note:** If you include a table as a search source but don't grant the AI specialist access through its assigned roles, it can't search that table.

        -   **Automatically create KFT records**: Enable if you want the AI specialist to create a KB Feedback Task record after proposing a solution without an existing knowledge article.
        -   **Research depth**: Select how extensively the AI specialist must gather and analyze data during investigation.
        -   **Pre resolution condition**: The conditions that must be true before the AI specialist will resolve the ticket. These are fields that get filled in after a ticket has been submitted.
        -   **Execution mode**: Determine how autonomously the AI specialist should act. **Autopilot** mode grants the AI specialist the ability to mark a ticket as resolved once resolution steps are sent. **Copilot** mode requires human acceptance of its resolution proposal.
        -   **Auto-submit catalog requests**: Enable AI specialists to submit catalog items on behalf of the user without an additional confirmation step.
    -   **Response formatting: Configure the details on how the AI specialist communicates to keep requesters informed through communication channels.**
        -   **Inbound channels**: Select the inbound channels such as Activity stream through which the AI specialist can receive messages from requesters.
        -   **Outbound Channels**: Select the outbound channels the AI specialist uses to send responses or notifications. You can select channels such as Activity stream, email, portal, or phone.
        -   **Internal communication when confidence is low**: Enable the AI specialist to log its solution as a work note rather than proposing it directly.
        -   **Response templates**: Write the template for what the AI specialist should say to communicate to the user. You can set response templates for three different AI specialist states: Awaiting Info, Solution Proposed, and Reassign to Human. You can format your message using the editor to include things like bold text, specific fonts, tables, highlighting, links, and bullets.
    -   **Reassign: Configure the following details on how the AI specialist directs unresolved incidents to the correct team or agent for timely resolution.**
        -   **Maximum number of interactions before escalation**: Set how many times to contact the requester before sending to a human agent. Enter a number greater than zero.
        -   **Reassign on follow-up question**: Enable this option to send the ticket to a human agent when the requester asks a follow-up question. Turning off the option lets the AI specialist handle follow-ups.
        -   **Choose where to reassign records**: Select the assignment group to reassign the ticket after an AI specialist has reviewed it and chosen to reassign it.
        -   **Cross-group reassignment**: Enable the AI specialist to recommend reassigning an incident to a different assignment group. The AI specialist never reassigns an incident to a different assignment group on its own.
        -   **Cross-group confidence threshold**: Set the confidence threshold for whether an incident belongs to a specific other assignment group.
6.  Select **Save** to save your changes.

    You can make additional changes to your AI specialist before selecting save. Changing tabs in the AI specialist guided setup won't lose your changes.

    If you don't select **Save** before navigating to a new page or closing the browser, your changes are lost.



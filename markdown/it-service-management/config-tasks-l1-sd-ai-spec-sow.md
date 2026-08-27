---
title: Configure L1 IT Service Desk AI Specialist tasks
description: Select tasks that the L1 IT Service Desk AI Specialist is capable of.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/config-tasks-l1-sd-ai-spec-sow.html
release: australia
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 6
breadcrumb: [Configure, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Configure L1 IT Service Desk AI Specialist tasks

Select tasks that the L1 IT Service Desk AI Specialist is capable of.

## Before you begin

Role required: sn\_itsm\_common.sn\_service\_desk\_manager or admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace**.

2.  On the Homepage, in the **L1 Service Desk AI Specialist** card, select **View details**.

    The L1 IT Service Desk AI Specialist setup page displays the following sections that you can select to review and configure the details:

    -   Profile
    -   Tasks
    -   Test
3.  Select **Tasks** to review or configure the following tasks on how the L1 IT Service Desk AI Specialist makes decisions, acts, and interacts with workflow.

    1.  Configure the Classify and assign section.

        Configure how the L1 IT Service Desk AI Specialist identifies incidents, classifies them, and assigns a specific incident type for follow-up.

        -   **Table**: Select the table where resolution workflows will run.
        -   **Fields to predict**: Select the fields the AI specialist should classify when they are empty.
            -   Category
            -   Subcategory
            -   Service
            -   Service offering
            -   Configuration item
        -   **Similar records search profile**: Select the AI Search profile to be used for fetching similar records.
        -   **Override existing field values with predictions**: When enabled, AI predictions from similar records can override existing service, offering, and CI values on the incident. When disabled, predictions only fill empty fields.
    2.  Configure the Triage and diagnose section.

        Configure the following details how the L1 IT Service Desk AI Specialist analyzes the incident for accurate handling.

        -   **Field to use**: Select the record fields which the L1 IT Service Desk AI Specialist uses to analyze next steps.
        -   **Use attachment content**: Turn on to enable the L1 IT Service Desk AI Specialist to review the content of attached files as part of incident triage and diagnosis.
        -   **Map L1 Service Desk AI Specialist states to record states**: Map the states of the L1 IT Service Desk AI Specialist execution to the states of the incident record.

            For example, the L1 IT Service Desk AI Specialist **Awaiting info** state can be mapped to the Incident record **On Hold** state. If you have customized state values for your Incident table, you can map them to the L1 IT Service Desk AI Specialist states here.

        -   **Router \(recommended\)** uses your configured routing decision criteria. **Script** runs a custom script.

    3.  Configure the Investigate and resolve section.

        Configure how the L1 IT Service Desk AI Specialist investigates to find relevant solutions and resolve the issue.

        -   **Knowledge sources**: Select a search profile to define how the L1 IT Service Desk AI Specialist retrieves knowledge articles for investigation and resolution. This ensures relevant, accurate content is used to support incident handling.

            AI search profiles can be configured to include sources such as Knowledge articles, ServiceNow documentation, or specific tables. You can create new AI Search profiles specifically for your L1 IT Service Desk AI Specialist.

            To customize the information your L1 IT Service Desk AI Specialist has access to, you can add search profiles along with the pre-installed ones, or you can remove them. You must have at least one search profile selected for the L1 IT Service Desk AI Specialist to complete the Investigate and resolve task.

            **Note:** If you include a table from your instance as a search source, but you don't grant the L1 IT Service Desk AI Specialist access to the table with its assigned roles, it can't search on that table.

        -   **Automatically create KFT records**: When enabled, the L1 IT Service Desk AI Specialist automatically creates a KB Feedback Task \(KFT\) for solution\_proposed resolutions where no existing KB article was referenced. This helps surface knowledge gaps for content authors to address.
        -   **Research depth**: Select how extensively the L1 IT Service Desk AI Specialist must gather and analyze data during investigation.
            -   Low: Faster results, less detail.
            -   Medium: Balanced results, moderate depth.
            -   High: Slower results, more detail.
        -   **Pre resolution condition**: Encoded query to validate the record against the table. The conditions that need to be true before the L1 IT Service Desk AI Specialist will resolve the ticket. These are fields that get filled in after a ticket has been submitted.
        -   **Execution mode**: Determine how autonomously the L1 IT Service Desk AI Specialist should act. **Autonomous** mode grants the L1 IT Service Desk AI Specialist the ability to mark a ticket as resolved once resolution steps are sent. **Supervised** mode requires human acceptance of its resolution proposal.
        -   **Auto-submit catalog requests**: When enabled, the L1 IT Service Desk AI Specialist automatically submits catalog items that have no required variables on behalf of the user. When disabled, the L1 IT Service Desk AI Specialist always returns the catalog URL for the user to review and submit manually.
        -   **Flag high-risk resolution steps**: When on, resolutions requiring elevated access, backend changes, or irreversible actions are sent to a service desk agent instead of the requester.
    4.  Configure the Response formatting section.

        Configure the following details on how the L1 IT Service Desk AI Specialist communicates to keep the requesters informed through communication channels.

        -   **Inbound channels**: Select the inbound channels such as Activity stream through which the L1 IT Service Desk AI Specialist can receive messages from requesters.
        -   **Outbound Channels**: Select the outbound channels the L1 IT Service Desk AI Specialist uses to send responses or notifications. You can select channels such as Activity stream, email, portal or phone and set the preferred message format such as HTML or plain text.
        -   **Internal communication when confidence is low**: Enable to allow the L1 IT Service Desk AI Specialist to log its solution as a work note rather than proposing it directly.
        -   **Response templates**: Write the template for what the L1 IT Service Desk AI Specialist should say to communicate to the user. You can set response templates for three different AI specialist states: Follow up, Propose a solution, and Reassign to human. You can format your message using the WYSIWYG editor to include things like bold text, specific fonts, tables, highlighting, links, and bullets.
    5.  Configure the Reassign section.

        Configure the following details on how the L1 IT Service Desk AI Specialist directs unresolved incidents to the right team or agent for timely resolution.

        -   **Maximum number of interactions before escalation**: Set how many times to contact the requester before sending to an agent. Enter a number greater than zero.
        -   **Reassign on follow-up question**: Option to send the ticket to a human agent when the requester asks a follow-up question. Turning off the option lets the L1 IT Service Desk AI Specialist handle follow-ups.
        -   **Stuck monitor filter**: Set the filter for incidents that are considered stuck and need escalation.
        -   **Choose where to reassign records**: Select the assignment group, or specific person to reassign the ticket to after the L1 IT Service Desk AI Specialist has reviewed it and chosen to reassign it.
        -   **Cross-group reassignment**: When a different assignment group consistently resolves similar resolved incidents, control whether the L1 IT Service Desk AI Specialist surfaces a routing recommendation. Off: none. Recommend only: post a recommendation and unassign the L1 IT Service Desk AI Specialist; assignment group is never changed.
        -   **Cross-group confidence threshold**: Minimum confidence \(0-1\) that a single different assignment group is the consistent resolver before a recommendation is surfaced.
4.  Select **Save** to save your changes.

    You can make additional changes to your L1 IT Service Desk AI Specialist before selecting save. Changing tabs in the L1 IT Service Desk AI Specialist guided setup won't lose your changes.

    However, if you don't select **Save** before navigating to a new page or closing the browser, your changes are lost.



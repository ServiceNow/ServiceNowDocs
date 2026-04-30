---
title: Viewing incident record information using the Contextual side panel
description: View the incident record information, such as caller details and assets, from the Contextual side panel. Use this information to help manage an incident more efficiently.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Incident Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Viewing incident record information using the Contextual side panel

View the incident record information, such as caller details and assets, from the Contextual side panel. Use this information to help manage an incident more efficiently.

Select the **Record information** \(![Record information](../image/mim-record-info.png)\) icon on the Contextual side panel to view the incident information. The record information side panel includes this following information.

## Active calls

The Active calls card displays active conference calls that are currently in progress for major incidents. This card is displayed only for major incident records and if the Major Incident Management for Service Operations Workspace \(sn\_sow\_mim\) plugin is installed and active. For more information, see [Setting up Major Incident Management in Service Operations Workspace](setup-mim-sow.md).

A maximum of five collaboration records are displayed on this card. You can select the call record links displayed on this card to join the calls. You can use the **Collaborate** side panel tab to view and manage additional call record information.

**Note:**

For Twilio calls, plain text is displayed instead of a link. In such case, you can join the call using the **Collaborate** side panel tab.

The collaboration information is retrieved from the Collaboration services integration with Service Operations Workspace.

## SLAs and timings

The SLAs and timings card includes the following information:

-   Major incident duration – Time duration since the incident has been promoted, created, or accepted as a major incident. This field is visible only if Major Incident Management for Service Operations Workspace is installed and active.
-   Response SLA – The Task service level agreement \(SLA\) stage according to the configured Incident Response SLA timer configuration. Displays the time left to respond to an incident before the task SLA is breached.
-   Resolution SLA – The Task SLA stage according to the configured Incident Resolution SLA timer configuration. Displays the time left to resolve an incident before the task SLA is breached.
-   View all SLAs – All SLAs associated with the incident record.

    **Note:** This option is visible only if there is at least one SLA associated with the current incident task.


## Caller

The Caller card displays quick information about the caller, such as name, local time, department, and location. You can also select the **Preview caller** \(![Preview caller icon](../image/inc-preview-record.png)\) icon to preview the caller record. Select **Open record** to open the caller record on a separate tab. You can also select **Contact** to view all details about the caller.

**Note:** The caller card is displayed first on the Record information side panel, if you are a tier 1 agent.

You can view the VIP field decorator if the caller is a VIP user. The VIP field decorator also appears for the **Caller** field in the **Details** tab.

You can select the following links to get additional record information specific to the caller, if necessary:

-   Caller assets – List of the caller's assets \(CIs\).
-   Recent interaction – List of recent interactions with the caller that have been created in the last seven days.  You can view up to ten interaction records on the card. Select **View all** to view the list of all interactions on a separate tab.

    **Note:** For interaction records, the **Assigned to** user is considered as the caller.

-   Recent incidents - List of recent incidents associated with the caller that have been created in the last seven days. You can view up to ten incident records on the card. Select **View all** to view the list of all incidents on a separate tab.

## Origin

The origin card displays the information related to the origin record. An origin record is the record from which the incident record is created such as change request, interaction or problem.

![Origin card](../image/sow-origin-card-new.png "Origin card")

The card displays the following information about the origin record:

-   State - State of the origin record.
-   Number - Number of the origin record.
-   Opened by - User who created or opened the origin record
-   Type - Channel type of origin record. For example, if the origin is an interaction record, the type can be Chat
-   Short description - Short description of the origin record.
-   The following options are available if the incident is created from an interaction record:
    -   View chat transcript - Select **View chat transcript** to view the chat history with the caller of the interaction record. You can perform additional activities such as maximize or minimize the chat window. This option is available only if the interaction record is of **Chat** type and in **Closed complete** or **Closed Abandoned** state.
    -   View work notes - Select **View work notes** to view the work notes activity history of the interaction record.

When an incident is created from an interaction record, the following features are applicable:

-   When an incident record created from an interaction record is resolved, the interaction record is automatically set to **Wrap up** or **Closed complete** state. An admin role user must set the **Auto close the origin interaction** \(**sn\_sow\_inc.autoclose\_origin.interaction**\) system property to `true` to enable this feature. The **Close interaction from incident** business rule checks the following conditions and updates the interaction record to **Wrap up** or **Closed complete** state:
    -   When the **Auto close the origin interaction** \(**sn\_sow\_inc.autoclose\_origin.interaction**\) system property is set to `true` and the **Fallback Timeout for interactions in Wrap Up** scheduled script is active, the interaction record is moved to **Wrap up** state.
    -   When the **Auto close the origin interaction** \(**sn\_sow\_inc.autoclose\_origin.interaction**\) system property is set to `true` and the **Fallback Timeout for interactions in Wrap Up** scheduled script is inactive, interaction record is moved to **Closed complete** state.
-   You can add multiple related interaction records to an incident using the **Add** option on the Interaction related list in the **Related records** tab of an Incident record page.

## Assigned to

The Assigned to card displays the assignment status of the incident record. Select **Assign to** to assign the incident record to you. You can select the **View additional collaborators** link to view the list of collaborators associated with the incident record in a modal experience. The list of collaborators is retrieved from the following data sources:

-   Historical **Assigned to** users for the incident or incident tasks except the current **Assigned to** user.
-   Users who have added comments and work notes to the major incident record. This data source is applicable only for major incidents.
-   Collaborators from the collaboration channels that are initiated from the **Collaborate** side panel. This information is retrieved using the collaboration APIs.

You can view a list of five collaborators on a page at a time.

**Parent Topic:**[Incident Management in Service Operations Workspace](incident-sow.md)

**Related topics**  


[Create an incident in Service Operations Workspace](../task/create-incident-sow.md)

[View and update incident information on the Overview tab](../task/view-update-inc-overview-tab.md)

[Work on an incident list page in Service Operations Workspace](../task/work-incident-list-page-sow.md)

[Work on an incident record in Service Operations Workspace](../task/work-on-incident-sow.md)

[Close resolved incident](../task/close-resolved-incident-sow.md)

[Remedial actions using Playbook](remedial-actions-playbook.md)

[Reopen an incident in Service Operations Workspace](../task/reopen-incident-sow.md)

[Incident Management in Service Operations Workspace reference](sow-im-reference.md)


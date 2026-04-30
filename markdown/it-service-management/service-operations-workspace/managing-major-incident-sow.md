---
title: Managing a major incident record
description: Manage a major incident record with a playbook or the various tabs on the major incident record page.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Major Incident Management in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Managing a major incident record

Manage a major incident record with a playbook or the various tabs on the major incident record page.

Based on the information displayed on different tabs, an agent can propose a major incident using the **Propose Major Incident** option. A major incident manager reviews the information on the **Overview** tab, such as the location information, and then accepts or rejects the major incident proposal. After a proposal is accepted, the major incident manager uses the **Promote Major Incident** option to promote the candidate to a major incident.

After an incident is promoted to a major incident, each tab on a Major Incident record page contains information about the major incident. You can use the various options and the action menu to manage the major incident process and view incident information on the following:

-   Overview tab
-   Details tab
-   Communicate tab
-   Related records tab
-   Playbook tab
-   Contextual side panel

-   **Overview tab**

    The **Overview** tab displays the incident information in the following sections:

    -   Summary – Basic incident information, such as short description, description, impact, urgency, and state.
    -   Impact:
        -   Impact summary - Impact summary information, such as business impact, configuration item, service, and service offering.
        -   Location – The location of the caller on the world map, the number of locations, and the number of users. This information is only displayed for a major incident and if you have the major\_incident\_manager role.
        -   Affected CIs – The number of CIs affected by the incident.
        -   Impacted Services/CIs – The number of CIs and services impacted by the incident.
        -   Assets – The number of assets associated with the incident.
    -   Cause – The probable cause of the incident.
    -   Resolution – Incident resolution-related information, such as resolution code and resolution notes, once the incident is resolved.
    On the Activity section, you can view all comments, work notes, actions taken, and composed emails. This section also includes user activities, such as a change in the state and the assignment group. In the Compose section, you can add comments, work notes, and actions taken, as well as compose emails.

    For more information on the **Overview** tab, see [View and update incident information on the Overview tab in SOW](../task/view-update-inc-overview-tab.md).

-   **Details tab**

    The **Details** tab displays detailed information about the incident, such as category, subcategory, impact, related record, assignment group, watch list, cause, and resolution. For more information on the **Details** tab, see [Incident Management in Service Operations Workspace](incident-sow.md).

-   **Communicate tab**

    The **Communicate** tab displays the list of communication tasks with various options that are used to maintain communications with the stakeholders for major incidents. For more information on the options available on the **Communicate** tab, see [Communicating with stakeholders about incidents and major incidents in SOW](communicating-with-stakeholders-sow.md).

-   **Related records tab**

    The **Related records** tab provides the related lists containing records associated with the major incident record. For example, task SLAs, child incidents and affected CIs.

    In the Child incidents related list, you can use the **Find similar** option to find multiple similar incidents and add them as child incidents to a major incident or major incident candidate record.

    Similar incidents are retrieved based on the similarity solution definition that can be configured to train on various fields such as **Short description** and **Description**. Adding the similar incidents as child incidents to the major incident record ensures avoiding creation of multiple major incident records for the same issue.

-   **Playbook tab**

    The **Playbook** tab displays the information of the playbooks available for Major Incident Management. For each playbook, you can select to work with the playbook to manage major incidents. For more information, see [Managing major incidents using playbooks](managing-mi-playbook-sow.md).

-   **Contextual side panel options**

    On the Contextual side panel, you can use the following options:

    -   Major Incident Playbook – Select the **Major Incident Playbook** \(![Major incident playbook](../image/mim-playbook-icon.png)\) icon to launch the playbook side panel. The playbook provides a guided approach to the entire major incident process. It provides a way to visualize business process workflows for major incidents in a simple, task-oriented view. The playbook contains the following two tabs:
        -   Current – List of major incident playbooks running currently.
        -   History – Historical list of major incident playbooks.
    -   Recommended actions – Select the **Recommended Actions** \(![Recommended actions for ITSM](../image/mim-sow-ra-itsm.png)\) icon to launch the **View recommendation** side panel. The side panel lists all the recommended actions for major incidents. When an incident is promoted to a major incident and doesn’t have a problem record associated with it, this tab displays a card with the **Create a problem** option to create a problem record.

        You can also configure whether the incident field information is copied automatically when a problem record is created by using the **List of attributes \(comma-separated\) that will be copied from the incident to create a new problem** \(**com.snc.problem.create\_from\_incident.attributes**\) system property. For more information, see [Create a problem](../../problem-management/task/create-a-problem-v2.md).

    -   Record Information – Select the **Record information** \(![Record information](../image/mim-record-info.png)\) icon to view the incident record information on the side panel. The record information side panel includes the following information:

        -   Active calls – Details of the active conference calls for major incidents. You can select the call record to start a conference call.
        -   Caller details – Name, local time, address, email id, and other caller information. Select the **Contact** option to view the caller details and caller assets. You can also see recent interactions and incidents with the caller.
        -   SLAs and timing – Duration of time since a major incident has occurred, as well as the state of the response and the resolution SLAs for the major incident. You can select **View all SLA** to see all the task SLAs associated with the incident.
        -   Assign to – The assignment status of the incident. You can select the **Assign to** option to assign the incident to yourself. You can select the **View additional collaborators** option to view the list of collaborators associated with the incident.
        For more information on the record information in the Contextual side panel, see [Viewing incident record information using the Contextual side panel](view-inc-record-info-contextual-sidepanel.md).

    -   Collaborate – Select the **Collaborate** \(![Collaborate icon](../image/mim-collaborate-icon.png)\) icon to open the **Collaborate** side panel tab. This tab displays the following tabs:
        -   Call – Call-related information for the upcoming, pending, overdue, or active calls with the collaborators such as status and due date with time duration. You can select **Start** to initiate that call. You can also select the **Initiate collaboration** \(![Add call](../image/mim-add-call-chat-icon.png)\) icon to create a call using various communication channels such as Zoom and Webex.
        -   Chat - Chat-related information, such as name, number of participants, and due date, for upcoming, pending, overdue, or active chats with collaborators. You can select **Open discussion** to start that chat. You can select the **Initiate collaboration** \(![Add call](../image/mim-add-call-chat-icon.png)\) icon to create a chat using various communication channels, such as Microsoft Teams and Slack.
    -   On call – Select the **Experts on-call** \(![On call icon](../image/mim-on-call.png)\) icon to identify and contact available on-call members of a support group to resolve an issue.

-   **[Propose a major incident](../task/propose-major-incident-sow.md)**  
Propose an incident to a major incident candidate based on the incident information.
-   **[Managing major incidents using playbooks](managing-mi-playbook-sow.md)**  
Manage the major incident life cycle and process using Major Incident Playbooks from the contextual side panel of an incident record page.
-   **[Promote a major incident](../task/promote-major-incident-sow.md)**  
Review the information of the proposed major incident candidate and promote it to major incident using the Major Incident Playbook.
-   **[Communicating with stakeholders about incidents and major incidents in SOW](communicating-with-stakeholders-sow.md)**  
Use the **Communicate** tab to create and manage all communications with stakeholders during the various phases of an incident or a major incident.
-   **[Collaborate with stakeholders during a major incident](../task/collaborate-stakeholders-mim-sow.md)**  
Collaborate with the required stakeholders during the various phases of a major incident to discuss and resolve the incident quickly. You can initiate a chat or make conference calls using a service provider to communicate with stakeholders.
-   **[Resolve and close a major incident](../task/resolve-close-mim-sow.md)**  
Resolve a major incident to reinstate service after the interruption.
-   **[Review and update a post incident report](../task/review-update-pir-mim-sow.md)**  
Review a post incident report \(PIR\) using the **Post Incident Report** tab. A PIR helps you review and understand the cause of the major incident and the actions taken by the teams to resolve the incident. This helps prevent the issue in the future.

**Parent Topic:**[Major Incident Management in Service Operations Workspace](mim-in-sow.md)


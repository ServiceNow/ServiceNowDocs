---
title: Collaborate with stakeholders during a major incident
description: Collaborate with the required stakeholders during the various phases of a major incident to discuss and resolve the incident quickly. You can initiate a chat or make conference calls using a service provider to communicate with stakeholders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/collaborate-stakeholders-mim-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing a major incident record, Major Incident Management in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Collaborate with stakeholders during a major incident

Collaborate with the required stakeholders during the various phases of a major incident to discuss and resolve the incident quickly. You can initiate a chat or make conference calls using a service provider to communicate with stakeholders.

## About this task

Collaboration services provide a way to communicate and collaborate in real time to resolve incidents. For more information on the integration and features of Collaboration services available in Service Operations Workspace, see [Collaboration in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/collaboration-sow.md).

## Before you begin

Role required: major\_incident\_manager, itil, ia\_admin, or admin

## Procedure

1.  On the incident record, select the **Collaborate** \(\[Omitted image "mim-collaborate-icon.png"\] Alt text: Collaborate icon\) icon on the contextual side panel to open the collaborate tab on the side panel.

    The collaborate tab displays the following tabs:

    -   Call – Includes a list of call records and call-related information, such as status and due date with time duration, for the upcoming, pending, overdue, and active calls with the collaborators.
    -   Chat - Includes a list of chat records and chat-related information, such as name and number of participants and due date with time duration, for upcoming, pending, overdue, and active chats with collaborators.
2.  Select the **Initiate collaboration** \(\[Omitted image "mim-add-call-chat-icon.png"\] Alt text: Add call\) icon.

3.  Collaborate using chat.

    1.  Select any one of the following chat options:

        -   Select **Start Sidebar discussion** to open the conversation on a sidebar chat.
        -   Select **MS Teams chat** to open the conversation on Microsoft Teams.
        **Note:**

        -   The chat application must be configured with Service Operations Workspace.
        -   Slack channels aren't supported.
        -   Users with incident\_write or itil role assigned to a Collaborate task such as call or chat, can now view the existing Collaborate card and start a sidebar discussion, Microsoft Teams chat, or call.
    2.  On the pop-up window, fill in the details.

        |Field|Description|
        |-----|-----------|
        |Record number|Incident record number associated with the collaboration chat. The incident record is selected by default.|
        |Subject|Subject or title for the collaboration chat.|
        |Add participants|User, user group, or list of recipients who must attend the collaboration chat.|
        |Include a brief message for participants|Brief description about the issue to be discussed in the chat.|

    3.  Select **Start Discussion**.

    The chat application opens with the selected participants.

4.  Collaborate using call.

    1.  Select one of the following call options.

        -   Start Webex meeting
        -   Start MS teams meeting
        -   Start Twilio meeting
        -   Start Zoom meeting
        **Note:** The selected call channel applications must be configured for Service Operations Workspace.

        .

    2.  On the pop-up window, fill in the details.

        |Field|Description|
        |-----|-----------|
        |Conference bridge|Call channel used for collaboration.|
        |Title|Subject or title for the collaboration call.|
        |Add participants|User, user group, or list of recipients who must attend the collaboration call.|
        |Provide a brief description, this note will be stored in the conference record|Brief description about the issue to be discussed in the call.|

    3.  Select **Start**.

        The call starts with the selected participants.


-   **[Create adhoc communication and collaboration using the Related record tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-adhoc-comm-collab-mim-sow.md)**  
Create adhoc communication and collaboration using the incident communication plan related list on the **Related records** tab of an incident record page.

**Parent Topic:**[Managing a major incident record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/managing-major-incident-sow.md)


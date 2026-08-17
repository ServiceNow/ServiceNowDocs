---
title: Collaborate on a task record using Microsoft Teams in Service Operations Workspace
description: Start or import a Microsoft Teams chat from a task record in Service Operations Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/service-operations-workspace/start-msteams-chat-sow.html
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow integrations with Microsoft Teams in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Collaborate on a task record using Microsoft Teams in Service Operations Workspace

Start or import a Microsoft Teams chat from a task record in Service Operations Workspace.

## Before you begin

Role required: itil or admin

Before you begin, make sure that the Microsoft Teams application is configured for your ServiceNow instance. For more information on configuration, see and the Microsoft Teams integration setup documentation.

## About this task

When you view or import a Microsoft Teams chat conversation for a task record, the record details are displayed in the **Details** section of the **MS Teams Import** tab. For information about configuring these details, see [Configure the task record information in the MS Teams Import tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/service-operations-workspace/configure-record-details-import-chat-sow.md).

## Procedure

1.  Open a task record, for example, incident.

2.  From the Sidebar, select the collaborate icon \(\[Omitted image "collab-icon-02.png"\] Alt text: Collaborate\).

3.  To view a chat conversation, select the more options icon \(\[Omitted image "more-options-card.png"\] Alt text: more options icon\) on the chat and select **View chat**.

4.  To start a chat conversation, perform the following actions.

    1.  In the **Collaborate** panel, select the plus sign \(+\), and select **Start Microsoft Teams chat**.

    2.  In the **Start Microsoft Teams chat** dialog box, specify the participants.

    3.  To specify more chat options, select **Show more chat options** and specify a client.

        You can choose Microsoft Teams application or the Microsoft Teams web application.

    4.  Select **Start Chat**.

        -   A chat conversation is initiated in Microsoft Teams.
        -   All automatic chats are automatically imported to the **Collaborate** panel.
5.  To view a chat conversation, select the more options icon \(\[Omitted image "more-options-card.png"\] Alt text: more options icon\) on the chat and select **View chat**.

6.  To import a chat conversation, perform one of the following actions.

<table id="choicetable_tnl_jfr_vsb"><thead><tr><th align="left" id="d292714e221">

Option

</th><th align="left" id="d292714e224">

Description

</th></tr></thead><tbody><tr><td id="d292714e230">

**Import a chat from any conversation**

</td><td>

1.  Select the plus sign \(+\) and select **Import Microsoft Teams chat**.
2.  Under the **Choose a conversation to view details** section, select a conversation that you want to import.
3.  Select the chat and select **Import**.


</td></tr><tr><td id="d292714e260">

**Import a chat from a conversation in which you are a member**

</td><td>

1.  From the conversation that you're a member of, select the more options icon \(\[Omitted image "more-options-card.png"\] Alt text: more options icon\) and select **View chat**.
2.  Select the filter chat messages icon \(\[Omitted image "filter-icon.png"\] Alt text: filter chat messages icon\) and select the type of messages you want to view.
3.  Select the required messages and select **Import**.


</td></tr></tbody>
</table>    Imported chats are reflected in the activity stream of the task record.


**Parent Topic:**[ServiceNow integrations with Microsoft Teams in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/service-operations-workspace/msteams-sow.md)


---
title: Request based chat - Start and import chat from classic view
description: Initiate a conversation with the requester to resolve the ticket.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent actions, Use ITSM and HRSD integrations with Microsoft Teams, Use Microsoft Teams integration for Employee Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Request based chat - Start and import chat from classic view

Initiate a conversation with the requester to resolve the ticket.

You must have the "write" role to use the **Start Microsoft Teams chat** and **Import messages from Microsoft Teams** features for an incident, request, change request and a catalog task. This role is available when you activate the ITSM roles plugin, or for all the instances starting the Madrid release.

|Record|Role|Plugin|
|------|----|------|
|Incident|sn\_incident\_write|ITSM Roles - Incident Management \(com.snc.itsm.roles.incident\_management\) plugin|
|Change Request|sn\_change\_write|ITSM Roles — Change Management \(com.snc.itsm.roles.change\_management\) plugin|
|Request|sn\_request\_write|ITSM Roles — Request Management \(com.snc.itsm.roles.request\_management\) plugin|
|HR Case|sn\_hr\_core.case\_writer|Human Resources Scoped App — Employee Relations \[com.sn\_hr\_employee\_relations\] plugin|

-   **[Request-based chat - Start and import chat from field decorator](../task/initiate-chat-record-field-decorator.md)**  
Interact with a requester in Microsoft Teams from the chat icon from the workspace to quickly resolve the ticket.
-   **[Request-based chat - Start and import chat from Start Microsoft Teams chat action](../task/initiate-chat-record.md)**  
Interact with a requester in Microsoft Teams for an issue related to an incident, request item, change request, and HR case records to quickly resolve the ticket.
-   **[Import messages from a ticket manually](../task/import-messages.md)**  
You can import the conversation with a user from Microsoft Teams and append them in the **Comments** to store all the important messages in the ServiceNow instance.

**Parent Topic:**[Agent actions](agent-sn-ms-teams.md)


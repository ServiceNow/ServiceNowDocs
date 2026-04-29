---
title: Update chat credentials with Azure GCC URL
description: Update the Azure URL in the chat credentials of GCC customers. Enable GCC customers to start chat and import chat conversations from Microsoft Teams to the ServiceNow instance.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Request-based chat with Microsoft Teams for GCC-H or DoD, Integrating ServiceNow with Microsoft Teams for GCC-H or DoD, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Update chat credentials with Azure GCC URL

Update the Azure URL in the chat credentials of GCC customers. Enable GCC customers to start chat and import chat conversations from Microsoft Teams to the ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `http_connection_list.do`.

    The HTTP\(s\) Connection \[http\_connection\_list.do\] table appears.

2.  Open the Chat Credential record with the connection alias sn\_tcm\_collab\_hook.MS\_Teams\_Chat\_Credentials.

3.  In the **Connection\_URL** field, enter the URL `https://graph.microsoft.us/`.

    **Note:** For DoD customers, enter the URL `https://dod-graph.microsoft.us`.

4.  Select **Update**.


**Parent Topic:**[Integrating Request-based chat with Microsoft Teams for GCC-H or DoD](../concept/ec-teams-request-based-chat-integration-gcch.md)


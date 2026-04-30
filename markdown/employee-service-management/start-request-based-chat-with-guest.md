---
title: Request-based chat - Start chat with guest user from a record
description: Start a Microsoft Teams chat with the guest user of an external and allowed domain through a record.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent actions, Use ITSM and HRSD integrations with Microsoft Teams, Use Microsoft Teams integration for Employee Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Request-based chat - Start chat with guest user from a record

Start a Microsoft Teams chat with the guest user of an external and allowed domain through a record.

## Before you begin

The guest user must be authenticated with chat access. For more information, see [Enable chat access for guest users](enable-guest-chat-access-st.md) for self-configured app and [Enable chat access for a guest user](enable-guest-chat-access-mt.md) for pre-published app instances.

The guest users list is fetched from the Microsoft Azure AD. For more information, see [Guest access in Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/guest-access).

Role required: agent

## About this task

For information about starting a chat with an external user who is not added in the allowed-guest domains list, see [Add or invite people outside your Teams org to a chat](https://support.microsoft.com/en-us/office/add-or-invite-people-outside-your-teams-org-to-a-chat-6897ab47-9f60-4db6-8b95-18599714fe57).

## Procedure

1.  Launch Microsoft Teams.

2.  Navigate to **ServiceNow for Microsoft Teams** &gt; **Employee Center** &gt; **My Requests**.

3.  Open the ticket that you want to work on in your ServiceNow instance.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Assignment group|Search and select **Teams group**.|
    |Short description|Description of the chat purpose.|

5.  Right-click in the form header and select **Save**.

6.  Select **Start Microsoft Teams Chat**.

7.  Select the user that you want to chat with.

    You can select the requester and employees, or multiple guests from different domains.

8.  Select **Start Chat**.

    On the web client, the domain associated Tenant ID appends to your Microsoft Teams URL.

    The chat opens in the Microsoft Teams application.


## Result

All team members see an announcement message in the Microsoft Teams channel thread that the team owner has added a guest and the guest name is listed. A tag in the upper-right corner of the channel thread indicates the number of guests on the team and a **\(Guest\)** label appears next to each guest name.

**Note:**

A tag with the label **External** indicates that a user is guest and not present in the allowed-domain.

**Parent Topic:**[Agent actions](../concept/agent-sn-ms-teams.md)


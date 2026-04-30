---
title: Enable or configure the Microsoft Teams integration
description: Enable or configure the Microsoft Teams integration as part of integrating Sidebar with Microsoft Teams.
locale: en-US
release: yokohama
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Sidebar and Microsoft Teams, Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Enable or configure the Microsoft Teams integration

Enable or configure the Microsoft Teams integration as part of integrating Sidebar with Microsoft Teams.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select Sidebar.

3.  On the Integrations card:

    -   If Sidebar and Microsoft Teams are not already integrated, select **Set up**.
    -   If Sidebar and Microsoft Teams are already integrated, select **View configuration** from the Manage drop-down list.
4.  On the Microsoft Teams Integration screen, slide the activate toggle to allow or prevent Microsoft Teams users from participating in Sidebar discussions.

    -   When this is switched on, Microsoft Teams users that previously had access to Sidebar will regain access and any Microsoft Teams users that are newly included will gain access to Sidebar.
    -   When this is switched off:
        -   Microsoft Teams users that previously had access to Sidebar will no longer have access to Sidebar.
        -   Any Microsoft Teams users that are newly included will not gain access to Sidebar.
        -   Existing discussions will become inactive in Microsoft Teams. Microsoft Teams users will still be able to access older messages in a Microsoft Teams group chat, but any messages sent in those group chats will not be sent to Sidebar.
        -   Existing discussions will remain active for Sidebar users.
5.  Enter **Client Secret**, **Callback URL**, and **Redirect URL**.

    **Note:** For more information about the Microsoft Azure Portal fields needed, see [Use the portal to create an Azure AD application](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

<table id="table_wc4_1zj_kvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application \(client\) ID

</td><td>

ID associated with the app created in the portal.

</td></tr><tr><td>

Directory \(tenant\) ID

</td><td>

ID associated with the Microsoft Teams organization that will be linked to Sidebar discussions.

</td></tr><tr><td>

App ID

</td><td>

ID used to subscribe to Sidebar conversations from Microsoft Teams.

</td></tr><tr><td>

Client Secret

</td><td>

Auto-assigned credentials used to authenticate the Microsoft Azure app with Microsoft. If this field is changed, then a new integration setup will be triggered.

</td></tr><tr><td>

Callback URL

</td><td>

Web location Microsoft Teams uses to send a response to Sidebar. For your own instance, add the value like https://your-instance.service-now.com/api/now/collaboration\_chat\_event\_processor/chats. If this field is changed, then a new integration setup will be triggered.

</td></tr><tr><td>

Redirect URL

</td><td>

Web page that appears after you successfully log in to Microsoft Teams. If this field is changed, then a new integration setup will be triggered.

</td></tr></tbody>
</table>6.  Select **Save**.



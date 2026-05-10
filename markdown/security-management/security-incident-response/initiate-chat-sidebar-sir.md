---
title: Start a Sidebar chat in Security Incident Response
description: Using Sidebar, security analysts can collaborate with others in real-time based on a Workspace task-based or interaction-based record. These Sidebar discussions facilitate the exchange of information and knowledge to help resolve issues faster and with higher-quality outcomes.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collaborate using conference call or chat in Security Incident Response, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Start a Sidebar chat in Security Incident Response

Using Sidebar, security analysts can collaborate with others in real-time based on a Workspace task-based or interaction-based record. These Sidebar discussions facilitate the exchange of information and knowledge to help resolve issues faster and with higher-quality outcomes.

## Before you begin

Role required: sn\_si.read

Verify that you have activated the Omni-Experience Standard Feature Set plugin. For more information, see [Installing Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/sidebar/install-sidebar.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select the List view ![list view icon](../image/listview-icon.png) icon.

3.  Open a security incident for which you want to initiate a sidebar discussion.

4.  Select **Collaborate**, and then select **Start Chat**.

    The Start a Sidebar discussion dialog box appears.

    **Note:** Sidebar's integration with Microsoft Teams enables Sidebar users and Microsoft Teams users to communicate with each other from their respective platforms. For more information, see [Sidebar and Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/sidebar/sidebar-teams-overview.md).

5.  On the Start a Sidebar discussion dialog box, fill in the fields.

<table id="choicetable_ps5_3w2_2cc"><thead><tr><th align="left" id="d306329e122">

Field

</th><th align="left" id="d306329e125">

Description

</th></tr></thead><tbody><tr><td id="d306329e131">

**Record number**

</td><td>

The task or incident number associated with the Sidebar discussion.

</td></tr><tr><td id="d306329e140">

**Subject**

</td><td>

Provide a title for the sidebar discussion.

</td></tr><tr><td id="d306329e149">

**Add participants**

</td><td>

Option to add participants for the sidebar discussion. If you have integrated sidebar chat with Microsoft Teams, you can also add participants from Microsoft Teams.**Note:**

-   You need to add at least one participant to create a new discussion.
-   If Sidebar and Microsoft Teams are integrated, Microsoft Teams users are differentiated from Sidebar users with a Microsoft Teams icon.
-   By default, all users who have read access to the SIR records will also have access to sidebar chats, but this can be controlled using member query. For more information, see [Configuring Sidebar member query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/sidebar/configure-sidebar-member-query.md).


</td></tr><tr><td id="d306329e179">

**Include a brief message**

</td><td>

Provide a brief summary about the issue to be discussed in the sidebar discussion.

</td></tr></tbody>
</table>    ![Initiate a Sidebar chat in Security Incident Response](../image/native-sidebar-chat.png "Initiate a Sidebar chat in Security Incident Response")

6.  Select **Start discussion**.

7.  You can perform additional configuration like quick actions.

    To limit the action usage, you can use the **Apply to group** field on the quick action page. For more information, see [Creating a quick action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ci-quick-actions-overview.md).


**Parent Topic:**[Collaborate using conference call or chat in Security Incident Response](../concept/collab-sir-call-chat.md)


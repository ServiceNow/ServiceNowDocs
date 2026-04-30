---
title: Email Interaction record page
description: The Email interaction record page enables customer service agents to work on incoming emails as interactions, similar to the chat and voice interaction record pages.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-28"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Email Interaction record page

The Email interaction record page enables customer service agents to work on incoming emails as interactions, similar to the chat and voice interaction record pages.

Email interactions help client support teams triage and obtain proper approvals before proceeding with any work on an account. Email interactions act as a staging record before agents create cases for additional work.

![The Email Interaction record page enables agents to work on incoming emails in the activity stream of an interaction record.](../image/email-interaction-record-page.png "Email Interaction record page")

## Email Interaction record page variant

The Email Interaction record page variant is included with the CSM Configurable Workspace application \(com.snc.uib.csm\_agent\_workspace\). This page variant includes the following settings.

<table id="table_zqv_lvv_q1c"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Enabling the **Active** check box makes the page variant available to the selected audience. The Email Interaction record page variant is inactive by default.The active setting combined with the page order determines the page that CSM Configurable Workspace uses to display record information. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the Email interaction record page variant is -1001.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The Email interaction record page variant has the following conditions:-   **table = interaction**: Limits the use of the Email interaction page variant to records from the Interaction \[interaction\] table.
-   **csm.isEmailInteractionVisible = true**: Checks the UX screen condition for the variable setting. If this variable is set to true, this page variant should be displayed.

If all of these conditions are met, the system displays the Email Interaction record page variant.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The Email Interaction record page does not have a defined audience.For more information, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr></tbody>
</table>To access the settings for this page variant:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the Record section of the Pages and variants list, select **Email Interaction page**.
4.  Select **Settings** at the top of the page.

## Email Interaction record page components

The Email Interaction record page includes the following components.

<table id="table_pk2_g1w_q1c"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Form heading

</td><td>

The form heading displays the interaction short description and also includes the action bar and record tags.

</td></tr><tr><td>

Record tags

</td><td>

Agents can create multiple tags for a record and then use the tags to group and organize records.For more information, see [Group and find records using tags in workspace](https://www.servicenow.com/docs/access?context=setting-record-tags-agent-workspace&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Action bar

</td><td>

The action bar contains the actions available to users while working on phone interaction records.-   **Create**: Create records related to the interaction such as cases, incidents, requests, and consumers.
-   **Save**: Save changes to the interaction record.
-   **Close**: Close the interaction record.
-   **More Actions**: Perform additional actions such as associating a record.

**Note:** The specific actions available are determined by factors such as the user role and other attributes.

</td></tr><tr><td>

Interaction details

</td><td>

The interaction details include information about the interaction including the account and contact, short description, and record state.

</td></tr><tr><td>

Activity stream

</td><td>

The activity stream component displays a list of activities occurring on a case record. This list can be collapsed to provide a quick view of case activities or expanded to provide more detail about individual activities.Agents can use the activity stream to compose work notes or emails.

For more information, see [Activity stream component](csm-front-line-case-page.md#section_ntx_lnh_s1c).

</td></tr><tr><td>

Contextual side panel component

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Email Interaction record page includes the following tabs.-   Record Information
-   Recommendations
-   Agent Assist
-   Collaborate
-   Attachments
-   Response Templates
-   Templates

</td></tr></tbody>
</table>
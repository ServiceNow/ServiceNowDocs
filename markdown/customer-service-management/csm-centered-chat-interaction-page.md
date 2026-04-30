---
title: CSM centered chat interaction record page
description: The CSM centered chat interaction record page provides a chat component in the center of the workspace that agents can use to handle customer chat conversations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM centered chat interaction record page

The CSM centered chat interaction record page provides a chat component in the center of the workspace that agents can use to handle customer chat conversations.

![Centered chat interaction record page with customer history, chat, and contextual side panel components](../image/centered-chat-interaction-record-page.png "CSM centered chat interaction record page")

To use the CSM centered chat interaction record page in CSM Configurable Workspace, enable the page and set the **Order** value. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

**Note:** The [CSM Interaction record page](csm-interaction-record-page.md) is the default experience for chat interaction. This page includes the chat component in the left panel.

## Page structure

The CSM centered chat interaction record page contains three panels.

<table id="table_jx2_dkp_q2c"><thead><tr><th>

Panel

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Left panel

</td><td>

The left panel includes two tabs: Customer and Interaction.The **Customer** tab includes the contact or consumer lookup component as well as customer history.

-   Contact or consumer [lookup component](csm-record-page-lookup-component.md):
    -   Includes the contact or consumer lookup card which agents can use to search for, select, and verify a customer.
    -   When a customer has been selected and linked to an interaction, a card with customer information is displayed at the top of the Customer tab.
-   Customer history: Includes the [Customer History component](csm-native-voice-record-page.md#section_imd_r1b_ldc), which displays customer, consumer, or account history information, depending on the customer information provided on the interaction record.

The **Interaction** tab includes the Interaction record form fields.

</td></tr><tr><td>

Center panel

</td><td>

The center panel includes the chat component. This panel is hidden when there is no chat conversation.

</td></tr><tr><td>

Right panel

</td><td>

The right panel contains the [contextual side panel component](csm-native-voice-record-page.md#section_uyq_2l1_ldc), which includes the following tabs:-   Recommended Actions search
-   Related Items
-   Attachments
-   Templates

</td></tr></tbody>
</table>## Plugin

The CSM centered chat interaction page template and page variant are included with the CSM Configurable Workspace application \(com.snc.uib.csm\_agent\_workspace\).

## CSM centered chat interaction record template

The CSM centered chat interaction record template brings the chat component to the center of the workspace and give agents greater visibility and access to customer chat conversations. This page view enables agents to manage chats and displays information, such as customer history and interaction details, that help agents to resolve issues.

Use the CSM centered chat interaction record template to create chat interaction record page variants and customize them as needed. For more information, see [Creating pages and page variants](config-csm-ws-create-page-variant.md).

## CSM centered chat interaction page variant

The CSM centered chat interaction page variant includes the following settings.

<table id="table_zqv_lvv_q1c"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Enabling the **Active** check box makes the page variant available to the selected audience. The CSM centered chat interaction record page variant is active by default.The active setting combined with the page order determines the page that CSM Configurable Workspace uses to display record information. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the CSM centered chat interaction record page variant is -2000.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The CSM centered chat interaction record page variant has the following conditions:-   **table = interaction**: Limits the use of the CSM centered chat interaction page variant to records from the Interaction \[interaction\] table.
-   **csm.isChatCenteredInteractionVisible = true**: Stores the result of the system's evaluation of the UX Page property that determines user roles.

If these conditions are met, the system displays the CSM centered chat interaction record page variant.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The CSM centered chat interaction record page has the following audience: **CSM - Front-line Agent**.This audience includes the sn\_cwf\_wrkspc.frontline\_agent role.

By default, agents who belong to the **CSM - Front-line Agent** audience will see the CSM centered chat interaction record page in the CSM Configurable Workspace. This is the default for both new \(zboot\) and upgrade customers.

For more information, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr></tbody>
</table>To access the settings for this page variant:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the Record section of the Pages and variants list, select **CSM centered chat interaction page**.
4.  Select **Settings** at the top of the page.

## CSM centered chat interaction record page components

The CSM centered chat interaction page includes the following components.

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

[Action bar](csm-centered-chat-interaction-page.md#section_mjh_fh1_ldc)

</td><td>

The action bar contains the actions available to users while working on chat interaction records.-   **Discuss**: Opens a pop-up window to start a Sidebar discussion.
-   **End Chat**: Ends the chat conversation.
-   **Create Incident**: Creates an incident record related to the interaction.
-   **Create Case**: Creates a case record related to the interaction.
-   **Save**: Saves changes to the interaction record.
-   **More Actions**: Perform additional actions such as creating a request or associating a record.

**Note:** The specific actions available are determined by factors such as the user role and other attributes.

</td></tr><tr><td>

[Contact or consumer lookup component](csm-record-page-lookup-component.md)

</td><td>

The **Customer** tab includes the contact or consumer lookup component, which agents can use to do the following:-   Search for a contact or consumer.
-   Select a contact or consumer from the list of search results and link that contact or consumer to the interaction record.
-   Verify the contact or consumer.
-   Edit the information for a contact or consumer.

</td></tr><tr><td>

[Customer History component](csm-centered-chat-interaction-page.md#section_imd_r1b_ldc)

</td><td>

The Customer History component displays customer, consumer, or account history information, depending on the field selections on the interaction record.This component can also display live call transcript.

**Note:** Live call transcript requires additional configuration.

</td></tr><tr><td>

Interaction details

</td><td>

The interaction details include information about the interaction including the account and contact, short description, and record state.

</td></tr><tr><td>

[Contextual side panel component](csm-centered-chat-interaction-page.md#section_uyq_2l1_ldc)

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the CSM centered chat interaction record page includes the following tabs.-   Recommended Actions search
-   Related Items
-   Attachments
-   Templates

</td></tr><tr><td>

[Thin compose modeless dialogs](csm-front-line-case-page-modeless-dialogs.md)

</td><td>

Thin compose modeless dialogs enable agents to initiate a work note or email in the activity stream and then open the text in a modeless dialog.**Note:** For the CSM centered chat interaction record page, the thin compose modeless dialogs feature is hidden by default and can be enabled by the admin.

</td></tr></tbody>
</table>## Customer History component

The Customer History component appears below the Interaction Controls Component in the left panel. This component is included with the [Customer Central](customer-central.md) plugin, which is activated as part of the CSM Configurable Workspace application.

The Customer History component includes the **Customer** tab. This tab displays customer, consumer, or account history information, depending on the customer information provided on the interaction record. This tab also includes a search field, filter, and date range selector that agents can use to find specific information in the history.

<table id="table_pyc_pgl_ydc"><thead><tr><th>

Interaction record information

</th><th>

Customer tab information

</th></tr></thead><tbody><tr><td>

Customer information is provided

</td><td>

When a customer is selected on the interaction record and customer history is available, the customer history is displayed in the Customer History tab.If customer history is not available, the Customer History tab displays a message that there is no activity yet.

</td></tr><tr><td>

Customer information is not provided

</td><td>

When a customer is not selected on the interaction record, the Customer History tab displays a message suggesting to link to a customer.

</td></tr><tr><td>

Account information is provided

</td><td>

When an account is selected on the interaction record, the account history is displayed in the Customer History tab.

</td></tr></tbody>
</table>Refreshing the customer history information:

-   When an agent selects a different customer on the interaction record and then saves the record, the agent needs to select **Refresh** on the Customer History component to update the information. The agent can also refresh the record page.
-   If there is new activity while the page is open, the agent needs to refresh the Customer History component or the record page to display the new activity in the Customer HIstory tab. For example, if the agent selects **Create Case** on the interaction record.

## Action bar component

The action bar component contains the actions available to users while working on chat interaction records.

-   **Discuss**: Opens a pop-up window to start a Sidebar discussion.
-   **Create Case**: Creates a new case record.
-   **End Chat**: Ends the chat conversation.
-   **Save**: Saves changes to the interaction record.
-   **More Actions**: Perform additional actions such as creating a request or associating a record.
    -   **Create Consumer**: Creates a new Consumer record in a subtab.
    -   **Create Request**: Creates a new Request record in a subtab and adds the record to the Related Tasks related list.
    -   **Associate Record**: Opens a new record in a subtab that the agent can use to link a record to the current interaction. This new record is displayed in the Related Tasks related list.

**Note:** The specific actions available are determined by factors such as the user role and other attributes.

The CSM centered chat interaction record page supports actions from the following Customer Service Management and CSM Configurable Workspace plugins:

-   Customer Service \(com.sn\_customerservice\)
-   CSM/FSM Configurable WS Foundation \(com.snc.uib.cwf\_workspace\)
-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   CSM Workspace \(com.snc.agent\_workspace.csm\)
-   Major Issue Management \(com.sn\_majorissue\_mgt\)
-   Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Customer Service with Request Management \(com.sn\_cs\_sm\_request\)
-   Time Recording for Customer Service \(com.snc.csm\_time\_recording\)
-   Omni-Experience Standard Feature Set

If you are using any additional plugins, you must add the actions from those plugins to the CSM centered chat interaction record page action bar. For more information, see the configuration steps in this topic: [Configure the Front-line case page action bar](../task/config-front-line-case-page-action-bar.md).

## Contextual side panel component

The CSM centered chat interaction record page includes the contextual side panel component, which provides agents with the following functionality.

<table id="table_orh_5rr_m1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended Actions

</td><td>

The Recommended Actions tab is now available as the first tab in the contextual side panel and is enabled for Pro customers. It includes a set of base system recommendations, such as similar incidents and similar open incidents.

The Recommended Actions tab includes [AI search](ra-csm-ai-search.md) functionality and Suggested Actions.-   **AI search** tab: Agents can use AI search to find relevant resources or resolutions for customer issues. The search feature displays an initial set of search results based on the text in the interaction short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search. From the list of search results, agents can select a source to see search results of that type. For more information, see [Search sources and guidance actions on the CSM Interaction page for chat channel](csm-centered-chat-interaction-page.md#table-csm-ws-rp-chat).

For all the other source types, the default guidance is supported. The default guidance for search results is a guidance that can be used for any search sources that don't have mapped guidances. For more information on default guidance, see [Default guidance for search results](ra-csm-guidances-default-guidance-search.md).

For more information, see the following topics:

    -   [Enable AI search in Recommended Actions](../task/migrate-ra-agent-assist.md)
    -   [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md)
**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

-   **Suggested Actions** tab: This tab displays relevant actions to agents based on a context of a record or recommend a value for a field. For more information on how to configure contexts so that relevant recommendations are displayed for the agents, see [Recommended Actions](configure-nba.md).

</td></tr><tr><td>

Related Lists

</td><td>

The Related Lists tab provides access the interaction related lists.The CSM centered chat interaction record page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

The CSM centered chat interaction record page includes the following related lists:

-   Related Tasks
-   Recent Interactions
-   Open Cases

</td></tr><tr><td>

Attachments

</td><td>

The Attachments tab provides access to case-related attachments. From this tab, agents can view and download attachments.

</td></tr><tr><td>

Templates

</td><td>

The Templates tab provides access to available form templates which enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a new record such as an incident or change.

</td></tr></tbody>
</table>The following table shows the actions that an agent can perform on the search results of various source types:

<table id="table-csm-ws-rp-chat"><thead><tr><th>

Search sources

</th><th>

Guidance actions

</th></tr></thead><tbody><tr><td>

Knowledge base article

</td><td>

-   Send an article link in chat.
-   Copy an article link to the article.
-   Read an article.
-   Flag
-   Mark an article as helpful.

</td></tr><tr><td>

Cases

</td><td>

-   Show or copy a resolution for resolved cases.
-   Link or open a case.

</td></tr><tr><td>

Incidents

</td><td>

-   Link an incident.
-   Open an incident.

</td></tr><tr><td>

Problems

</td><td>

-   Link a problem.
-   Open a problem.

</td></tr><tr><td>

Requests

</td><td>

-   Link a change request.
-   Open a change request.

</td></tr></tbody>
</table>
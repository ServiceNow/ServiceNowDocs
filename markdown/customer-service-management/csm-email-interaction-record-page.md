---
title: Email Interaction record page
description: The Email interaction record page enables agents to manage email conversations with customers using interaction records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Record pages, Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Email Interaction record page

The Email interaction record page enables agents to manage email conversations with customers using interaction records.

## Email interaction record page variant

The Email interaction record page variant is included with the CSM Configurable Workspace application \(com.snc.uib.csm\_agent\_workspace\). This page variant includes the following settings.

![email-interaction-record-page](../image/email-interaction-record-page.png)

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
-   **csm.isEmailInteractionVisible = true**: &lt;details&gt;.

 If all of these conditions are met, the system displays the Email Interaction record page variant.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The Email Interaction record page does not have a defined audience.For more information, see Learn about audiences.

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

The form heading displays the interaction short description and record tags.

 Action buttons are located in the dock.

</td></tr><tr><td>

Record tags

</td><td>

Agents can create multiple tags for a record and then use the tags to group and organize records.

</td></tr><tr><td>

Dock

</td><td>

The dock is a toolbar at the bottom of the page that displays minimized modeless dialogs, including emails, comments, and work notes. On the Email Interaction page, the dock also contains the following action buttons:

 -   **Close**: Closes the interaction record.
-   **Create Case**: Create records related to the interaction such as cases, incidents, requests, and consumers.
-   **Save**: Save changes to the interaction record.
-   **More Actions**: Perform additional actions such as starting a discussion and associating a record.

 **Note:** The specific actions available are determined by factors such as the user role and other attributes.

</td></tr><tr><td>

Contact and consumer lookup components

</td><td>

The lookup components display contact and consumer lookup cards on the left side of the page. Agents can use these cards to do the following:-   Search for a contact or consumer by name, phone number, or email address.
-   Select a contact or consumer from the list of search results and link that card to the interaction record. The selected card replaces the lookup components.
-   Verify the contact or consumer.
-   Edit the information for a contact or consumer.
-   Unlink a contact or consumer.
-   Collapse or expand the contact or consumer card.

For more information, see [Lookup component](csm-record-page-lookup-component.md).

</td></tr><tr><td>

Customer History component

</td><td>

The Customer History component displays customer, consumer, or account history information, depending on the field selections on the interaction record.This component can also display live call transcript.

**Note:** Live call transcript requires additional configuration.

</td></tr><tr><td>

Interaction details

</td><td>

The interaction details include information about the interaction including the account and contact, short description, and record state.

</td></tr><tr><td>

Activity stream

</td><td>

The activity stream displays activities in reverse chronological order with the newest activities appearing at the bottom and older activities at the top. This layout provides a natural conversation flow similar to messaging applications. Agents can use the activity stream to compose work notes or emails using the thin composer at the bottom of the activity stream.

</td></tr><tr><td>

Contextual side panel component

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Email Interaction record page includes the following tabs.-   Recommended Actions search
-   Related Lists
-   Attachments
-   Form Templates
-   Collaborate

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

## Workspace dock

The [workspace dock](csm-config-ws-bottom-utility-bar.md) component provides agents with a centralized location where they can see all current drafts at a glance. The dock also contains the actions available to users while working on email interaction records.

**Note:** The specific actions available are determined by factors such as the user role and other attributes.

-   **Create**: Create records related to the interaction.
    -   **Create Case**: Creates a new Case record in a sub tab and adds the record to the Related Tasks and Open Cases related lists.
    -   **Create Incident**: Creates a new Incident record in a sub tab and adds the record to the Related Tasks related list.
    -   **Create Request**: Creates a new Request record in a sub tab and adds the record to the Related Tasks related list.
    -   **Create Problem**: Creates a new Problem record in a sub tab and adds the record to the Related Tasks related list.
    -   **Create Consumer**: Creates a new Consumer record in a sub tab and adds the record to the Consumers list.
-   **Save**: Saves changes to the interaction record.
-   **Close**: Close the interaction record.
-   **More Actions**: Perform additional actions such as starting a discussion and associating a record.
    -   **Discuss**: Opens a pop-up window to start a Sidebar discussion.
    -   **Associate Record**: Opens a new record in a sub tab that the agent can use to link a record to the current interaction. This new record is displayed in the Related Tasks related list.

The Email Interaction record page supports actions from the following Customer Service Management and CSM Configurable Workspace plugins:

-   Customer Service \(com.sn\_customerservice\)
-   CSM/FSM Configurable WS Foundation \(com.snc.uib.cwf\_workspace\)
-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   CSM Workspace \(com.snc.agent\_workspace.csm\)
-   Major Issue Management \(com.sn\_majorissue\_mgt\)
-   Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Customer Service with Request Management \(com.sn\_cs\_sm\_request\)
-   Time Recording for Customer Service \(com.snc.csm\_time\_recording\)
-   Omni-Experience Standard Feature Set

If you are using any additional plugins, you need to add the actions from those plugins to the Email Interaction record page action bar. For more information, see the configuration steps in this topic: [Configure the Front-line case page action bar](../task/config-front-line-case-page-action-bar.md).

## Thin compose modeless dialogs

The thin composer is located at the bottom of the activity stream with the Email tab as the first tab. Agents can pop out the composer into a separate window called a modeless dialog.

Drafts are created when agents add or modify content in the composer. Minimized modeless dialogs appear in the [workspace dock](csm-config-ws-bottom-utility-bar.md).

For more information about modeless dialogs, see [Thin compose modeless dialogs](csm-front-line-case-page-modeless-dialogs.md#section_nws_1rs_rfc).

## Contextual side panel component

The Email Interaction record page includes the contextual side panel component, which provides agents with the following functionality.

<table id="table_orh_5rr_m1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended Actions

</td><td>

The Recommended Actions tab is now available as the first tab in the contextual side panel and is enabled for Pro customers. It includes a set of base system recommendations, such as similar incidents and similar open incidents.

The Recommended Actions tab includes [AI search](ra-csm-ai-search.md) functionality and suggested actions. Agents can use AI search to find relevant resources or resolutions for customer issues.The search feature displays an initial set of search results based on the text in the interaction short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

From the list of search results, agents can select a source to see search results of that type.

Depending on the source type, agents can do the following:

-   Open an article in full view in a sub tab.
-   Flag an article.
-   Mark an article as helpful.
-   Order a catalog item.

For more information, see [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

Related Lists

</td><td>

The Related Lists tab provides access the interaction related lists.The Email Interaction record page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

The Email Interaction record page includes the following related lists:

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

</td></tr><tr><td>

Collaborate

</td><td>

The Collaborate component enables agents to communicate with stakeholders and other users and gather information for case resolution. For more information, see [Collaborate component](csm-config-ws-collaborate-component.md).

</td></tr></tbody>
</table>## Email interaction tab notifications

Unread email counters display on email interaction tabs to help agents track new email activity across multiple interactions. When new emails arrive for an email interaction that's open in an inactive tab, an unread counter appears on the tab. The counter increments as additional emails arrive and clears when you select the tab.

For example, you have multiple email interactions open. A customer replies to an interaction in an inactive tab. The tab displays an unread counter \(for example, "2"\), so you can identify which interactions have new activity without losing context. For configuration requirements, see [View unread email counters on interaction tabs](../task/view-unread-email-counters-on-interaction-tabs.md).


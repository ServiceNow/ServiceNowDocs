---
title: Front-line case page
description: The Front-line case page provides a simplified case view that enables front-line agents to quickly gather context, categorize cases, and provide prompt responses to customers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Record pages, Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Front-line case page

The Front-line case page provides a simplified case view that enables front-line agents to quickly gather context, categorize cases, and provide prompt responses to customers.

The Front-line case page focuses on the essential functionality that front-line or tier 1 agents need:

-   Look up and verify customer information
-   Scan the activity stream
-   View related information
-   Search for knowledge articles

The Front-line case page is included with the CSM Configurable Workspace application.

![The Front-line case page enables agents to focus on four main areas, including contact information, case details, the activity stream, and the contextual side panel.](../image/front-line-case-page-template.png "Front-line case page")

## Front-line case page variant

The Front-line case page variant is included with the CSM Configurable Workspace application. This variant includes the following settings.

<table id="table_zqv_lvv_q1c"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Enabling the **Active** check box makes the page variant available to the selected audience. The Front-line case page variant is active for new and upgrade customers.The active setting combined with the other page variant settings determines the page that CSM Configurable Workspace uses to display record information. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the Front-line case page variant is 1000.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The Front-line case page has the following condition: **table=sn\_customerservice\_case**This condition limits the use of the Front-line case page variant to records from the Case \[sn\_customerservice\_case\] table and tables that extend the Case table.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The Front-line case page has the following audience: **CSM - Front-line Agent**This audience includes the sn\_cwf\_wrkspc.frontline\_agent role.

For more information, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr></tbody>
</table>To access the settings for this page variant:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the Record section of the Pages and variants list, select **Front-line case page**.
4.  Select **Settings** at the top of the page.

## Roles

The CSM Configurable Workspace application includes the following role: Front-line agent role \(sn\_cwf\_wrkspc.frontline\_agent\). Agents with this role have access to the Front-line case page in CSM Configurable Workspace.

The Front-line case page variant includes the CSM - Front-line Agent audience, which includes the sn\_cwf\_wrkspc.frontline\_agent role.

**Note:** To make the Front-line case the default page, the system administrator can set the page to active and set it to the lowest page order.

## Front-line case page components

The Front-line case page includes the following components.

<table id="table_pk2_g1w_q1c"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Form header

</td><td>

The form header displays the case short description. Agents can quickly glance at the form header to see what the case is about.Agents can edit the short description of a record directly from the record header field. For more information, see [Editable record headers](../reference/csm-workspace-agent-actions.md#section_hhb_1tj_23c).

</td></tr><tr><td>

Record tags

</td><td>

Tags enable agents to assign categories to records. Agents can create multiple tags for a record and then use the tags to group and organize records.

</td></tr><tr><td>

[Action bar](csm-config-workspace-components.md#section_bl4_wnr_2hc)

</td><td>

The action bar contains the actions available to agents while working on case records. This includes buttons and items in the More Actions menu.The specific actions are determined by factors such as the user role, case state, and other attributes.

</td></tr><tr><td>

Contact lookup

</td><td>

The contact lookup component enables agents to search for contacts and link them to the case record. Agents can use the contact lookup component to do the following:

-   Search for a contact.
-   Link or unlink a contact.
-   Edit and save a linked contact record.
-   Select a reference field on a lookup card, such as a contact name, to open the reference in a sub-tab.
-   Select an email address on a lookup card to open a draft email in the email composer in a sub-tab.
-   Select a phone number on a lookup card to make a call.

The contact lookup component displays information in record cards. These cards display contact information and provide quick access to details such name, email, and phone.For more information, see the [Contact and consumer lookup components](csm-front-line-case-page.md#section_dnl_3f4_s1c) section below.

</td></tr><tr><td>

Consumer lookup

</td><td>

Agents can use the consumer lookup component to do the following:-   Search for a consumer.
-   Link or unlink a consumer.
-   Edit and save a linked consumer record.
-   Select a reference field on a lookup card, such as a consumer name, to open the reference in a sub-tab.
-   Select an email address on a lookup card to open a draft email in the email composer in a sub-tab.
-   Select a phone number on a lookup card to make a call.

The consumer lookup component displays information in record cards. These cards display consumer information and provide quick access to details such name, email, and phone.

For more information, see the [Contact and consumer lookup components](csm-front-line-case-page.md#section_dnl_3f4_s1c) section below.

</td></tr><tr><td>

Case details

</td><td>

The case details component includes collapsible sections for:-   Case
-   Notes
-   Closure Information
-   Related Records

This component also includes a menu with additional form actions, such as personalizing the form, exporting data, and copying the URL.

</td></tr><tr><td>

Case summarization

</td><td>

The case summarization component appears above the activity stream. When an agent opens a case record, the component is collapsed and in the default state.Agents can use this component to do the following:

-   Summarize case details.
-   Post the summary to the activity stream.
-   Refresh the summary.

The case summarization component requires the Now Assist for Customer Service Management \(CSM\) application to be activated and configured. For more information, see the [Case summarization component](csm-front-line-case-page.md#section_ots_wnh_s1c) section below.

</td></tr><tr><td>

Activity stream

</td><td>

The activity stream component displays a list of activities occurring on a case record. This list can be collapsed to provide a quick view of case activities or expanded to provide more detail about individual activities.For more information, see the [Activity stream component](csm-front-line-case-page.md#section_ntx_lnh_s1c) section below.

**Note:** The Front-line case page uses [modeless dialogs](csm-front-line-case-page-modeless-dialogs.md) for composing comments, work notes, and emails.

</td></tr><tr><td>

Contextual side panel

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Front-line case page includes the following tabs.-   Record information, including SLA details
-   Recommended Actions search
-   Attachments
-   Form Templates
-   Response Templates
-   Email Templates
-   Related Lists
-   Collaborate

For more information, see the following sections:

-   [Contextual side panel component](csm-front-line-case-page.md#section_trg_ypr_m1c)
-   [Related lists component](csm-front-line-case-page.md#section_urr_nrh_s1c)

</td></tr></tbody>
</table>## Action bar component

The Front-line case page supports actions from the following Customer Service Management and CSM Configurable workspace plugins:

-   Customer Service \(com.sn\_customerservice\)
-   CSM/FSM Configurable WS Foundation \(com.snc.uib.cwf\_workspace\)
-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   CSM Workspace \(com.snc.agent\_workspace.csm\)
-   Major Issue Management \(com.sn\_majorissue\_mgt\)
-   Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Customer Service with Request Management plugin \(com.sn\_cs\_sm\_request\)
-   Time Recording for Customer Service \(com.snc.csm\_time\_recording\)
-   Omni-Experience Standard Feature Set

If you are using any additional plugins, you must add the actions from those plugins to the Front-line case page action bar. For more information, see [Configure the Front-line case page action bar](../task/config-front-line-case-page-action-bar.md).

The **Create** action on the Front-line case page displays a list of available actions. Selecting an action from this list opens the record either in a sub-tab or in a modeless dialog. For more information, see [Create action layout group](csm-config-ws-action-layout-groups.md).

The Front-line case page action bar includes the **Follow** action in the More Actions menu. Selecting this action enables you to receive notifications when comments or work notes are added to the record.

You receive notifications in the Notifications menu at the top of the page according to your notification preferences. You can select the notification to open the record that was updated. For more information, see the following topics:

-   [Configure Next Experience notification preferences](https://www.servicenow.com/docs/access?context=next-experience-notifications-preferences&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)
-   [Follow records in Next Experience](https://www.servicenow.com/docs/access?context=follow-records-in-next-experience&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

When the **Follow** action is selected, the button toggles to **Unfollow**. To stop receiving notifications, select **Unfollow**.

## Contact and consumer lookup components

The contact and consumer lookup components enable users to do the following:

-   Look up a contact or consumer by name, phone number, or email address. As you type characters in the search box, matching information appears in record cards below the search box.
-   Select a contact or consumer after searching by selecting the desired record card. The selected record card replaces the lookup component.

User roles determine which lookup component appears on the Front-line case page.

-   Front-line case agents can see the Contact lookup component.
-   Consumer agents with the Front-line case agent role can see the Consumer lookup component.
-   Some users, such as managers, can have both B2B \(account and contact\) and B2C \(consumer\) roles. When a user has both roles, they can see both the Contact and Consumer lookup components.

When using the Contact lookup component to look up and select a contact, the system hides the Consumer lookup component. When using the Consumer lookup component to look up and select a consumer, the system hides the Contact lookup component.

When using the Contact component, the system displays the contacts for the selected account. If the agent selects a different contact, the system updates the account.

After selecting a contact or consumer, users can perform the following actions from the contact or consumer record card:

-   Remove a linked contact or consumer from a case record by selecting the more actions icon and then selecting **Unlink**.
-   Edit and save a linked contact or consumer record by selecting the pencil icon, editing the information for the contact, and selecting **Save**.
-   Select a reference field on a lookup card to open the referenced record in a subtab.
-   Select an email address on a lookup card to open to open the email composer in a subtab.
-   Select a phone number on a lookup card to make a phone call.
-   Collapse the card to display more record content. When collapsed, users can see a link to the contact or consumer name.

The Contact and Consumer lookup components include advanced search capabilities that enable agents to perform a type-ahead search across multiple tables and fields. This includes the following types of matching:

-   Exact match: phone number and record number
-   Starts with match: name and email address

## Case summarization component

The case summarization component provides agents with a summary of a customer service case, including the issue and the actions taken. Agents can generate summaries to understand case context and post summaries to the case work notes.

The case summarization component appears above the activity stream on the Front-line case page variant. Upon first opening a case, the component is collapsed and in the default state.

Using this component, agents can:

-   Select **Summarize** to create a summary of the case details.
-   Select **Share to work notes** to copy the summary text to the activity stream.
    -   Review the summary text in the Share to work notes pop-up window and modify the text as needed.
    -   Select **Save to work notes** on the pop-up window to add the text to the activity stream.
-   Select the refresh icon in the component footer to refresh the text and get the latest summary.

**Note:** If the case does not contain enough text to summarize, the system displays the following message: "This case doesn't have the minimum number of words required for summarization yet."

To use the case summarization component with the Front-line case page, activate the Now Assist for Customer Service Management \(CSM\) application and configure the case summarization skill in the Now Assist Admin console. For more information, see:

-   [Activate Now Assist for Customer Service Management \(CSM\)](now-assist-csm-supporting-info.md)
-   [Configure the case summarization skill in the Now Assist Admin console](now-assist-csm-configuring.md).

## Activity stream component

The activity stream component displays a list of the activities occurring on a case record. The activities in the list can be collapsed or expanded. When collapsed, the agent can quickly scan the list to get an overview of case activities. When expanded, the agent can see detailed information on individual activities.

![The front-line case page activity stream component lists record activities in a collapsed or expanded format and uses tiles to represent the activity types.](../image/front-line-case-page-activity-stream.png "Front-line case page activity stream component")

The activities in the activity stream are represented by tiles that use icons and colors to indicate the activity type.

-   Comment
-   Work note
-   Attachment
-   Field change
-   Email sent or email received
-   Chat discussion
-   Custom icon

When collapsed, each activity in the list includes:

-   A tile that represents the activity type.
-   The name of the user responsible for the activity.
-   A brief one-line summary of the activity.
-   A badge that indicates if an activity is internal or external.
-   A relative timestamp.
-   An expand button that the agent can use to see a detailed summary of the activity.

When expanded, each activity also includes:

-   A full date and time stamp.
-   An action label that describes the type of activity.
-   For comments and work notes, the full text of the comment or work note.
-   For field updates, the field name and the updated field value.
-   For emails, detailed message information.
-   For attachments, a small preview of the attached file.
-   For chats, a sidebar chat card.

The activity stream uses [Modeless dialogs](csm-front-line-case-page-modeless-dialogs.md) for composing comments, work notes, and emails.

## Contextual side panel component

The Front-line case page includes the contextual side panel component, which provides agents with the following functionality.

<table id="table_orh_5rr_m1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended Actions

</td><td>

The Recommended Actions tab is now available as the first tab in the contextual side panel and is enabled for Pro customers. It includes a set of base system recommendations, such as similar incidents and similar open incidents.

The Recommended Actions tab includes [AI search](ra-csm-ai-search.md) functionality. Agents can use AI search to find relevant resources or resolutions for customer issues.The search feature displays an initial set of search results based on the text in the case short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

From the list of search results, agents can do the following:

-   Select a source to see search results of that type.
-   Filter the list of search results.
-   Sort the list of search results.
-   Open the search results in full view in a record sub-tab.
-   Take the following actions:
    -   [Attach and share article](csm-front-line-case-page.md#section_j54_wlv_sdc)
    -   Perform other actions such as reading articles in full view, flagging articles, or marking articles as helpful or unhelpful.
-   View successful actions by selecting the Actions history icon.

Suggested Actions tab: This tab displays relevant actions to agents based on the context of a record or recommends a value for a field. For more information on how to configure contexts to display relevant actions for the agent, see [Recommended Actions](configure-nba.md). The Suggested Actions tab is available in the base system for Pro customers and doesn’t require additional configuration. It becomes visible when the Task Intelligence plugin is installed. Non-Pro customers can enable the tab manually.

-   Without the plugin, only the Search tab is visible on the Front-line case page.

-   With the plugin installed, both Search and Suggested Actions tabs appear, and recommendations are shown under Suggested Actions.

-   If the plugin is uninstalled, the Suggested Actions tab is no longer available.


For more information, see [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

Record Information

</td><td>

The Record Information tab includes the following information: record overview and SLAs.-   The **Overview** card displays relevant information about the record including account and contact, case priority, and state.
-   The Task SLA cards component displays cards with the record SLA information, including time remaining, the SLA state, and any breaches. For more information, see [Task SLA cards component](csm-record-page-sla-card-component.md).

**Note:** The cards that appear in the Record Information tab can be configured in the **Front-line Case Page Ribbon Config** ribbon configuration. For more information, see [Set up a ribbon configuration in CSM Configurable Workspace](../task/config-csm-config-ws-ribbon.md).

</td></tr><tr><td>

Attachments

</td><td>

The Attachments tab provides access to case-related attachments. From this tab, agents can view and download attachments.

</td></tr><tr><td>

Templates

</td><td>

The Templates tab provides access to available form templates which enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a new record such as an incident or change.

</td></tr><tr><td>

Response Templates

</td><td>

The Response Templates tab provides access to available response templates. These templates contain reusable messages that agents can copy to provide quick and consistent messages to customers.

</td></tr><tr><td>

Email Templates

</td><td>

The Email Templates tab provides access to available email templates. These templates contain default values for fields that agents can add to email messages. These default values can include the recipients \(email addresses in the To, Cc, and Bcc fields\), the sender, the subject of the email, and text to include in the message body.

</td></tr><tr><td>

Related Lists

</td><td>

The Related Lists tab provides access the case-related lists.The Front-line case page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

For more information, see the [Related lists component](csm-front-line-case-page.md#section_urr_nrh_s1c) section below.

</td></tr><tr><td>

Collaborate

</td><td>

The Collaborate component enables agents to communicate with stakeholders and other users and gather information for case resolution. For more information, see [Collaborate component](csm-config-ws-collaborate-component.md).

</td></tr></tbody>
</table>## Related lists component

The related lists component provides access to the case related lists. This component uses an expandable accordion format. Agents can expand the desired lists to see the related items. This component also displays an icon with the number of items in a list.

![The Front-line case page related lists component in the contextual side panel uses an accordion format to expand and display related list items](../image/front-line-case-page-related-lists.png "Front-line case page related lists component")

Related lists include the following actions:

-   **Create**: Opens a blank record in a sub tab that the agent can use to create a new item.
-   **View all**: Opens a list of records in a sub tab.
-   **Show more**: is displayed for lists that have more than five items.

The items in an expanded list are displayed as cards. An expanded list shows one card for each item in the list.

-   Agents can open an item in a sub-tab.
-   If a list has more than five items, it includes a **Show more** option.

## Customer History component

The Customer History component displays customer, consumer, or account history information, depending on the field selections on the interaction record. This component displays the information previously displayed in the Customer Activity tab. For more information, see [Customer History component](customer-central.md#section_i2b_kpt_ydc) in the Customer Central documentation.

## Record presence feature

The Front-line case page includes the record presence feature. This feature allows agents to see other users who are viewing the same record and enables easy collaboration.

The user presence component displays an icon in the form header that shows the user who is currently viewing the record. For three or more users, the component displays two icons plus a number that represents additional users.

-   Hover over an icon to see more information about a user.
-   Select the number icon to see more information about the additional users.

For more information about this feature, see [User presence](https://www.servicenow.com/docs/access?context=c_UserPresence&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## Requesting information from customers

The Front-line case page includes a **Request Info** UI action that agents can use to request information from customers. This action provides agents with the option to send a comment to the customer when requesting information.

**Note:** The **Request Info** UI action is available to users with the sn\_cwf\_wrkspc.frontline\_agent role and for cases in the Open state.

The **Request Info** UI action on the Front-line case page behaves differently than the same action on the CSM default record page. On the Front-line case page, this action moves a case to the Awaiting Info state but does not require the agent to add a comment.

To request information:

1.  Select **Manage Case** in the action bar.
2.  Select **Request Info**.

The system sets the case **State** field to Awaiting Info and displays the following message to the agent: **Send a comment to request info if you haven’t already. The case is awaiting info.**

-   If the agent has not sent a comment, they can compose and post a comment in the activity stream.
-   If the agent has already composed a comment and then selects **Request Info**, the system saves the record and automatically posts the comment to the activity stream.

## Attaching and sharing knowledge articles

Agents can share articles with customers by using the **Attach and share article** knowledge guidance. This guidance recommends relevant knowledge articles to customer service agents and enables them to share the selected articles with customers in comments, work notes, or emails.

From the Recommendations tab in the contextual side panel, agents can use [modeless dialogs](csm-front-line-case-page-modeless-dialogs.md) to do the following:

-   Attach and add a link to a comment.
-   Attach and add a link to an email.
-   Add a link to a work note.

Selecting these actions displays the comment, work note, or email modeless dialog. Once the guidance is executed, it is marked as Complete. After an action is completed, an entry is posted in the case record activity stream.

To display the knowledge article links that are added to the modeless dialogs with the **Attach and share article** guidance, the system administrator needs to manually enable the rich text editor:

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
2.  Search for the **glide.ui.journal.use\_html** system property.
3.  Set the **Value** to true.

When the **glide.ui.journal.use\_html** is set to true, the Rich Text Editor is enabled by default for comments and work notes in the Activity Stream. A **Rich Text Editor** toggle appears in the upper-right corner of the message box, allowing users to switch between rich text and plain text as needed.

The editor provides options such as bold, italics, lists, hyperlinks, and text alignment to help create structured, readable content. This setting does not affect email composition, which is managed  separately via **sys\_email\_client\_confguration**. The rich text editor and formatting options are available by default in email messages, but the toggle does not appear.

For more information about the knowledge guidance, see [Attach and share article guidance](ra-csm-guidances-attach-share-article.md).


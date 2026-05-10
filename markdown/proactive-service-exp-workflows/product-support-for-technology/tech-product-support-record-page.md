---
title: Technology Product Support record page
description: The Technology product support record page provides a simplified case view in CSM Configurable Workspace that enables agents to research and resolve technology cases.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Technology Product Support Case, Explore, Product Support for Technology]
---

# Technology Product Support record page

The Technology product support record page provides a simplified case view in CSM Configurable Workspace that enables agents to research and resolve technology cases.

![The Technology product support record page enables agents to focus on case details, the activity stream, and information in the contextual side panel.](../image/tech-product-support-record-page.png "Technology product support record page")

The Technology product support record page focuses on the essential functionality that agents need:

-   Looking up and verifying customer information
-   Scanning the activity stream
-   Viewing related information
-   Searching for knowledge articles

The Technology product support record page is included with the Technology Product Support Case application \(sn\_tech\_product\_support\).

## Technology product support record page variant

The Technology product support record page variant is included with the Technology Product Support Case application. A page variant is a version of a page that has unique settings. This page variant includes the following settings.

<table id="table_jcm_z3m_bbc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Enabling the **Active** check box makes the page variant available to the selected audience. The technology product support record page is active by default.

The active setting combined with the page order determines the page that CSM Configurable Workspace uses to display record information. For more information, see [Set record page order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/config-csm-ws-set-record-page-order.md).

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the Technology product support record page variant is -1000.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The Technology product support record page has the following condition:**table=sn\_tech\_product\_support\_case**

This condition limits the use of the page variant to records from the Tech Product Support Case \[sn\_tech\_product\_support\_case\] table.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The Technology product support record page variant audience doesn’t specify any user roles so all users can see this variant.

</td></tr></tbody>
</table>To access the settings for this page variant:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the Record section of the Pages and variants list, select **Technology product support record page**.
4.  Select **Settings** at the top of the page.

## Technology product support record page components

The Technology product support record page includes the following components.

<table id="table_fkk_jlm_bbc"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Form heading

</td><td>

The form heading displays the case short description and also includes the action bar and record tags.

</td></tr><tr><td>

Record tags

</td><td>

Agents can create multiple tags for a record and then use the tags to group and organize records.For more information, see [Tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_Tags.md).

</td></tr><tr><td>

[Action bar](tech-product-support-record-page.md#section_bwz_3nm_bbc)

</td><td>

The action bar contains the actions available to users while working on case records. The specific actions are determined by factors such as the user role, case state, and other attributes.

</td></tr><tr><td>

[Modeless dialogs](tech-product-support-record-page.md#section_lpp_5ys_y1c)

</td><td>

Modeless dialogs are windows that overlay the main window content. Agents can use these windows to create and post comments and work notes to the activity stream and to compose and send emails.

</td></tr><tr><td>

[Account and contact lookup components](tech-product-support-record-page.md#section_dnl_3f4_s1c)

</td><td>

Agents can use the account and contact lookup components to do the following:-   Search for an account or contact.
-   Create an account or contact.
-   Link or unlink an account or contact.
-   Edit and save a linked account or contact record.
-   Select a reference field on a lookup card, such as a contact name, to open the reference in a subtab.
-   Select an email address on a lookup card to open a draft email in the email composer in a subtab.
-   Select a phone number on a lookup card to call.

The account and contact lookup components display information in record cards. These cards display account and contact information and provide quick access to customer details such name, email, and phone.

</td></tr><tr><td>

Workspace form view

</td><td>

The Workspace form view includes the following sections:-   Case Details
-   Issue Details
-   Initial Response
-   Technical Action Plan
-   Other Case Details
-   Related Records
-   Notes
-   Closure Information

These sections can be expanded and collapsed to display the fields within each section.

The Workspace form view also includes a menu with additional form actions, such as personalizing the form, exporting data, and copying the URL.

For more information about the fields that appear in these sections, see [Tech Product Support Case table](../reference/tech-product-support-case-table.md).

</td></tr><tr><td>

[Case summarization component](tech-product-support-record-page.md#section_ots_wnh_s1c)

</td><td>

The case summarization component appears above the activity stream. When an agent opens a case record, the component is collapsed and in the default state.Agents can use this component to do the following:

-   Summarize case details.
-   Post the summary to the activity stream.
-   Refresh the summary.

**Note:** The case summarization component requires the [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md) application to be activated and configured.

</td></tr><tr><td>

[Activity stream component](tech-product-support-record-page.md#section_ntx_lnh_s1c)

</td><td>

The activity stream component displays a list of activities occurring on a case record. This list can be collapsed to provide a quick view of case activities or expanded to provide more detail about individual activities.The Technology product support record page uses [modeless dialogs](tech-product-support-record-page.md#section_lpp_5ys_y1c) for composing comments, work notes, and emails.

</td></tr><tr><td>

[Contextual side panel](tech-product-support-record-page.md#section_c53_csn_n1c)

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Technology product support record page includes the following tabs.-   Activity Stream
-   Recommended Actions search
-   Related Items
-   Attachments
-   Templates
-   Response Templates
-   Email Templates

For more information, see the following sections:

-   [Contextual side panel component](tech-product-support-record-page.md#section_c53_csn_n1c)
-   [Recommended Actions search component](tech-product-support-record-page.md#section_ev4_wyf_bbc)
-   [Related items component](tech-product-support-record-page.md#section_b1b_dfh_z1c)

</td></tr></tbody>
</table>## Actions available in the action bar

The following actions are available on the Technology product support record page action bar. The specific actions that are available are determined by factors such as the user role, case state, and other attributes.

|Action|Description|
|------|-----------|
|In-progress Actions|Provides a list of minimized [modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-front-line-case-page-modeless-dialogs.md) and includes a badge that displays the number of items in the list. From this list, an agent can select an item to open the minimized comment, work note, or email.|
|Submit Case|Moves the case from the Draft state to the New state.|
|Assign to me|Assigns the case to the logged-in user and moves the case to Work in Progress.|
|Accept|Assigns the case to the logged-in user and moves the case to Work in Progress.|
|Request Information|The agent requests information from the customer. Selecting this action moves the case state to Awaiting Information.|
|Information Received|The agent acknowledges that information was received from the customer. Selecting this action moves the case state to Work in Progress.|
|Propose Solution|The agent proposes a solution to the customer.|
|Accept Solution|The agent can accept the proposed solution on behalf of the customer. Selecting this action moves the case to Closed.|
|Reject Solution|The agent can reject the proposed solution on behalf of the customer. Moves the case to Work in Progress.|
|Save|Saves changes to the case record.|
|Cancel|Cancels changes to the case record.|
|Compose|Compose comments, work notes, and emails in [modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-front-line-case-page-modeless-dialogs.md).|
|Create|Create records such as work orders, incidents, and requests.|
|More Actions|Perform additional actions such as proposing a major case or reporting a knowledge gap.|

## Modeless dialogs

The Technology product support record page uses modeless dialogs to create comments, work notes, and email messages. The following actions are available from the **Compose** button in the form header:

-   **Compose &gt; Comment**: Opens the Compose a comment modeless dialog.
-   **Compose &gt; Work note**: Opens the Compose a work note modeless dialog.
-   **Compose &gt; Email**: Opens the Compose email modeless dialog.

The following rules apply to modeless dialog visibility:

-   One modeless dialog of each type \(comment, work note, or email\) can be active at a time.
-   One modeless dialog can displayed at a time while the other two are minimized.
-   Minimized modeless dialogs appear in the In-progress Actions menu in the action bar. This menu displays a badge that shows the number of minimized modeless dialogs.
-   If an agent opens a second modeless dialog while the first modeless dialog is displayed, the system minimizes the first modeless dialog.

Agents can do the following:

-   Select the In-progress Actions menu to see a list of minimized modeless dialogs. Each entry in the list includes the title and category of the minimized item.
    -   For email, the title is the email subject.
    -   For comments and work notes, the title is the first line of text.
-   Select an item from the list to open the minimized modeless dialog.

Closure behavior for comments, work notes, and email:

-   Posting a comment or work note to the activity stream closes the modeless dialog.
-   Saving the record posts a comment or work note to the activity stream closes the modeless dialog.
-   Sending an email closes the modeless dialog. The system adds the email to the activity stream and to the Emails related list.

Discard behavior for comments and work notes:

-   Closing a work note or comment modeless dialog discards the text. The system displays a Close Dialog pop-up window and asks the agent to confirm the action.
    -   Selecting **Continue** confirms the action, discards the text, and closes the window.
    -   Selecting **Cancel** or the Close Dialog button cancels the action. The modeless dialog remains open and the text remains in the dialog.
-   The text is discarded in the modeless dialog and on the form field.

Agents can use response templates from the contextual side panel to copy text into the modeless dialogs.

Agents can apply templates to emails in a modeless dialog:

-   Select a template from the Email Templates tab in the contextual side panel and then select **Apply Template**. The contents of the template is added to the modeless dialog.
-   If a modeless dialog is minimized, display the dialog before applying the template.

Agents can also toggle the **Rich text editor** button in the email modeless dialog to show or hide the TinyMCE formatter.

For more information, see [Modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-front-line-case-page-modeless-dialogs.md).

## Account and contact lookup components

The account and contact lookup components enable agents to do the following:

-   Look up an account or contact by name, phone number, or email address. As the agent types characters in the search box, matching information appears in record cards below the search box.
-   Select an account or contact after searching by selecting the desired record card. The selected record card replaces the lookup component.
-   Create a new account or contact by selecting the **+** icon on the lookup component, filling in the fields for the account or contact, and selecting **Save**. A record card for the new account or contact replaces the lookup component.

Agents can perform the following actions from a record card:

-   Remove a linked account or contact from a case record by selecting the more actions icon and then selecting **Unlink**. Then save the form to apply this change.
-   Edit and save a linked account or contact record by selecting the pencil icon, editing the information for the account or contact, and selecting **Save**.
-   Select a reference field on a lookup card to open the referenced record in a subtab.
-   Select an email address on a lookup card to open the email composer in a subtab.
-   Select a phone number on a lookup card to make a phone call.

## Case summarization component

The case summarization component provides agents with a summary of a customer service case, including the issue and the actions taken. Agents can generate summaries to understand the case context and post summaries to the case work notes.

The case summarization component appears above the activity stream on the Technology product support record page variant. Upon first opening a case, the component is collapsed and in the default state.

Using this component, agents can:

-   Select **Summarize** to create a summary of the case details.
-   Select **Share to work notes** to copy the summary text to the activity stream.
    -   Review the summary text in the Share to work notes pop-up window and modify the text as needed.
    -   Select **Save to work notes** on the pop-up window to add the text to the activity stream.
-   Select the refresh icon in the component footer to refresh the text and get the latest summary.

**Note:** If the case doesn’t contain enough text to summarize, the system displays the following message: "This case doesn't have the minimum number of words required for summarization yet."

To use the case summarization component with the Technology product support record page variant, activate the Now Assist for Customer Service Management \(CSM\) application and configure the case summarization skill in the Now Assist Admin console. For more information, see:

-   [Activate Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-supporting-info.md)
-   [Configure the case summarization skill in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-configuring.md).

## Activity stream component

The activity stream component displays a list of the activities occurring on a case record. The activities in the list can be collapsed or expanded. When collapsed, the agent can quickly scan the list to get an overview of case activities. When expanded, the agent can see detailed information on individual activities.

![The technology product support record page activity stream component lists record activities in a collapsed or expanded format and uses tiles to represent the activity types.](../image/front-line-case-page-activity-stream.png "Technology product support record page activity stream component")

The activities in the activity stream are represented by tiles that use icons and colors to indicate the activity type:

-   Comment
-   Work note
-   Attachment
-   Field change
-   Email sent or email received
-   Chat discussion

When collapsed, each activity in the list includes:

-   A tile that represents the activity type.
-   The name of the user responsible for the activity.
-   A brief one-line summary of the activity.
-   A badge that indicates if an activity is internal or external.
-   A relative timestamp.
-   An expand button that the agent can use to see a detailed summary of the activity.

When expanded, each activity also includes:

-   A full date and timestamp.
-   An action label that describes the type of activity.
-   For comments and work notes, the full text of the comment or work note.
-   For field updates, the field name and the updated field value.
-   For emails, detailed message information.
-   For attachments, a small preview of the attached file.
-   For chats, a sidebar chat card.

The activity stream uses [modeless dialogs](tech-product-support-record-page.md#section_lpp_5ys_y1c) for composing comments, work notes, and emails. Use the **Compose** button in the action bar to create these items.

-   **Compose &gt; Comment**: Opens the Compose a comment modeless dialog.
-   **Compose &gt; Work note**: Opens the Compose a work note modeless dialog.
-   **Compose &gt; Email**: Opens the Compose email modeless dialog.

## Contextual side panel component

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Technology product support record page includes the following tabs.

<table id="table_orh_5rr_m1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Activity stream](tech-product-support-record-page.md#section_ntx_lnh_s1c)

</td><td>

The activity stream component displays a list of the activities occurring on a case record.

</td></tr><tr><td>

[Recommended Actions search](tech-product-support-record-page.md#section_ev4_wyf_bbc)

</td><td>

The Recommended Actions tab includes [AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-ai-search.md) functionality. Agents can use AI search to find relevant resources or resolutions for customer issues.The search feature displays an initial set of search results based on the text in the case short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

From the list of search results, agents can do the following:

-   Select a source to see search results of that type.
-   Filter the list of search results.
-   Sort the list of search results.
-   Open the search results in full view in a record subtab.
-   Take the following actions:
    -   View and attach article
    -   Perform other actions such as reading articles in full view, flagging articles, or marking articles as helpful or unhelpful.
-   View successful actions by selecting the Actions history icon.

For more information, see [Use AI search in Recommended Actions to resolve cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba-use-ai-search.md).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

[Related Items](tech-product-support-record-page.md#section_b1b_dfh_z1c)

</td><td>

The Related Items tab provides access the case-related lists.The Technology product support record page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

</td></tr><tr><td>

Attachments

</td><td>

The Attachments tab provides access to case-related attachments. From this tab, agents can view and download attachments.

</td></tr><tr><td>

Templates

</td><td>

The Templates tab provides access to available form templates which enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a record such as an incident or change.

</td></tr><tr><td>

Response Templates

</td><td>

The Response Templates tab provides access to available response templates. These templates contain reusable messages that agents can copy to provide quick and consistent messages to customers.

</td></tr><tr><td>

Email Templates

</td><td>

The Email Templates tab provides access to available email templates. These templates contain default values for fields that agents can add to email messages. These default values can include the recipients \(email addresses in the To, Cc, and Bcc fields\), the sender, the subject of the email, and text to include in the message body.

</td></tr></tbody>
</table>## Recommended Actions search component

The Recommended Actions component appears as a tab in the contextual side pane and provides agents with an AI search capability. Agents can search for information, review and attach knowledge articles, and attach similar cases.

By default the AI search configuration searches on the case short description.

For knowledge articles, an agent can view an article and attach the article to the current case. After attaching an article, the article is displayed in the Attached Knowledge list of the Related Records tab.

-   Selecting **Review and attach article** displays the article in the contextual side panel.
-   Selecting **Attach this article** attaches the knowledge article to the current case.

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

## Related Items component

The Technology product support record page incorporates related items functionality into the contextual side panel. The Related Items tab provides agents with access to the case-related lists. These lists are displayed in an accordion format that agents can expand and collapse as needed.

![The technology product support record page related lists component in the contextual side panel uses an accordion format to expand and display related list items](../image/front-line-case-page-related-lists.png "Technology product support record page related lists component")

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format. If a related list is empty, agents can select Create one in the list to create a record.

The related items component in the contextual side panel includes the following related lists:

-   Affected Install Base Items
-   Tasks
-   SLAs
-   Special Handling Notes List
-   Escalations
-   Child Cases
-   Change Requests
-   Blocked By
-   Related Parties
-   Attached Knowledge
-   Knowledge Gaps
-   Emails
-   Draft Emails
-   Task Skills
-   Work Orders

Related lists include the following actions:

-   **Create**: Opens an empty record in a subtab that the agent can use to create a new item.
-   **View all**: Opens a list of records in a subtab.
-   **Show more**: Is displayed for lists that have more than five items.

The items in an expanded list are displayed as cards. An expanded list shows one card for each item in the list.

-   Agents can open an item in a subtab.
-   If a list has more than five items, it includes an **Show more** option.

## Creating a case

Agents can create a technology product support case by selecting **Create case** from the More Actions menu in the action bar.

Creating a case opens a service selector modal and displays the services defined for the Technology Product Support case type. From this modal, agents can:

-   Search for a service.
-   Select a service.
-   Select **Create case**.

The system creates the case and displays the new case record.

**Note:** This action is active by default for the Technology product support record page.

## Using Now Assist for CSM to generate resolution notes for a case

Agents can automatically generate the resolution notes for a case, propose the resolution to the customer, and add the resolution information to the case record by using the resolution notes generation skill in the Now Assist for Customer Service Management \(CSM\) application.

Selecting the **Propose Solution** UI action on a case record displays the Propose Solution modal. If the **Resolution notes** field on the case record is empty, the resolution notes that generation skill adds the information to this field in the modal. For more information, see [Generate the resolution notes for a case by using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-generate-resolution.md).

**Note:** The resolution notes that generation skill requires a minimum of 200 words in the case record to generate the resolution notes. If the resolution notes can’t be generated, the system displays a message below the **Resolution notes** field.

To use the resolution notes generation skill with the Technology product support record page variant:

-   [Activate Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-supporting-info.md).
-   [Configure the resolution notes generation skill in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-configuring.md).
-   [Configure the Propose Solution UI action and declarative action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-config-propose-solution.md).

**Parent Topic:**[Exploring Technology Product Support Case](tech-product-support-case-app.md)


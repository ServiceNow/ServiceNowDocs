---
title: Order case record page
description: The Order case record page displays information about order cases and the associated list of order case line items in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Order case pages, Order Operations Case Management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Order case record page

The Order case record page displays information about order cases and the associated list of order case line items in CSM Configurable Workspace.

![Order case page with customer and account information, SLA, and case details. Center panel displays the Order Case Line list. Page also includes the configurable side panel.](../image/csm-order-ops-order-case-page.png "Order case page with Order Case Line list")

Customer service agents use this page to do the following:

-   View details about the order case and the order case line items.
-   Add or remove orders or order lines to the order case as order case line items.
-   Create new order case line items.
-   Edit order case line item details.
-   Create tasks for order case line items.

## Order case record page components

The Order case record page includes the following components:

<table id="table_pk2_g1w_q1c"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order case form heading

</td><td>

The form heading displays the order case short description. If there is no short description, it displays the order case number. The form heading also includes the action bar and record tags.

</td></tr><tr><td>

Order case action bar

</td><td>

The action bar contains the actions available to users while working on order case records. The specific actions are determined by factors such as the user role, order case state, and other attributes.-   **In-progress Actions**: This icon provides a list of minimized [modeless dialogs](csm-front-line-case-page-modeless-dialogs.md). It includes a badge that displays the number of items in the list. From this list, an agent can select an item to open the minimized comment, work note, or email.
-   **Compose**: Compose comments, work notes, and emails in modeless dialogs.
-   **Manage case**: Perform case management actions such as requesting information or proposing a solution.
-   **Save**: Save changes to the order case record.
-   **More Actions**: Perform additional actions such as proposing a major case or reporting a knowledge gap.

</td></tr><tr><td>

Account lookup

</td><td>

Agents can use the account lookup component to do the following:-   Search for an account.
-   Link or unlink an account.
-   Select a reference field on a lookup card, such as a contact name, to open the reference in a sub-tab.
-   Select a phone number on a lookup card to make a call.

The account lookup component displays information in record cards. These cards display contact information and provide quick access to customer details such name, address, and phone.

</td></tr><tr><td>

SLA

</td><td>

Displays active SLAs for the order case, including time remaining, the SLA state, and any breaches.

</td></tr><tr><td>

Case details

</td><td>

The case details component includes collapsible sections for:-   Case Details
-   Notes
-   Closure Information
-   Related Records

This component also includes a menu with additional form actions, such as personalizing the form, exporting data, and copying the URL.

</td></tr><tr><td>

Case summarization

</td><td>

The case summarization component appears above the Order Case Line list. When an agent opens an order case, the component is collapsed and in the default state.Agents can use this component to do the following:

-   Summarize order case details.
-   Generate order case resolution notes.
-   Generate knowledge articles.
-   Generate email reply recommendation.

**Note:** The case summarization component requires the [Now Assist for Customer Service Management \(CSM\)](now-assist-csm.md) application to be activated and configured.

</td></tr><tr><td>

Order Case Line list

</td><td>

The Order Case Line list component displays the order case line items associated with the order case. Order case line items can be created for orders or order lines.-   If an order case is created for one or more orders, the system converts the order header from each customer order to a case line item on the order case.
-   If an order case is created for one or more order lines from a single order, the system converts the selected order lines from the customer order to case line items on that order case.

</td></tr><tr><td>

Order Case Line action bar

</td><td>

The Order Case Line action bar contains the actions available to users while working on order case line records.-   **New**: Opens a Create New Order Case Line record in a separate tab. Fill in the fields and select **Save** to add the order case line item to the list.
-   **Add**: Displays one of the following modals depending on the origin of the order case:

    -   Add order lines to case
    -   Add orders to case
Select one or more orders or order lines and then select **Add** to add the selected orders or order lines to the Order Case Line list.

-   **Create task**: Creates a task for the selected order case line item in a separate tab. Fill in the fields on the Create New Case Line Task record and select **Save**.

After selecting an order case line item, agents can edit selected order case line item details, assign an order case line item to themselves, or delete a case line.

-   **Edit**: Displays the details for the selected order case line item in a panel. Make the necessary changes and select **Update** at the bottom of the panel.
-   **Assign to me**: Assigns the selected order case line item to the current user.
-   **Delete**: Deletes the selected order case line item. Select **Delete all** in the confirmation pop-up window.

</td></tr><tr><td>

Activity stream

</td><td>

The activity stream component displays a list of activities occurring on an order case record. This list can be collapsed to provide a quick view of case activities or expanded to provide more detail about individual activities.The Order case record page uses [modeless dialogs](csm-front-line-case-page-modeless-dialogs.md) for composing comments, work notes, and emails. For more information, see the [Composing emails, comments, and work notes](csm-order-ops-order-case-record-page.md#section_eqt_5h5_ncc) section below.

</td></tr><tr><td>

Contextual side panel

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Order case record page includes the following tabs.

-   Activity stream
-   Attachments
-   Recommended Actions search
-   [Related Lists](csm-front-line-case-page.md#section_urr_nrh_s1c)
-   Email Templates
-   Response Templates
-   Form Templates

 For more information about related lists, see the [Order case record page related lists](csm-order-ops-order-case-record-page.md#section_ksh_pp3_lcc) section below.

 **Note:** The Order Operations Case Management application does not include response templates. To configure a response template, see [Create or modify a response template](https://www.servicenow.com/docs/access?context=create-modify-templated-snippet&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>## Order case record page settings

The Order case record page includes the following settings.

<table id="table_zqv_lvv_q1c"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Enabling the **Active** check box makes the page available to the selected audience. The Order case record page is active by default.The active setting combined with the page order determines the page that CSM Configurable Workspace uses to display record information. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the Order case record page is -1000.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The Order case record page has the following condition: **table=sn\_order\_case**This condition limits the use of the Order case record page to records from the Order Case \[sn\_order\_case\] table and tables that extend the Order Case table.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see a record page. The Order case record page does not have a specified audience.For more information, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr></tbody>
</table>To access the settings for this page variant:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the Record section of the Pages and variants list, select **Front-line case page**.
4.  Select **Settings** at the top of the page.

## Order case record page related lists

Related lists appear in the Related Lists tab in the contextual side panel.

The related lists component provides access to the order case related lists. This component uses an expandable accordion format. Agents can expand the desired lists to see the related items. This component also displays an icon with the number of items in a list.

1.  Case Tasks
2.  Order Case Lines
3.  Order Tasks
4.  SLAs
5.  Emails
6.  Draft Emails
7.  Knowledge
8.  Knowledge Gaps
9.  Child Cases

The items in an expanded list are displayed as cards. An expanded list shows one card for each item in the list, up to a maximum of 8 cards.

-   Agents can open an item in a sub-tab.
-   If a list has more than five items, it includes a Show more option.

Related lists include the following actions:

-   **Refresh**: refreshes the items in the list.
-   **Create**: opens a blank record in a sub tab that the agent can use to create a new item.
-   **View all**: opens a list of records in a sub tab.
-   **Show more**: is displayed for lists that have more than five items.

## Composing emails, comments, and work notes

The Order case record page uses modeless dialogs to create and post comments and work notes to the activity stream and to compose and send emails.

A modeless dialog is a window that appears in a workspace as an overlay on top of the main window content. This overlay enables users to interact with the window content and the overlay content at the same time.

The Compose group of actions on the Order case record page includes:

-   Compose Comments
-   Compose Email
-   Compose Work Notes\(Private\)

These actions launch the corresponding modeless dialogs \(the behavior is the same as the Front-line case page\).

The email templates should be accessed from email dialog.

For more information about composing emails, comments, and work notes, see [Modeless dialogs](csm-front-line-case-page-modeless-dialogs.md).


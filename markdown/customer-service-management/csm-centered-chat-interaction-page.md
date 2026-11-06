---
title: CSM centered chat interaction record page
description: The CSM centered chat interaction record page displays a chat component in the center of the workspace. This format enables agents to manage customer chat conversations alongside customer history and interaction details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/csm-centered-chat-interaction-page.html
release: australia
topic_type: concept
last_updated: "2026-10-20"
reading_time_minutes: 4
breadcrumb: [Record pages, Record pages and page templates, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM centered chat interaction record page

The CSM centered chat interaction record page displays a chat component in the center of the workspace. This format enables agents to manage customer chat conversations alongside customer history and interaction details.

\[Omitted image "centered-chat-interaction-record-page.png"\] Alt text: CSM centered chat interaction record page with customer history, chat, and contextual side panel components

The CSM centered chat interaction record page moves the chat component to the center of the workspace. This layout enables agents to manage chats and view information, such as customer history and interaction details, that help them resolve issues.

## Page structure

The CSM centered chat interaction record page contains three panels.

<table id="table_jx2_dkp_q2c"><thead><tr><th>

Panel

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Left panel

</td><td>

The left panel includes two tabs: Customer and Interaction.

 The **Customer** tab includes the contact or consumer lookup component and customer history.

-   Contact or consumer [lookup component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-record-page-lookup-component.md):
    -   Includes the contact or consumer lookup card which agents can use to search for, select, and verify a customer.
    -   When a customer has been selected and linked to an interaction, a card with customer information is displayed at the top of the Customer tab.
-   Customer history: includes the [Customer History component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/centered-chat-customer-history-component.md), which displays customer, consumer, or account history information, depending on the customer information provided on the interaction record.

 The **Interaction** tab includes the Interaction record form fields.

</td></tr><tr><td>

Center panel

</td><td>

The center panel includes the chat component. This panel is hidden when there is no chat conversation.

</td></tr><tr><td>

Right panel

</td><td>

The right panel contains the [contextual side panel component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/centered-chat-side-panel-component.md), which includes the following tabs:-   Recommended Actions search
-   Related Items
-   Attachments
-   Templates
-   Collaborate

</td></tr></tbody>
</table>## Page components

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

Agents can create multiple tags for a record and then use the tags to group and organize records.

</td></tr><tr><td>

[Action bar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/centered-chat-action-bar-component.md)

</td><td>

The action bar contains the actions available to users while working on chat interaction records.**Note:** The specific actions available are determined by factors such as the user role and other attributes.

</td></tr><tr><td>

[Contact or consumer lookup component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-record-page-lookup-component.md)

</td><td>

The **Customer** tab includes the contact or consumer lookup component. Agents can use this component to search for contacts or consumers and link them to interaction records.

</td></tr><tr><td>

[Customer History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/centered-chat-customer-history-component.md)

</td><td>

The Customer History component displays customer, consumer, or account history information, depending on the field selections on the interaction record. This component can also display live call transcript.**Note:** Live call transcript requires additional configuration.

</td></tr><tr><td>

Interaction details

</td><td>

The interaction details include information about the interaction including the account and contact, short description, and record state.

</td></tr><tr><td>

[Contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/centered-chat-side-panel-component.md)

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues, including Recommended Actions, related items, and attachments.

</td></tr><tr><td>

[Thin compose modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-front-line-case-page-modeless-dialogs.md)

</td><td>

Thin compose modeless dialogs enable agents to initiate a work note or email in the activity stream and then open the text in a modeless dialog.**Note:** For the CSM centered chat interaction record page, the thin compose modeless dialogs feature is hidden by default and can be enabled by the admin.

</td></tr></tbody>
</table>## Plugin information

The CSM centered chat interaction page template and record page are included with the CRM Workspace plugin \(com.snc.uib.csm\_agent\_workspace\).

## Default interaction record page in CRM Workspace

The [CSM Interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-interaction-record-page.md) is the default experience for chat interaction in CRM Workspace. This page includes the chat component in the left panel.

To use the CSM centered chat interaction record page in CRM Workspace, enable the page and set the **Order** value. For more information, see [Set record page order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-ws-set-record-page-order.md).


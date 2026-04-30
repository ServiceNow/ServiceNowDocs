---
title: CSM Configurable Workspace form features
description: CSM Configurable Workspace form features include account hierarchy, special handling notes, and agent actions.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# CSM Configurable Workspace form features

CSM Configurable Workspace form features include account hierarchy, special handling notes, and agent actions.

## Account hierarchy

From the Account form, customer service agents can click the open hierarchy icon \(![Open hierarchy icon](../../../product/customer-service-management/image/workspace-account-hierarchy-icon.jpg)\) in the **Name** field to see the parent-child account relationships in the Account Hierarchy pop-up window. The account hierarchy is available for accounts that have a parent or child account.

![Window displaying the parent-child relationship for an account. For the text description, refer to the text that follows in the Account Hierarchy section.](../../../product/customer-service-management/image/csm-config-workspace-account-hierarchy.png "CSM Workspace Account Hierarchy pop-up window")

The account hierarchy uses a tree structure to show the parent, child, and sibling accounts. The parent view displays the current account, the parent account \(if applicable\), and any child or sibling accounts. The full view displays the entire structure of the organization from the root account. The current account is highlighted in the account structure.

Customer service agents can:

-   Expand and collapse the tree structure.
-   Switch between the parent view and the full view of the account hierarchy.
-   Click an account to open the Account form in a sub tab.

For information about creating an account hierarchy, see [Account hierarchy](../../../product/customer-service-management/concept/c_AccountHierarchy.md).

## Special handling notes

Special handling notes bring important information about individual records to the attention of the customer service agent. If special handling notes are available for a record, these notes are displayed in a pop-up window when the record is opened in a CSM workspace. Notes can also be displayed in an embedded list or a related list on a record form. Notes are ordered by priority in the pop-up window and in lists.

Agents can see the priority, short description, and message for each note. A note can be assigned one of the following priorities, which also have associated colors.

-   Priority 1 — red
-   Priority 2 — orange
-   Priority 3 — purple
-   Priority 4 — gray

![Window displaying special handling information for records requiring attention, based on priority. For the text description, refer to the preceding text in the Special handling notes section.](../../../product/customer-service-management/image/csm-config-workspace-special-handling-note.png "Special handling notes pop-up window")

Agents can:

-   Dismiss individual notes. When all notes are dismissed, the pop-up window closes.
-   Close the window.

In the Special Handling Notes module on the platform interface:

-   Users with the sn\_shn.admin role can configure special handling notes and specify properties.
-   Users with the sn\_shn.admin or sn\_customerservice\_manager roles can create special handling notes.

For more information about configuring the special handling notes feature, see [Special handling notes overview](../../../product/customer-service-management/concept/c_OnScreenAlerts.md).

## Agent actions

Actions available to customer service agents appear in the form header as buttons or menu items.

-   For CSM Agent Workspace, actions must be enabled for each form by the workspace administrator. For more information, see Set up custom UI actions in legacy workspace.
-   For CSM Configurable Workspace, you can link UI actions to form actions. For more information, see [Set up a form action in CSM Configurable Workspace](../../../product/customer-service-management/task/config-csm-config-ws-form-action.md).

The **Create Knowledge** action requires the following setup:

-   Activate the Knowledge Management Advanced Installer plugin \(com.snc.knowledge\_advanced.installer\).
-   Set the **sn\_customerservice.enable\_knowledge\_kcs** property to true.
-   Set the KCS Article template to true \(navigate to **Knowledge** &gt; **Administration** &gt; **Article Templates**\).

## Agent assist

Agent assist is available on the Interaction form in CSM Configurable Workspace. Users with the customer service agent role \(sn\_customerservice\_agent\) can use Agent assist to search for information from an interaction. By default, the available search sources include Knowledge articles, Service Catalog, and ServiceNow Community blogs and posts. For more information, see Set up Agent assist.

For more information on how to enable Recommended Actions - AI search and disable Agent Assist, see [Enable AI search in Recommended Actions](../../../product/customer-service-management/task/migrate-ra-agent-assist.md).


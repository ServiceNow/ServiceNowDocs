---
title: CSM Configurable Workspace form features
description: Use features available on CSM Configurable Workspace forms to view fields with unsaved changes, edit the text in the record header field, and view special handling notes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace form features

Use features available on CSM Configurable Workspace forms to view fields with unsaved changes, edit the text in the record header field, and view special handling notes.

For more information about working with forms, see the following topics in the [Configurable Workspace UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/workspace-landing-page.md) documentation:

-   [Administering forms for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/administer-forms-configurable-workspace.md)
-   [Using forms in Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/using-forms-configurable-workspace.md)

## Visual field indicators for unsaved changes

Use visual indicators in CSM Configurable Workspace such as icons and background colors to indicate form fields with unsaved changes. When this feature is enabled, customer service agents see the following indicators:

-   Dot icons appear next to the field labels for updated fields.
-   Background colors change for updated fields.
-   Tooltips identify each updated field.

Field updates include manual changes made by the agent, by the application of a template, or automatic updates made by AI. These visual indicators are removed when the agent saves the form.

This feature is available for the following CSM Configurable Workspace [record pages](../concept/csm-config-workspace-record-pages.md):

-   Front-line case page
-   CSM default record page
-   Email interaction record page
-   CSM voice interaction record page
-   CSM Interaction record page
-   CSM centered chat interaction record page

Users with the administrator role can enable the background colors along with a dot icon to indicate fields with unsaved changes. The workspace-level property **enableBgColorForUnsavedFieldIndicator** controls these indicators. This property is set to true by default.

To set this property:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experience**.
2.  Select **CSM/FSM Configurable Workspace**.
3.  In the UX Page Properties related list, select **enableBgColorForUnsavedFieldIndicator**.
4.  Update the value in the **Value** field.
5.  Select **Update**.

## Editable record headers

Customer service agents can edit the short description \(primary field\) of a record directly from the record header field. To edit the text, simply click in the record header field and make the changes.

This feature is available on the following CSM Configurable Workspace record pages:

-   [Front-line case page](../concept/csm-front-line-case-page.md)
-   [CSM Interaction record page](../concept/csm-interaction-record-page.md)
-   [CSM default record page](../concept/csm-default-record-page.md)
-   [CSM voice interaction record page](../concept/csm-native-voice-record-page.md)
-   [CSM centered chat interaction record page](../concept/csm-centered-chat-interaction-page.md)
-   [Email Interaction record page](../concept/csm-email-interaction-record-page.md)

The editable record header feature includes the following benefits:

-   The system validates the text entered in the record header field.
-   The **Short description** field \(primary field\) automatically updates with the changes made in the record header field.
-   Changes to the record header field are saved when the agent saves the record.
-   Empty record header fields display placeholder text. For example, default placeholder text such as **Enter short description here** is displayed for new record forms.
-   The text in the record header field is truncated if it is longer than the field width. Hovering over the field displays the full text.
-   Editing permissions for the record header field are restricted to authorized agent roles.

**Note:** The record header is not editable if the form field used as the record header is either read-only or not present on the form.

Suggestions for using the editable record header feature:

-   Use only static text fields such as **Short description** or **Subject** as the editable record header field.
-   Do not re-use the placeholder text as the value in the record header field as the placeholder text indicates that the field is empty.

    **Note:** If the placeholder text is used as the value in the record header field, the agent must double-click the record header field to change the text.


## Field label positions

The labels for form fields can appear either above the field or next to the field. The UI Builder configuration property **Label value layout** controls the position of the form fields. This property has the following options:

-   Stacked: Labels appear on top of the fields.
-   Tabbed: Labels appear next to the fields.

This property is available for the following CSM Configurable Workspace [record pages](../concept/csm-config-workspace-record-pages.md):

-   Front-line case page
-   CSM default record page
-   Email interaction record page
-   CSM voice interaction record page
-   CSM Interaction record page
-   CSM centered chat interaction record page

## Special handling notes

Special handling notes bring important information about individual records to the attention of the customer service agent. If special handling notes are available for a record, these notes are displayed in a pop-up window when the record is opened in a CSM workspace. Notes can also be displayed in an embedded list or a related list on a record form. Notes are ordered by priority in the pop-up window and in lists.

Agents can see the priority, short description, and message for each note. A note can be assigned one of the following priorities, which also have associated colors.

-   Priority 1 — red
-   Priority 2 — orange
-   Priority 3 — purple
-   Priority 4 — gray

![Window displaying special handling information for records requiring attention, based on priority. For the text description, refer to the preceding text in the Special handling notes section.](../image/csm-config-workspace-special-handling-note.png "Special handling notes pop-up window")

Agents can:

-   Dismiss individual notes. When all notes are dismissed, the pop-up window closes.
-   Close the window.

In the Special Handling Notes module on the platform interface:

-   Users with the sn\_shn.admin role can configure special handling notes and specify properties.
-   Users with the sn\_shn.admin or sn\_customerservice\_manager roles can create special handling notes.

For more information about configuring the special handling notes feature, see [Special handling notes overview](../concept/c_OnScreenAlerts.md).

## Agent actions

Actions available to customer service agents appear in the form header as buttons or menu items.

For CSM Configurable Workspace, you can link UI actions to form actions. For more information, see [Set up a form action in CSM Configurable Workspace](../task/config-csm-config-ws-form-action.md).

The **Create Knowledge** action requires the following setup:

-   Activate the Knowledge Management Advanced Installer plugin \(com.snc.knowledge\_advanced.installer\).
-   Set the **sn\_customerservice.enable\_knowledge\_kcs** property to true.
-   Set the KCS Article template to true \(navigate to **Knowledge** &gt; **Administration** &gt; **Article Templates**\).

## Agent assist

Agent assist is available on the Interaction form in CSM Configurable Workspace. Users with the customer service agent role \(sn\_customerservice\_agent\) can use Agent assist to search for information from an interaction. By default, the available search sources include Knowledge articles, Service Catalog, and ServiceNow Community blogs and posts.

For more information on how to enable Recommended Actions - AI search and disable Agent Assist, see [Enable AI search in Recommended Actions](../task/migrate-ra-agent-assist.md).

## Account hierarchy

From the Account form, customer service agents can click the open hierarchy icon \(![Open hierarchy icon](../image/workspace-account-hierarchy-icon.jpg)\) in the **Name** field to see the parent-child account relationships in the Account Hierarchy pop-up window. The account hierarchy is available for accounts that have a parent or child account.

![Window displaying the parent-child relationship for an account. For the text description, refer to the text that follows in the Account Hierarchy section.](../image/csm-config-workspace-account-hierarchy.png "CSM Workspace Account Hierarchy pop-up window")

The account hierarchy uses a tree structure to show the parent, child, and sibling accounts. The parent view displays the current account, the parent account \(if applicable\), and any child or sibling accounts. The full view displays the entire structure of the organization from the root account. The current account is highlighted in the account structure.

Customer service agents can:

-   Expand and collapse the tree structure.
-   Switch between the parent view and the full view of the account hierarchy.
-   Click an account to open the Account form in a sub tab.

For information about creating an account hierarchy, see [Account hierarchy](../concept/c_AccountHierarchy.md).


---
title: CSM default record page
description: The CSM default record page provides case management features and functionality and enables agents to create, monitor, and resolve cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Record pages, Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM default record page

The CSM default record page provides case management features and functionality and enables agents to create, monitor, and resolve cases.

The CSM default record page includes the basic structure for a record page, including record information, a communication interface, and suggestions for issue resolution. This page is also known as the standard record page.

![The CSM default record page provides agents with an overview of case record details and the activity stream. It also provides access to multiple features in the contextual side panel.](../image/csm-default-record-template.png "CSM default record page")

The CSM default record page is included with the CSM/FSM Configurable Workspace experience.

## Activity stream component

The activity stream component on the CSM default record page displays a list of activities occurring on a case record. This list can be collapsed to provide a quick view of case activities or expanded to provide more detail about individual activities. For more information about this component, see [Activity stream component](csm-front-line-case-page.md#section_ntx_lnh_s1c).

## Action bar component

The action bar contains the actions available to users while working on case records. The specific actions are determined by factors such as the user role, case state, and other attributes.

-   **Create**: Create records such as work orders, incidents, and requests.
-   **Manage case**: Perform case management actions such as accepting a case or requesting information.
-   **Save**: Save changes to the case record.
-   **Follow**: Receive notifications when comments or work notes are added to the record.
-   **More Actions**: Perform additional actions such as following a case, proposing a major case, or reporting a knowledge gap.

The CSM default record page action bar includes the **Follow** action in the More Actions menu. Selecting this action enables you to receive notifications when comments or work notes are added to the record.

You receive notifications in the Notifications menu at the top of the page according to your notification preferences. You can select the notification to open the record that was updated. For more information, see the following topics:

-   [Configure Next Experience notification preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-notifications-preferences.md)
-   [Follow records in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/follow-records-in-next-experience.md)

When the **Follow** action is selected, the button toggles to **Unfollow**. To stop receiving notifications, select **Unfollow**.

## Thin compose modeless dialogs

The CSM default record page uses the thin compose modeless dialog feature, which incorporates modeless dialogs into the activity stream. This feature enables agents to initiate a comment, work note, or email in the activity stream and then open the text in a modeless dialog. For more information, see [Thin compose modeless dialogs](csm-front-line-case-page-modeless-dialogs.md#section_nws_1rs_rfc).

## Record presence feature

The CSM default record page and the CSM Interaction record page include the record presence feature. This feature allows agents to see other users who are viewing the same record and enables easy collaboration.

The user presence component displays an icon in the form header that shows the user who is currently viewing the record. For three or more users, the component displays two icons plus a number that represents additional users.

-   Hover over an icon to see more information about a user.
-   Click the number icon to see more information about the additional users.

For more information about this feature, see [User presence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UserPresence.md).

## Email templates feature

The CSM default record page includes the Email Templates feature. CSM Configurable Workspace pages that use the CSM default record page include the Email Templates tab in the contextual side panel.

These templates contain default values for fields that agents can easily add to email messages in the Compose panel on case records. These default values can include the recipients \(email addresses in the To, Cc, and Bcc fields\), the sender, the subject of the email, and text to include in the message body.

Users with the system administrator role can configure email templates by navigating to **All** &gt; **Email Client** &gt; **Email Client Templates** and selecting **New**. For more information, see [Create an email client template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAnEmailClientTemplate.md).

Agents can use this feature to do the following:

-   View available email templates.
-   Select an email template to display the template details.
-   Apply the selected template to an email in the Compose panel.

For more information, see [Compose an email from an email template](../task/compose-email-from-email-template.md).

## Creating emails and applying email templates

Customer service agents can create emails from case records in the following ways:

-   By selecting **Email** at the top of the activity stream to open the Compose Email component.
-   By selecting the More actions \(![agent workspace more actions menu](../image/agent-workspace-more-ui-actions-icon.jpg)\) menu in the case activity bar and then selecting **Compose email** to open a draft email in a new tab.

When creating emails, agents can apply templates to add content to the draft emails, such as the subject line and message body. To apply a template:

1.  Select the Apply email templates icon \(![Compose email apply templates icon](../image/csm-email-modeless-dialog-apply-template.png)\) in the Compose email footer.

    The system displays a list of available templates. It does not display quick messages or response templates.

2.  Select a template from the list. You can also search for a specific template.

    The system adds the contents of the template to the body of the email.


**Note:** If no templates are available, the icon does not appear in the footer.

## Recommended Actions feature

The Recommended Actions tab is now available as the first tab in the contextual side panel and is enabled for Pro customers. It includes a set of base system recommendations, such as similar incidents and similar open incidents.

The Recommended Actions tab includes [AI search](ra-csm-ai-search.md) functionality and Suggested Actions.

-   [AI search](ra-csm-ai-search.md) tab: Agents can use AI search to find relevant resources or resolutions for customer issues. The search feature displays an initial set of search results based on the text in the case short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search. From the list of search results, agents can select a source to see search results of that type.

    The following table shows the actions that an agent can perform on search results:

<table id="table_mc2_njv_bfc"><thead><tr><th>

Source type

</th><th>

Guidance actions

</th></tr></thead><tbody><tr><td>

Knowledge base articles

</td><td>

-   Attach and add a link in email.
-   Attach and add a link in comment.
-   Add a link in work note.
-   Copy a link.
-   Read an article.
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
</table>    For all the other source types, default guidance is supported. The Default guidance for search results is a guidance that can be used for any search sources that don't have mapped guidances. For more information on default guidance, see [Default guidance for search results](ra-csm-guidances-default-guidance-search.md).

    For more information on how to avail the AI search feature in Recommended Actions, see [Enable AI search in Recommended Actions](../task/migrate-ra-agent-assist.md).

    For more information, see [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md).

    **Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

-   Suggested Actions tab: This tab displays relevant actions to agents based on a context of a record or recommend a value for a field. For more information on how to configure contexts to display relevant actions for the agent, see [Recommended Actions](configure-nba.md).

    The Suggested Actions tab is available in the base system for Pro customers and doesn’t require additional configuration. It becomes visible when the Task Intelligence plugin is installed. Non-Pro customers can enable the tab manually.

    -   Without the plugin, only the Search tab is visible on the Front-line case page.

    -   With the plugin installed, both Search and Suggested Actions tabs appear, and recommendations are shown under Suggested Actions.

    -   If the plugin is uninstalled, the Suggested Actions tab is no longer available.


## Editable record header field

Agents can edit the short description of a record directly from the record header field. For more information, see [Editable record headers](../reference/csm-workspace-agent-actions.md#section_hhb_1tj_23c).

## Collaborate component

The Collaborate component enables agents to communicate with stakeholders and other users and gather information for case resolution. This component is available on the CSM default record page n the contextual side panel. For more information, see [Collaborate component](csm-config-ws-collaborate-component.md).


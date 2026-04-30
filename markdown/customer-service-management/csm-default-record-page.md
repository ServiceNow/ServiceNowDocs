---
title: CSM default record page
description: The CSM default record page provides CSM case management features and functionality and enables agents to create, monitor, and resolve cases.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# CSM default record page

The CSM default record page provides CSM case management features and functionality and enables agents to create, monitor, and resolve cases.

The CSM default record page includes the basic structure for a record page, including record information, a communication interface, and suggestions for issue resolution. This page is also known as the standard record page.

![The CSM default record page provides agents with an overview of case record details and the activity stream. It also provides access to multiple features in the contextual side panel.](../image/csm-default-record-template.png "CSM default record page")

The CSM default record page is included with the CSM/FSM Configurable Workspace experience.

## Record presence feature

The CSM default record page and the CSM Interaction record page include the record presence feature. This feature allows agents to see other users who are viewing the same record and enables easy collaboration.

The user presence component displays an icon in the form header that shows the user who is currently viewing the record. For three or more users, the component displays two icons plus a number that represents additional users.

-   Hover over an icon to see more information about a user.
-   Click the number icon to see more information about the additional users.

For more information about this feature, see [User presence](https://www.servicenow.com/docs/access?context=c_UserPresence&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Email templates feature

The CSM default record page includes the Email Templates feature. CSM Configurable Workspace pages that use the CSM default record page include the Email Templates tab in the contextual side panel.

These templates contain default values for fields that agents can easily add to email messages in the Compose panel on case records. These default values can include the recipients \(email addresses in the To, Cc, and Bcc fields\), the sender, the subject of the email, and text to include in the message body.

Users with the system administrator role can configure email templates by navigating to **All** &gt; **Email Client** &gt; **Email Client Templates** and selecting **New**. For more information, see [Create an email client template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailClientTemplate&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Agents can use this feature to do the following:

-   View available email templates.
-   Select an email template to display the template details.
-   Apply the selected template to an email in the Compose panel.

For more information, see [Compose an email from an email template](../task/compose-email-from-email-template.md).

## Recommended Actions feature

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
</table>    For all the other source types, default guidance is supported. The Default guidance for search results is a guidance that can be used for any search sources that don't have mapped guidances. For more information on default guidance, see .

    For more information on how to avail the AI search feature in Recommended Actions, see [Enable AI search in Recommended Actions](../task/migrate-ra-agent-assist.md).

    For more information, see [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md).

    **Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

-   Suggested Actions tab: This tab displays relevant actions to agents based on a context of a record or recommend a value for a field. For more information on how to configure contexts to display relevant actions for the agent, see [Recommended Actions](configure-nba.md).


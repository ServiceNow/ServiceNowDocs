---
title: Playbook contextual side panel component
description: The playbook contextual side panel component provides agents with access to tools and information such as the activity stream, templates, and attachments.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Playbook page templates, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Playbook contextual side panel component

The playbook contextual side panel component provides agents with access to tools and information such as the activity stream, templates, and attachments.

The contextual side panel component provides agents with the following functionality.

<table id="table_orh_5rr_m1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity Stream

</td><td>

The activity stream displays a list of activities occurring on a case record. For more information, see [Playbook activity stream component](csm-playbook-activity-stream-component.md).

</td></tr><tr><td>

Agent Assist

</td><td>

Agent assist provides agents with a list of resources that show possible solutions for the current record. This list is based on the record short description.

</td></tr><tr><td>

Search

</td><td>

The Search tab includes [AI search](ra-csm-ai-search.md) functionality. Agents can use AI search to find relevant resources or resolutions for customer issues.The search feature displays an initial set of search results based on the text in the case short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

From the list of search results, agents can do the following:

-   Select a source to see search results of that type.
-   Filter the list of search results.
-   Sort the list of search results.
-   Open the search results in full view in a record sub-tab.
-   Take the following actions:
    -   View and attach article
    -   Perform other actions such as reading articles in full view, flagging articles, or marking articles as helpful or unhelpful.
-   View successful actions by selecting the Actions history icon.

For more information, see [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

Related Items

</td><td>

The Related Items tab provides access to the case-related lists.The Case playbook: horizontal stages page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

For more information, see [Playbook related items component](csm-playbook-related-items-component.md).

</td></tr><tr><td>

Attachments

</td><td>

The Attachments tab provides access to case-related attachments. From this tab, agents can view and download attachments.

</td></tr><tr><td>

Response Templates

</td><td>

The Response Templates tab provides access to available response templates. These templates contain reusable messages that agents can copy to provide quick and consistent messages to customers.

</td></tr><tr><td>

Email Templates

</td><td>

The Email Templates tab provides access to available email templates. These templates contain default values for fields that agents can add to email messages. These default values can include recipients \(email addresses in To, Cc, and Bcc\), sender, subject, and text for the message body.For more information, see [Email Templates](https://www.servicenow.com/docs/access?context=configure-email-templates&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Templates

</td><td>

The Templates tab provides access to available form templates which enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a new record such as an incident or change.

</td></tr><tr><td>

Record Information

</td><td>

The Record Information tab includes the following cards:-   **Overview**: Displays relevant information about the case including the account and contact, the case priority, and the state.
-   **Contact**: Displays customer information including the name, title, phone numbers, and email address.
-   **Timeline**: Displays a chronological summary of case activities, including case state changes and interactions between the agent and the requester.
-   **Active SLA**: Displays active SLAs for the case, including time remaining, the SLA state, and any breaches.

</td></tr></tbody>
</table>
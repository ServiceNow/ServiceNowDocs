---
title: CSM Configurable Workspace contextual side panel components
description: Use the contextual side panel to quickly access tools and information directly from the record page, helping agents research and resolve customer issues without leaving the case view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-config-ws-side-panel-components.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace contextual side panel components

Use the contextual side panel to quickly access tools and information directly from the record page, helping agents research and resolve customer issues without leaving the case view.

The contextual side panel is embedded within multiple [record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-ws-pages-templates.md) in CSM Configurable Workspace. The side panel contains tabs with different functionality that vary depending on the record page. While the content within the side panel may be similar from one record page to another, the order and availability of the tabs may vary.

<table id="id_rzq_vgj_vfc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record Information

</td><td>

The Record Information tab includes the following cards:

-   Overview: Displays relevant information about the case including the account and contact, the case priority, and the state.
-   Active SLA: Displays active SLAs for the case, including time remaining, the SLA state, and any breaches.

 The cards that appear in the Record Information tab can be configured in the Front-line Case Page Ribbon Config ribbon configuration. For more information, see [Set up a ribbon configuration in CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/config-csm-config-ws-ribbon.md)

</td></tr><tr><td>

Recommended Actions

</td><td>

The Recommended Actions tab includes [AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-ai-search.md) functionality. Agents can use AI search to find relevant resources or resolutions for customer issues.

 The search feature displays an initial set of search results based on the text in the case short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

 From the list of search results, agents can do the following:

-   Select a source to see search results of that type.
-   Filter the list of search results.
-   Sort the list of search results.
-   Open the search results in full view in a record sub-tab.

 Agents can take the following actions:

-   View and attach an article.
-   Perform other actions such as reading articles in full view, flagging articles, or marking articles as helpful or unhelpful.
-   View successful actions by selecting the Actions history icon.

 For more information, see [Use AI search in Recommended Actions to resolve cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba-use-ai-search.md).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

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

The Email Templates tab provides access to available email templates. These templates contain default values for fields that agents can add to email messages. These default values can include the recipients \(email addresses in the To, Cc, and Bcc fields\), the sender, the subject of the email, and text to include in the message body.For more information, see [Email Templates](https://www.servicenow.com/docs/access?context=configure-email-templates&version=yokohama).

</td></tr><tr><td>

Related Lists

</td><td>

The Related Lists tab provides access to the record's related lists.Related lists appear in the side panel in an accordion format that agents can expand and collapse as needed. An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

</td></tr><tr><td>

Activity Stream

</td><td>

The activity stream displays a list of activities occurring on a case record. For more information, see [Playbook activity stream component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-activity-stream-component.md).

</td></tr><tr><td>

Agent Assist

</td><td>

Agent assist provides agents with a list of resources that show possible solutions for the current record. This list is based on the record short description.

</td></tr><tr><td>

Search

</td><td>

From the list of search results, agents can do the following: -   Select a source to see search results of that type.
-   Filter the list of search results.
-   Sort the list of search results.
-   Open the search results in full view in a record sub-tab.

Agents can take the following actions:

-   View and attach an article.
-   Perform other actions such as reading articles in full view, flagging articles, or marking articles as helpful or unhelpful.
-   View successful actions by selecting the Actions history icon.

For more information, see [Use AI search in Recommended Actions to resolve cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba-use-ai-search.md).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba.md) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

Related Items

</td><td>

The Related Items tab provides access to the case-related lists.The Case playbook: horizontal stages page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

For more information, see [Playbook related items component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-related-items-component.md).

</td></tr><tr><td>

Collaborate

</td><td>

The Collaborate feature enables agents to collaborate with stakeholders through multiple channels.For more information, see [Collaborate component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-ws-collaborate-component.md).

</td></tr></tbody>
</table>
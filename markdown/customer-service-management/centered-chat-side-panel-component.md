---
title: Contextual side panel component
description: The contextual side panel component includes different tools that agents can use to research and resolve customer issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/centered-chat-side-panel-component.html
release: australia
topic_type: reference
last_updated: "2026-10-19"
reading_time_minutes: 3
breadcrumb: [CSM centered chat interaction record page, Record pages, Record pages and page templates, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Contextual side panel component

The contextual side panel component includes different tools that agents can use to research and resolve customer issues.

The CSM centered chat interaction record page includes the contextual side panel component, which provides agents with the following functionality.

<table id="table_orh_5rr_m1c"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommended Actions

</td><td>

The Recommended Actions tab is available as the first tab in the contextual side panel. It includes a set of base system recommendations, such as similar incidents and similar open incidents.

The Recommended Actions tab includes [AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/ra-csm-ai-search.md) functionality and Suggested Actions.-   **AI search** tab: Agents can use AI search to find relevant resources or resolutions for customer issues. The search feature displays an initial set of search results based on the text in the interaction short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search. From the list of search results, agents can select a source to see search results of that type. For more information, see Search sources and guidance actions.

For all the other source types, the default guidance is supported. The default guidance for search results is a guidance that can be used for any search sources that don't have mapped guidances. For more information on default guidance, see [Default guidance for search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/ra-csm-guidances-default-guidance-search.md).

For more information, see the following topics:

    -   [Enable AI search in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migrate-ra-agent-assist.md)
    -   [Use AI search in Recommended Actions to resolve cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/nba-use-ai-search.md)
**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/nba.md) application \(sn\_cs\_nb\_action\) which is included with the CRM Workspace application.

-   **Suggested Actions** tab: This tab displays relevant actions to agents based on a context of a record or recommend a value for a field. For more information on how to configure contexts so that relevant recommendations are displayed for the agents, see [Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/configure-nba.md).

</td></tr><tr><td>

**Related Lists**

</td><td>

Provides access to the interaction related lists.The CSM centered chat interaction record page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

The CSM centered chat interaction record page includes the following related lists:

-   Related Tasks
-   Recent Interactions
-   Open Cases

</td></tr><tr><td>

**Attachments**

</td><td>

The Attachments tab provides access to case-related attachments. From this tab, agents can view and download attachments.

</td></tr><tr><td>

**Templates**

</td><td>

The Templates tab provides access to available form templates which enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a new record such as an incident or change.

</td></tr><tr><td>

**Collaborate**

</td><td>

The Collaborate component enables agents to communicate with stakeholders and other users and gather information for case resolution. For more information, see [Collaborate component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-ws-collaborate-component.md).

</td></tr></tbody>
</table>## Search sources and guidance actions

The following table shows the actions that an agent can perform on the search results of various source types:

<table id="table-csm-ws-rp-chat"><thead><tr><th>

Search sources

</th><th>

Guidance actions

</th></tr></thead><tbody><tr><td>

Knowledge base article

</td><td>

-   Send an article link in chat
-   Copy an article link to the article
-   Read an article
-   Flag
-   Mark an article as helpful

</td></tr><tr><td>

Cases

</td><td>

-   Show or copy a resolution for resolved cases
-   Link or open a case

</td></tr><tr><td>

Incidents

</td><td>

-   Link an incident
-   Open an incident

</td></tr><tr><td>

Problems

</td><td>

-   Link a problem
-   Open a problem

</td></tr><tr><td>

Requests

</td><td>

-   Link a change request
-   Open a change request

</td></tr></tbody>
</table>
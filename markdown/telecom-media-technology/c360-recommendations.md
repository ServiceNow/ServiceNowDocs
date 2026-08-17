---
title: Recommendations panel
description: The Recommendations panel displays Knowledge Base article suggestions and enables you to search for Knowledge Base articles and trigger agentic workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/c360-recommendations.html
release: australia
topic_type: concept
last_updated: "2026-07-26"
reading_time_minutes: 3
breadcrumb: [Use, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Recommendations panel

The Recommendations panel displays Knowledge Base article suggestions and enables you to search for Knowledge Base articles and trigger agentic workflows.

The Recommendations panel is available in the contextual side panel on the [Telecommunications Customer 360 home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-home-page.md). It contains two tabs:

-   Suggested actions: Knowledge Base articles that are available as part of demo data.
-   Search: Enter a search term to find Knowledge Base articles and, when the ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application is installed, agentic workflows that match the term.

## Suggested actions

If demo data is installed, the Suggested actions tab displays Knowledge Base articles relevant to the current account or consumer.

When demo data is not installed, no rule mappings exist and the Suggested actions tab is empty.

To open the full content of a suggested Knowledge Base article, select **Open record** on the article.

## Search

By default, a non-AI recommended action context is installed that supports Knowledge Base article search only. When you enter a search term, the results show matching Knowledge Base articles with a **Knowledge** badge. Select **Open record** on a result to view the article.

\[Omitted image "rec-action-non-ai.png"\] Alt text: Recommendations without ServiceNow Otto for TMT installed

When the ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) is installed, AI recommended action contexts are installed and the default non-AI recommended action contexts are deactivated. When you enter a search term, the results show both Knowledge Base articles and matching agentic workflows with an option to trigger them.

**Note:**

-   You can view the agentic workflows only if you have the sn\_aia\_viewer role.
-   You can execute a workflow only if you have the sn\_nb\_action.next\_best\_action\_user role and at least one of the roles defined for the specific agentic workflow.

\[Omitted image "rec-action-ai.png"\] Alt text: Recommendations with ServiceNow Otto for TMT installed

The **Trigger Workflow** button is enabled only when all of the following conditions are true:

-   You have the now\_assist\_panel\_user role, which lets you open the Now Assist panel.
-   A record exists in the sys\_gen\_ai\_skill table for the agentic workflow. Without this record, the agentic workflow appears in the search results, but the **Trigger workflow** option is turned off.
-   You have at least one of the roles defined for the specific agentic workflow. The role list is configured on the Workflow Role Masking Configuration related list of the use case record, in an Agent Access Role Configuration with the **Limit To Roles** action.

Select **Trigger Workflow** to open the Now Assist panel and run the workflow. Your search term is passed to the workflow as the initial user prompt.

If the rule mapping for the workflow includes a context data input, that JSON string is also passed into the workflow as context memory.

For example, if you search for `suggest configuration items for change request CHG0001234` and select **Trigger Workflow**, the workflow opens in the AI Admin Hub with that full string as the initial prompt. The workflow uses the change request number directly to find relevant configuration items.

To map the context data input for a workflow, open the recommendation rule record and populate the **Context Data** guidance input with an optional JSON string. Alternatively, open the search result mapping record and populate the **Context Data** guidance input. For more information, see [Launch agentic workflow guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-launch-agentic-workflow-guidance.md).

-   **[Launch agentic workflow guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-launch-agentic-workflow-guidance.md)**  
Launch agentic workflow guidance is a configuration record that determines which agentic workflow runs when a user selects it from the Recommended Actions panel. It also defines what context data is passed to the workflow during execution.

**Parent Topic:**[Use Telecommunications Customer 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-use.md)

**Related topics**  


[ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)

[Telecommunications Customer 360 home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-home-page.md)


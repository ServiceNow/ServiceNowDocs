---
title: Default guidance for search results
description: The Default guidance for search results is a guidance that can be used for any search sources that don't have mapped guidances.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Guidances, Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Default guidance for search results

The Default guidance for search results is a guidance that can be used for any search sources that don't have mapped guidances.

Using AI search results in Recommended Actions requires a search application configuration. For each search source in that configuration, the admin creates a mapping from the search result to an action.

Starting with the Yokohama release, the Recommended Actions application automatically creates the mapping between search results and actions.

When an admin creates or updates the search application configuration for a context record, the system [automatically creates search result mapping records](ra-configuring-ai-search-automatically.md) for each of the search sources in that configuration.

-   If a search source does not have an existing mapping to an action, the system maps the search source to the default guidance.
-   If a search source has an existing mapping to a specific action, the system keeps that mapping and does not overwrite it with the default guidance.

The default guidance enables agents to view search results for any type of record. The agent can view the search results in the Recommended Actions tab in the contextual side panel in CSM Configurable Workspace. Search results are displayed in a card format.

The default guidance is available on the following pages:

-   CSM default record page
-   Front-line case page
-   CSM Interaction record page of type chat, video, email, and Walkup

## Default guidance card

The preview card for the default guidance displays information about the search result.

![Preview card for the default guidance displays information about the search result, including a title, fields that are relevant to the record type, "Open record" action and Dismiss action.](../image/ra-ai-search-preview-card.png)

The preview card for the default guidance includes the following elements.

<table id="table_f2f_xmq_12c"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search icon

</td><td>

The search icon appears at the top of the card along with the hint text. The icon is made up of a magnifying glass with a sparkle. This icon makes it easy for customers to identify search results from suggested actions.![Default guidance preview card magnifying glass icon and hint text](../image/ra-ai-search-magnify-glass-icon.png)

</td></tr><tr><td>

Hint text

</td><td>

Text that provides context for the guidance. The icon and hint text appear together at the top of the card above the title.

</td></tr><tr><td>

Title

</td><td>

The title appears at the top of the card.

</td></tr><tr><td>

Relevancy score

</td><td>

The relevancy score displays on the Share KB in chat interactions guidance in the Search tab of the Recommended Actions contextual side panel. It indicates how well a search result matches the agent’s query.

</td></tr><tr><td>

Record fields

</td><td>

Relevant fields related to the guidance content are displayed on the card. These fields provide key information about the guidance content.For example, a preview card for a knowledge article includes fields for the article number and author while the preview card for a case includes fields for the case number, state, and priority.

</td></tr><tr><td>

Dismiss

</td><td>

Agents can use this action to move the guidance from the Suggested actions tab to the Actions history tab. After selecting **Dismiss**, the agent receives a notification that the guidance has been moved.To view the Actions history tab, click the clock icon in the upper right corner of the Recommendations panel.

</td></tr><tr><td>

Open record

</td><td>

Agents can use this action to open the associated record in a sub tab. Agents can view the record details in the sub tab without navigating away from the main window.

</td></tr></tbody>
</table>**Related topics**  


[Automatically map AI search results with guidance inputs in Recommended Actions](ra-configuring-ai-search-automatically.md)


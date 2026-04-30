---
title: Contexts in Recommended Actions for Customer Service
description: A context enables agents to see recommendations for records from a table when certain rules are met. These recommendations can help agents by suggesting actions to take based on the record context.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Recommended Actions for Customer Service, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Contexts in Recommended Actions for Customer Service

A context enables agents to see recommendations for records from a table when certain rules are met. These recommendations can help agents by suggesting actions to take based on the record context.

The Recommended Actions for Customer Service application provides context records for the Case and Interaction tables.

## Case Context record

The Recommended Actions for Customer Service application provides the Case Context record for the Case table.

Context records include [rules](ra-csm-rules.md) and [recommendations](ra-csm-recommendations.md). The Case Context record also includes search result mapping records for the search source tables. The following tables are mapped to specific guidance actions:

-   Knowledge
-   Case
-   Incident
-   Problem
-   Change Request

The remaining tables are mapped to the [Default guidance for search results](ra-csm-guidances-default-guidance-search.md) guidance action.

## Interaction Context record

The Recommended Actions for Customer Service application includes a context record and search mapping record that automatically displays search results from the Knowledge table for chat interaction records.

The Interaction Context record enables search based on the short description of the interaction record and displays relevant articles. The search mapping record maps knowledge results to the **Share KB in chat interactions** guidance. During chat interactions, the system accurately displays knowledge results in the Search tab in the contextual side panel.

The Recommended Actions for Customer Service application also includes a search mapping record that maps all search source tables, with the exception of the Knowledge table, to the [Default guidance for search results](ra-csm-guidances-default-guidance-search.md) guidance action. During chat interactions, the system accurately displays results for the search source tables in the Search tab.

Follow these steps to enable recommendations in the contextual side panel for chat interactions:

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts** &gt; **CSM Interaction context**.
2.  Enable the **Active** check box.
3.  Select **Update**.

## Fix script

The Recommended Actions for Customer Service application includes a fix script that checks for existing context records associated with the same table as the Interaction Context record.

-   If one or more records for the same table are found, the Interaction Context record is deactivated.
-   If no existing context records for the same table are found, the Interaction Context record remains active.

This avoids duplicate or conflicting context records.

## Activating or deactivating context records

When activating or deactivating context records, the system displays alert messages so that contexts can be managed effectively without causing conflicts.

If multiple contexts are activated for the same table, the system alerts the admin to specify the correct **contextSysID** property in the Recommended Actions component on record pages for the referenced table.

If an admin activates multiple contexts for the same table, the system displays a message advising the admin to specify the correct **contextSysID** property on the Recommended Actions component for all record pages that reference this table.

The message includes information about how to configure the **contextSysID** property on the Recommended Actions component and what happens if the correct context is not specified.

The system logs all context activation and deactivation events along with the displayed alerts.


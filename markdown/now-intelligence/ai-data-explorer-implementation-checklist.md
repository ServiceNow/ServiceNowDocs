---
title: AI Data Explorer implementation checklist
description: Complete these steps to enable AI Data Explorer and verify that the semantic layer is configured correctly for your organization.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 1
keywords: [AI Data Explorer, implementation, semantic layer, query generation]
breadcrumb: [Configure, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# AI Data Explorer implementation checklist

Complete these steps to enable AI Data Explorer and verify that the semantic layer is configured correctly for your organization.

Use this checklist to verify that AI Data Explorer is properly configured and ready for use in your organization.

## Prerequisites and configuration

-   Verify that required AI skills are activated.
-   Enable Record Level Analysis in the Analytics Exploration skill to get better insights.
-   Check the base health of Query Generation using the Health page.
-   Confirm that AI Search is active.
-   Verify that the Semantic Layer is built. Entities and dimensions should not be 0.

## Testing and validation

1.  Navigate to **AI Data Explorer** from the main menu.
2.  Try a simple question such as "Open incidents" to verify end-to-end functionality.
3.  Verify that tables you want to use are added to the semantic layer. Task extended tables and some base tables are added by default, but custom tables that are not task-based might need to be added manually.
4.  To check if a table is already in the semantic layer, navigate to **Query generation** &gt; **Entities**. If the table is in the list and marked as active, it is already configured.

## User access

Grant users who need access to AI Data Explorer the **now-assist-explorer-user** role.

## General usage guidelines

-   Use short, simple questions for best results.
-   Only simple analytical questions are supported. Questions should be answerable with a single chart or single data source.
-   AI Data Explorer cannot answer general definition questions or questions requiring comparison across multiple data sources. Break down complex analysis into multiple questions.
-   When asking follow-up questions, use words like "these" to ensure filters are not dropped. For example, "Of these incidents, how many are critical?"

**Parent Topic:**[Configure AI Data Explorer](../../par-for-workspace/task/configure-now-ass-explorer.md)


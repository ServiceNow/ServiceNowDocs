---
title: Enable AI Search for Next Experience
description: Walk through a Guided Setup task to configure AI Search as the search engine for global and workspace searches from the Unified Navigation search field.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring AI Search for Next Experience, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Enable AI Search for Next Experience

Walk through a Guided Setup task to configure AI Search as the search engine for global and workspace searches from the Unified Navigation search field.

## Before you begin

The AI Search for Next Experience ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install AI Search for Next Experience](install-ais-next-experience-app.md).

You must have already completed the **Convert Zing search applications** Guided Setup task. For details on completing this task, see [Migrate Zing search application configurations to AI Search](migrate-srch-apps-ais-next-exp.md).

Role required: ais\_admin

## About this task

The **Activate AI Search for all Next Experience search applications** Guided Setup task walks you through enabling the AI Search for Next Experience application.

Once you enable the application, Next Experience search applications use AI Search instead of Zing. Each search application uses the specific settings defined in its search application configuration.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search for Next Experience** &gt; **Guided Setup for Zing to AI Search Migration**.

2.  In the **Complete migration to AI Search** category, select **Get Started**.

3.  In the **Activate AI Search for all Next Experience search applications** task, select **Configure**.

    A modal window reports whether AI Search for Next Experience is enabled on your instance.

4.  If the system reports **AI Search for Next Experience is disabled**, select **Enable AI Search for Next Experience**.

    **Note:** If AI Search for Next Experience is already enabled, ensure that all migrated search application configurations are activated by disabling the application and then re-enabling it.

5.  When the system reports **AI Search for Next Experience is enabled**, select **Close**, then select **Mark as Complete** for the **Activate AI Search for all Next Experience search applications** task.


## Result

The system uses AI Search as the search engine for global search and Next Experience workspace application searches issued from the Unified Navigation search field.

## What to do next

Notify all users of your instance about the following details.

-   Users need to log out and back in before they can use AI Search for Next Experience.
-   Once you enable AI Search for Next Experience, only workspace applications that use AI Search as their search engine appear in the Unified Navigation search context menu. To search from workspace applications that use the Zing text indexing and search engine, you must navigate to the workspace instead of using the Unified Navigation search context menu.

**Parent Topic:**[Configuring AI Search for Next Experience](../concept/configuring-ais-next-experience.md)


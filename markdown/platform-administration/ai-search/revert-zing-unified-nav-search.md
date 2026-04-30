---
title: Revert to Zing as the Unified Navigation search engine
description: Revert to using Zing text indexing and search engine for the Unified Navigation search field in Next Experience.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2024-07-29"
reading_time_minutes: 1
breadcrumb: [Configuring AI Search for Next Experience, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Revert to Zing as the Unified Navigation search engine

Revert to using Zing text indexing and search engine for the Unified Navigation search field in Next Experience.

## Before you begin

The AI Search for Next Experience ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install AI Search for Next Experience](install-ais-next-experience-app.md).

Role required: ais\_admin

## About this task

You can undo the configuration changes you made to enable AI Search for Next Experience. This may be for either of the following reasons:

-   You prefer to use Zing text indexing and search engine for Unified Navigation in Next Experience.
-   You plan to disable Next Experience and revert to the legacy UI. \(The legacy UI only supports the Zing engine for global search and workspace search.\)

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search for Next Experience** &gt; **Guided Setup for Zing to AI Search Migration**.

2.  In the **Complete migration to AI Search** category, select **Edit**.

3.  In the **Activate AI Search for all Next Experience search applications** task, select **Configure**.

    A modal window reports the enablement status of AI Search for Next Experience on your instance.

4.  If the system reports **AI Search for Next Experience is enabled**, select **Disable AI Search for Next Experience**.

5.  When the system reports **AI Search for Next Experience is disabled**, select **Close**, then select **Mark as Incomplete** for the **Activate AI Search for all Next Experience search applications** task.


## Result

The system reverts to using Zing as the search engine for global search and Next Experience workspace application searches issued from the Unified Navigation search field.

## What to do next

Notify all users of your instance that they need to log out and back in before they can use Zing search in the Unified Navigation search field.

**Parent Topic:**[Configuring AI Search for Next Experience](../concept/configuring-ais-next-experience.md)


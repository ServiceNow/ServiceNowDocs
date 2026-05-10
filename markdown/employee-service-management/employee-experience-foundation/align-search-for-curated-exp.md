---
title: AI Search for Curated Experiences
description: Align the AI search to limit the search to the content associated with your taxonomy.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup search experience, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# AI Search for Curated Experiences

Align the AI search to limit the search to the content associated with your taxonomy.

## Before you begin

Role required: admin

Deactivate the existing taxonomy so that the search configurations pick up the content from your taxonomy.

## About this task

For new customers, the AI search is enabled by default.

**Note:** AI Search returns additional results based on user roles:

-   Users with either the system admin or content admin role can see unpublished content.
-   For users with content approver roles, search results might include content for which they are not the audience. However, they cannot view the content unless they are part of the configured audience.
-   For users with content admin or content manager roles, search results shouldn't include content \(such as news, company events or rich content\) in AI search results if they don't meet the scheduled availability window, or for which they are not the configured audience.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Sources**.

2.  Click **ESC Portal Catalogs**.

3.  In the **Conditions** field, set the **Taxonomy topic . Taxonomy** filter condition to point to your taxonomy to enable the search to focus on the content associated with your taxonomy.

4.  You can modify the other default filter conditions or leave them as-is.

5.  Click **Update** to return to the AI search source list.

6.  Click **ESC Portal Knowledge Bases**.

7.  In the **Conditions** field, set the **Taxonomy topic. Taxonomy** filter condition to point to your taxonomy to enable the search to focus on the content associated with your taxonomy.

8.  You can modify the other default filter conditions or leave them as-is.

9.  Click **Update**.



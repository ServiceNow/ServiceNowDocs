---
title: Block search results and Genius Results using a result improvement rule
description: Configure a result improvement rule to prevent specific documents from appearing as Genius Results or search results.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Result improvement rules, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Block search results and Genius Results using a result improvement rule

Configure a result improvement rule to prevent specific documents from appearing as Genius Results or search results.

## Before you begin

Create your result improvement rule first to define your trigger conditions. For steps to create a result improvement rule, see [Create a result improvement rule](create-result-improve-rule-ais.md).

Role required: ais\_admin

## About this task

Block actions hide selected search results from the result set. When a result improvement rule with a block action activates, its effect depends on the result improvement rule's **Apply only to Genius Results** option setting:

-   If this option is selected, the block action prevents selected documents from appearing as Genius Result answers. Selected documents can still appear as search results.
-   If this option is cleared, the block action prevents the selected documents from appearing as Genius Result answers or search results.

## Procedure

1.  In the Actions related list, select **Block Documents**.

2.  In the Select Documents To Block dialog box, search for results that you want to block.

3.  To add a search result to the selected results pane, select the plus sign next to it.

4.  After selecting all the results that you want to block, select **Add Documents and Close**.

5.  Edit the **Order** values for the result improvement rule's block actions.


## What to do next

To make new or updated result improvement rule settings take effect, publish the search profile that you edited. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Result improvement rules](../concept/result-improvement-rules-ais.md)


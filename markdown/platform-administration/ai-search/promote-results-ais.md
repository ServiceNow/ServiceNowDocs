---
title: Promote search results using a result improvement rule
description: Configure a result improvement rule to make specific records appear first in results for a search.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Result improvement rules, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Promote search results using a result improvement rule

Configure a result improvement rule to make specific records appear first in results for a search.

## Before you begin

Create your result improvement rule first to define your trigger conditions. For steps to create a result improvement rule, see [Create a result improvement rule](create-result-improve-rule-ais.md).

Role required: ais\_admin

## About this task

Promote actions define search results to spotlight in the result set. When a result improvement rule with a promote action activates, it displays search results specified in the action ahead of other results for the search query.

**Note:** Promote actions can spotlight results that wouldn't otherwise match your search. Spotlighted results are added to the search results set if they're not already present in it.

## Procedure

1.  In the Actions related list, select **Promote Documents**.

2.  In the Select Documents To Promote dialog box, search for the results that you want to promote.

3.  To add a search result to the selected results pane, select the plus sign next to it.

4.  After selecting all the results that you want to promote, select **Add Documents and Close**.

5.  Edit the **Order** values for the result improvement rule's promote actions.

    The **Order** field only accepts integer values. AI Search evaluates promote actions with lower **Order** values before promote actions with higher values. As an example, a promote action with **Order** 150 is evaluated before one with **Order** 200.


## What to do next

To make new or updated result improvement rule settings take effect, publish the search profile that you edited. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Result improvement rules](../concept/result-improvement-rules-ais.md)


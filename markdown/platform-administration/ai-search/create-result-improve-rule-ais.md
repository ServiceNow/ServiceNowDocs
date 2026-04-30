---
title: Create a result improvement rule
description: Create a rule to boost, block, or promote search results or to block Genius Results. Specify the conditions that activate your rule and choose the action it performs when activated.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Result improvement rules, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a result improvement rule

Create a rule to boost, block, or promote search results or to block Genius Results. Specify the conditions that activate your rule and choose the action it performs when activated.

## Before you begin

Role required: ais\_admin

## About this task

You can configure activation conditions and triggers for a result improvement rule. Additional topics cover steps for configuring boost, block, or promote actions for your rule.

**Note:** Each result improvement rule can only perform actions of a single type when activated. You can define multiple actions of the same type for a rule.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to add the result improvement rule to.

3.  In the Result Improvement Rules related list, select **Create**.

4.  On the AI Search Results Improvement Rule form, fill in the fields.

    For a description of the field values, see [AI Search Results Improvement Rule form](../reference/result-improvement-rule-form-ais.md).

5.  Select **Submit**.

    The Actions related list appears.

6.  Choose the action that you want the result improvement rule to perform when activated, and see the appropriate topic for configuration steps:

    -   To increase the relevancy scores of search result records that include specific field values, see [Boost search results using a result improvement rule](boost-results-ais.md#).
    -   To prevent specific records from appearing in the search results, see [Block search results and Genius Results using a result improvement rule](block-results-ais.md).
    -   To make specific records appear first in the search results, see [Promote search results using a result improvement rule](promote-results-ais.md).

## What to do next

To make new or updated result improvement rule settings take effect, publish the search profile that you edited. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Result improvement rules](../concept/result-improvement-rules-ais.md)


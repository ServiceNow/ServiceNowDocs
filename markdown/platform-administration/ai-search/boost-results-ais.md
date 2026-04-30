---
title: Boost search results using a result improvement rule
description: Increase the relevancy scores for search results that satisfy a custom set of conditions.This list describes the types of search result relevancy boost that you can apply using a result improvement rule.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Result improvement rules, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Boost search results using a result improvement rule

Increase the relevancy scores for search results that satisfy a custom set of conditions.

## Before you begin

Create your result improvement rule first to define your trigger conditions. For steps to create a result improvement rule, see [Create a result improvement rule](create-result-improve-rule-ais.md).

Role required: ais\_admin

## About this task

Boost actions define relevancy changes applied by result improvement rules. When a result improvement rule with a boost action activates, AI Search modifies the relevancy scores for search results from an indexed source specified in the action. You can choose one of these boost types:

-   Boost all search results from the specified indexed source.
-   Boost only search results from the specified indexed source with a field value that matches a dynamically populated field value from the searcher's user context.
-   Boost only search results from the specified indexed source with a field value that matches a static string value specified in the action.
-   Boost only search results from the specified indexed source with a field value that matches a synonym defined in a synonym dictionary.

You can specify a boost weight for each boost action. This is an integer value that AI Search uses to alter the relevancy scores for search results affected by your boost action. Boost weights can be positive or negative.

Positive boost weights increase the relevancy scores for boosted search results. Each boost weight of 1 increases a boosted search result's relevancy score by 0.1% of its original value. For example, if you set a boost weight of 100, you increase each boosted search result's relevancy by +10%, so a search result with an original relevancy score of 60 gets a final relevancy score of 66. Setting a boost weight of 1000 adds +100%, doubling the relevancy scores for boosted search results.

Negative boost weights reduce the relevancy scores for boosted search results. Each boost weight of –1 reduces a boosted result's relevancy score by 0.1% of its original value. As an example, if you set a boost weight of –150, you reduce a boosted search result's relevancy by 15%, so a search result with an original relevancy score of 100 gets a final relevancy score of 85. Any boost weight of –1000 or lower reduces a boosted search result's relevancy score to 0, causing it to appear at the end of the search result list.

When a single search result is affected by multiple boost actions, AI Search adds the individual boost weights together to determine the total relevancy score modifier. For example, a search result boosted by three rules with boost weights 100, 150, and –25 has a total boost weight of 225, increasing its final relevancy score by 22.5% of its original value.

**Note:** Boost actions don't change the set of results returned for your search, so you can't boost a record that doesn't match your search. If you want to add a search result into your results whether or not it matches your search, try using a promote action instead. For details on this action, see [Promote search results using a result improvement rule](promote-results-ais.md).

## Procedure

1.  In the Actions related list, select **Create Boost Action**.

2.  On [the Rule - Action Mapping form](../reference/rule-action-map-form-ais.md), set the boost weight and fill in the other fields.

3.  Select **Submit**.

4.  Edit the **Order** values for the result improvement rule's boost actions.


## What to do next

To make new or updated result improvement rule settings take effect, publish the search profile you edited. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Result improvement rules](../concept/result-improvement-rules-ais.md)

## List of result improvement rule boost types

This list describes the types of search result relevancy boost that you can apply using a result improvement rule.

<table id="table_xyy_3h2_2nb"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boost All Documents In Indexed Source

</td><td>

Applies relevancy boost to every search result from the selected indexed source. As an example, you might boost all results from the Knowledge Table indexed source.

</td></tr><tr><td>

Boost By User Context \(dynamic\)

</td><td>

Applies relevancy boost to search results from the selected indexed source if they include a value for the selected field that matches a field value specified in the dynamically populated user context. As an example, you might boost all results from the Knowledge Table indexed source with Short description field values that contain matches for the city specified in the current search user's location, as set in their user context. This configuration could end up boosting different records when you search from Paris than when you search from New York City.

**Note:** Starting in the Xanadu release, AI Search expands user context field values using published, active synonyms defined in dictionaries linked to the current search profile. As an example, if the user context location is `Paris` and you define a synonym that defines `Paris` and `France` as equivalent, your result improvement rule boosts documents containing `France` as well as those containing `Paris`. For more details on synonym expansion, see [Synonyms](../concept/synonyms-ais.md).

</td></tr><tr><td>

Boost By Field Match \(static\)

</td><td>

Applies relevancy boost to search results from the selected indexed source if they include a value for the selected field that matches a specified static value. As an example, you might boost all results from the Knowledge Table indexed source that have Short description field values matching the static value `Dealing with Spyware and Viruses`.

</td></tr><tr><td>

Boost By Synonym Dictionary

</td><td>

Applies relevancy boost to search results from the selected indexed source if they include a value for the selected field that matches any synonym defined in a selected synonym dictionary. As an example, you might create a custom synonym dictionary named Boost Synonyms. You could then configure a result improvement rule to boost all results from the Knowledge Table indexed source which have Short description field values containing matches for synonyms in that dictionary. If the dictionary includes a synonym that defines `laptop` and `computer` as equivalent, this result improvement rule boosts knowledge article search results with short descriptions that include `laptop` or `computer` \(or both\).

 The selected synonym dictionary must be published, active, and linked to the current search profile. AI Search only checks for matches against published and active synonyms in the dictionary.

 For more details on synonyms and synonym dictionaries, see [Synonyms](../concept/synonyms-ais.md).

</td></tr></tbody>
</table>
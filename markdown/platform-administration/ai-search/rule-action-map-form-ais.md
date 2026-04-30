---
title: Rule - Action Mapping form
description: The Rule - Action Mapping form contains information about relationships between AI Search result improvement rules and boost actions. Use this form when linking boost actions to result improvement rules.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Rule - Action Mapping form

The Rule - Action Mapping form contains information about relationships between AI Search result improvement rules and boost actions. Use this form when linking boost actions to result improvement rules.

For information on configuring boost actions in result improvement rules, see [Boost search results using a result improvement rule](../task/boost-results-ais.md#).

<table id="table_ksn_hqd_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label for the boost action.

</td></tr><tr><td>

Type

</td><td>

Action type. This field is automatically set to **Boost Action**.

</td></tr><tr><td>

Application

</td><td>

Application scope for the boost action. This field is automatically set to the name of the current application.

</td></tr><tr><td>

Order

</td><td>

Order of evaluation for the boost action in the context of the result improvement rule.

</td></tr><tr><td class="sub-head" colspan="2">

Boost Action

</td></tr><tr><td>

Boost Type

</td><td>

Type of boost the action applies to search results from the selected indexed source. Supported types include:

-   **Boost All Documents In Indexed Source**: Applies relevancy boost to every search result from the indexed source.
-   **Boost By User Context \(dynamic\)**: Applies relevancy boost to search results from the indexed source if they include a value for the selected field that matches a field value specified in the dynamically populated user context.
-   **Boost By Field Match \(static\)**: Applies relevancy boost to search results from the indexed source if they include a value for the selected field that matches a specified static value.
-   **Boost By Synonym Dictionary**: Applies relevancy boost to search results from the indexed source if they include a value for the selected field that matches any synonym defined in a synonym dictionary.

</td></tr><tr><td>

Indexed Source

</td><td>

Reference to an indexed source. The boost action only applies to search results for records from this indexed source.

</td></tr><tr><td>

Boost Weight

</td><td>

Integer value that AI Search uses to alter the relevancy scores for search results affected by the boost action. Boost weights can be positive or negative.Positive boost weights increase the relevancy scores for boosted search results. Each boost weight of 1 increases a boosted search result's relevancy score by 0.1% of its original value. For example, if you set a boost weight of 100, you increase each boosted search result's relevancy by +10%, so a search result with an original relevancy score of 60 gets a final relevancy score of 66. Setting a boost weight of 1000 adds +100%, doubling the relevancy scores for boosted search results.

 Negative boost weights reduce the relevancy scores for boosted search results. Each boost weight of –1 reduces a boosted result's relevancy score by 0.1% of its original value. As an example, if you set a boost weight of –150, you reduce a boosted search result's relevancy by 15%, so a search result with an original relevancy score of 100 gets a final relevancy score of 85. Any boost weight of –1000 or lower reduces a boosted search result's relevancy score to 0, causing it to appear at the end of the search result list.

 When a single search result is affected by multiple boost actions, AI Search adds the individual boost weights together to determine the total relevancy score modifier. For example, a search result boosted by three rules with boost weights 100, 150, and –25 has a total boost weight of 225, increasing its final relevancy score by 22.5% of its original value.

</td></tr><tr><td>

When

</td><td>

Name of a field from the selected indexed source. This field appears only when you select **Boost By User Context \(dynamic\)**, **Boost By Field Match \(static\)**, or **Boost By Synonym Dictionary** as the boost type.

</td></tr><tr><td>

Matches the Searcher's

</td><td>

Dynamically populated user context element to compare with a search result's value for the field selected in the **When** field. This field appears only when you select **Boost By User Context \(dynamic\)** as the boost type. The choice list displays the source table and field for each user context element. As an example, the **Language** user context element is populated using the User \[sys\_user\] table's **language** field value for the search user.

</td></tr><tr><td>

Contains

</td><td>

Static value to compare with a search result's value for the field selected in the **When** field. This field appears only when you select **Boost By Field Match \(static\)** as the boost type.

</td></tr><tr><td>

Matches A Synonym Dictionary

</td><td>

Synonym dictionary to check for synonyms that match a search result's value for the field selected in the **When** field. This field appears only when you select **Boost By Synonym Dictionary** as the boost type.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)


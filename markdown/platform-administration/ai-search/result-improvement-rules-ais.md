---
title: Result improvement rules
description: Define rules with configurable trigger conditions to boost, block, or promote search results for specific searches. You can also boost search results for documents matching elements of the user context, such as a user's country, OS, or device type.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Result improvement rules

Define rules with configurable trigger conditions to boost, block, or promote search results for specific searches. You can also boost search results for documents matching elements of the user context, such as a user's country, OS, or device type.

Result improvement rules with boost actions override the default search result order produced by the AI Search machine learning relevancy feature. Rules with block or promote actions override the default result set for a search query.

## Rule structure

A result improvement rule consists of these parts:

-   A set of conditions that determine when the rule activates.
-   A set of boost, block, or promote actions that determine how the rule modifies the search query's results when activated. The rule can only include actions of a single type, but can include multiple actions of that type.

Rule conditions include the following:

-   A date range bounded by start and end dates. The rule can only activate during the specified date range.
-   A language. The rule can only activate if this language matches the search query's language.
-   Optionally, a set of one or more trigger conditions. Triggers can operate on individual search query keywords, the full search query, or elements of the search user's context such as their department, language, or browser version. The rule can only activate if all of its trigger conditions are met.

Rule actions include the following types:

-   **Boost**: Increase the relevancy scores for search results from an indexed source that satisfy your specified conditions. You can select any of the following options:
    -   Boost relevancy for all search results from the indexed source.
    -   Boost relevancy for search results from the indexed source that include field values matching a dynamically populated value from the user context.
    -   Boost relevancy for search results from the indexed source that include field values matching a static string value that you specify.
    -   Boost relevancy for search results from the indexed source that include field values matching synonyms from one of your synonym dictionaries.
-   **Block**: Exclude specific results from the search query's results list.
-   **Promote**: Display specific results at the start of the search query's results list.

Each result improvement rule can only perform actions of a single type when activated. You can define multiple actions of the same type for a rule.

Block actions take precedence over other actions. For example, if two result improvement rules block and promote the same search result, AI Search excludes the search result from the search query's results list.

## Language dependence

Result improvement rule activation is language-dependent. You specify a language for each result improvement rule.

AI Search supports result improvement rules for all languages activated in your instance. For the list of languages you can activate, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

## Interaction with other search features

The following table describes interactions between result improvement rules with Query triggers and other search features.

|Feature|Interaction with result improvement rules|
|-------|-----------------------------------------|
|[Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)|A search query term added by lemma or Unicode normalization can trigger a result improvement rule if it matches the rule's Query trigger.|
|[Stop words](stop-words-ais.md)|If a search query term that matches a result improvement rule's Query trigger is defined as a stop word, AI Search evaluates the rule trigger before removing the stop word from the search query.|
|[Synonyms](synonyms-ais.md)|By default, a synonym expansion term can activate a result improvement rule if it matches the rule's Query trigger. You can prevent synonym expansion terms from activating a rule with a Query trigger by clearing the **Expand Synonyms For Query Conditions** option that appears when you define the Query trigger.|
|[Typo handling](typo-handling-ais.md)|An auto-corrected search query term can trigger a result improvement rule if it matches the rule's Query trigger.|

-   **[Create a result improvement rule](../task/create-result-improve-rule-ais.md)**  
Create a rule to boost, block, or promote search results or to block Genius Results. Specify the conditions that activate your rule and choose the action it performs when activated.
-   **[Boost search results using a result improvement rule](../task/boost-results-ais.md#)**  
Increase the relevancy scores for search results that satisfy a custom set of conditions.
-   **[Block search results and Genius Results using a result improvement rule](../task/block-results-ais.md)**  
Configure a result improvement rule to prevent specific documents from appearing as Genius Results or search results.
-   **[Promote search results using a result improvement rule](../task/promote-results-ais.md)**  
Configure a result improvement rule to make specific records appear first in results for a search.
-   **[Share result improvement rules between search profiles](../task/mirror-result-improvement-rules.md)**  
Make your search experiences more consistent by configuring a search profile to mirror result improvement rules from other search profiles.

**Parent Topic:**[Search profiles in AI Search](defining-search-profiles-ais.md)


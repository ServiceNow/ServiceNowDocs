---
title: Genius Results
description: Optionally display the best answers for a search query as actionable Genius Result cards included with search results.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-12-18"
reading_time_minutes: 6
breadcrumb: [Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Genius Results

Optionally display the best answers for a search query as actionable Genius Result cards included with search results.

A Genius Result configuration includes a trigger condition and logic for creating answers. The trigger condition determines whether the Genius Result configuration activates for a search query. When activated, the configuration checks for search results with extremely high relevancy. If it finds any, its answer logic populates one or more Genius Result cards with information and actions derived from these results. The Genius Result cards appear alongside normal search results, giving the user immediate access to the most relevant answers and actions.

To use a Genius Result configuration in searches, link it to one or more of your search profiles. For details on this procedure, see [Link a Genius Result configuration to a search profile](../task/link-gr-search-profile-ais.md).

## Genius Result evaluation order and result limit

AI Search evaluates active Genius Result configurations for a search profile in an order determined by their numeric **Order** field values, as defined in the search profile's Genius Results related list. Genius Result configurations with lower **Order** field values are evaluated before those with higher field values. As an example, a Genius Result configuration with **Order** 100 is evaluated before one with **Order** 200. To learn how to change the evaluation order, see [Set the evaluation order for Genius Result configurations in a search profile](../task/set-gr-eval-order-srch-profile-ais.md).

**Note:** **Order** field values for linked Genius Result configurations are set separately for each search profile. A Genius Result configuration that's linked to multiple search profiles can have a different **Order** field value in each profile. For instance, you might set an **Order** value of 100 for the Q&amp;A Genius Result configuration in one search profile but set a value of 750 for the same Genius Result configuration in a second search profile that it's linked to.

A search application configuration's **Genius Results Limit** field value specifies the maximum number of Genius Result cards the application can display. For more details on search application configuration settings, see [Search Application Configuration form](../reference/search-app-config-form-ais.md).

## Genius Result trigger conditions

You can select any one of the following trigger conditions for a Genius Result configuration:

-   **Always**: The Genius Result configuration activates for all search queries.
-   **NLU**: The Genius Result configuration activates when the search query's detected intent matches a specified Natural Language Understanding \(NLU\) model intent. For more information on NLU models and intents, see [Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **Term**: The Genius Result configuration activates when the search query consists of a single specified term or phrase.

**Note:** A Genius Result configuration can trigger and still not return answers. Genius Result answers only display when AI Search has extremely high confidence that there’s a correct response for the search query. You should typically expect to see Genius Result answers for a small percentage of search queries.

## Genius Result answer types

A Genius Result configuration can include either of the following answer types:

-   **Search**: When triggered, displays Genius Result cards for results from a search query. The search query must be defined in a server-side script included in the Genius Result configuration. Each search result displays as a separate Genius Result card, to a maximum of three cards. If the search query returns no results, no Genius Result card is displayed.
-   **Script**: When triggered, displays a Genius Result card containing key-value pairs. The object containing these key-value pairs must be defined in a server-side script included in the Genius Result configuration. The script can use methods from any ServiceNow AI Platform® public API to construct this object.

## Language support

In the base system, Genius Results only support English search queries.

## Table record limit for Genius Result configurations with NLU trigger conditions

If an NLU model includes a table vocabulary source that references a table containing more than 100,000 records, sync fails for the vocabulary source. When sync fails, the model can't be successfully trained, and Genius Result configurations that use the model in their NLU trigger conditions don't operate correctly.

**Warning:** Don't activate the People Genius Result configuration if your instance has more than 100,000 records in any of the following tables:

-   Catalog Item \[sc\_cat\_item\]
-   Department \[cmn\_department\]
-   Location \[cmn\_location\]
-   User \[sys\_user\]

These tables are configured as vocabulary sources in the Default AI Search Genius Results Model specified in the People configuration's NLU trigger condition. If your instance has more than 100,000 records in any of the listed tables, training will fail for the NLU model and the People Genius Result configuration won't operate correctly.

For more information on NLU vocabulary sources, see [NLU vocabulary](https://www.servicenow.com/docs/access?context=using-nlu-vocabulary&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Genius Result review feedback

You can review individual Genius Result answers and provide feedback about their accuracy. To provide review feedback on a Genius Result answer, select one of the thumb icons shown on the answer card:

-   If the answer answers your question accurately, select the thumbs up icon ![](../image/genius-result-feedback-positive.png).
-   If the answer answers your question inaccurately, select the thumbs down icon ![](../image/genius-result-feedback-negative.png).

Your feedback helps ServiceNow improve future versions of Genius Result configurations.

## Interaction with other search features

The following table describes interactions between Genius Results and other search features.

|Feature|Interaction with Genius Results|
|-------|-------------------------------|
|[Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)|Search query terms added by lemma or Unicode normalization can't trigger Genius Result configurations with Term trigger conditions.|
|[Stop words](stop-words-ais.md)|If a search query term that matches a Genius Result configuration's Term trigger is defined as a stop word, AI Search evaluates the trigger before removing that stop word from the search query.|
|[Synonyms](synonyms-ais.md)|Synonym expansion terms can't trigger Genius Result configurations with Term trigger conditions.|
|[Typo handling](typo-handling-ais.md)|Auto-corrected search query terms can't trigger Genius Result configurations with Term trigger conditions.|

-   **[Genius Result configurations in the base system](default-genius-result-configs-ais.md)**  
Preconfigured AI Search Genius Result configurations display concise, actionable answers derived from high-relevancy search results. These configurations return Genius Result answers for Catalog Items, tables, users, and Knowledge articles that match your search.
-   **[Link a Genius Result configuration to a search profile](../task/link-gr-search-profile-ais.md)**  
Link a Genius Result configuration to one or more search profiles.
-   **[Set the evaluation order for Genius Result configurations in a search profile](../task/set-gr-eval-order-srch-profile-ais.md)**  
Change the order in which AI Search evaluates Genius Result configurations linked to a search profile.
-   **[Create a Genius Result configuration](../task/create-genius-results-config-ais.md)**  
Create a Genius Result configuration, set its trigger condition, and configure the results displayed on its answer card.
-   **[Link an NLU model and intents to a Genius Result configuration](../task/link-nlu-model-genius-result-ais.md)**  
Specify the NLU model and intents to use for a Genius Result configuration with an NLU trigger condition.

**Parent Topic:**[Search profiles in AI Search](defining-search-profiles-ais.md)


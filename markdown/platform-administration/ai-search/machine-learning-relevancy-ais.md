---
title: Machine learning relevancy in AI Search
description: AI Search displays the most relevant search results for a query first. Machine learning automatically tunes search result relevancy scoring for search experiences based on aggregated user interactions.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-01-20"
reading_time_minutes: 3
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Machine learning relevancy in AI Search

AI Search displays the most relevant search results for a query first. Machine learning automatically tunes search result relevancy scoring for search experiences based on aggregated user interactions.

Machine learning relevancy is automatically enabled and isn't configurable.

## Relevancy models and scoring

AI Search uses a relevancy model to compute a relevancy score for each result returned by a search. Documents with higher relevancy scores appear first in the result set. A result's relevancy score is specific to the particular document, search terms, and user associated with the query.

Each search profile includes its own relevancy model. You can't view, modify, or delete this relevancy model.

**Note:** AI Search doesn't apply relevancy ranking to `***` universal wildcard queries. Results from `***` queries appear in an unspecified order.

## Search signals and machine learning relevancy tuning

AI Search UX components record signals associated with user searches. These search signals include data on how search users interact with the search input field, auto-complete suggestions, facet and navigation tab filters, Genius Result answer cards, and search results. To learn more about how search signals are recorded and stored, see [Search signals](../../search-administration/concept/search-signals.md).

Machine learning relevancy uses data from these search signals to intelligently tune relevancy models on a continual basis. Every 30 days, AI Search computes a new version of each relevancy model, iteratively modifying its parameters and regression testing it against aggregated search signal data for the search profile. When this tuning process is complete, AI Search compares the existing and new relevancy models to see which one produces better matches for user search behavior as recorded in the historical signal data.

If the new relevancy model produces better results with the signal data, AI Search uses its modified parameter values to perform A/B testing evaluations of live search traffic for the search profile. These evaluations test individual parameter changes to verify that they produce better search relevancy.

**Note:** For details on the search query parameter evaluation framework used to perform A/B testing evaluations, see [Search query parameter evaluation framework](srch-qry-parm-eval-fw-ais.md#).

If the new model outperforms the original model in both the historical search-match comparison and the A/B testing, AI Search sets it as the active relevancy model for the search profile, overwriting the existing relevancy model. The updated relevancy model remains in use until the next tuning cycle begins.

These relevancy model tuning processes occur separately for each search profile. Changes made to the relevancy model in one search profile don't affect relevancy models in other search profiles.

**Note:** When you upgrade to Xanadu from a previous release, the default relevancy scores for your search results may change. Relevancy models trained in the previous release should continue to produce the same result ordering. Models trained more than one release ago may revert to the default relevancy model.

Successful relevancy tuning requires at least 10,000 stored search event signals for a search profile. If the search profile has fewer than 10,000 signals stored, relevancy tuning fails with an error message and AI Search continues to use the original relevancy model for that search profile.

## Relevancy model for auto-complete suggestions

AI Search uses a dedicated relevancy model to rank records for display as auto-complete suggestions in the search field. This relevancy model scores records based on their freshness and on search query term matches in their **title** fields. The system doesn't train this auto-complete suggestion relevancy model. For details on configuring auto-complete suggestions, see [Auto-complete suggestions in AI Search applications](auto-complete-ais.md#).

## Viewing relevancy scores for search results

Search administrators can view the scores for search results in the Search Preview UI from the Advanced AI Search Management Tools ServiceNow® Store application. For details on using this feature to investigate search behavior, see [Search Preview UI for AI Search](../../../use/dashboards/application-content-packs/ai-search-preview.md#).

**Parent Topic:**[Administering AI Search](administer-ais.md)


---
title: AI Search Genius Result Configuration form
description: The AI Search Genius Result Configuration form contains information about Genius Result configurations defined for your search profiles in AI Search. Use this form when creating or modifying a Genius Result configuration.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Genius Result Configuration form

The AI Search Genius Result Configuration form contains information about Genius Result configurations defined for your search profiles in AI Search. Use this form when creating or modifying a Genius Result configuration.

For details on creating or editing a Genius Result configuration, see [Create a Genius Result configuration](../task/create-genius-results-config-ais.md).

<table id="table_wqk_ttg_trb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Genius Result configuration.

</td></tr><tr><td>

Trigger condition

</td><td>

Condition that triggers evaluation of the Genius Result configuration. Supported values:

-   **Always**: The Genius Result configuration triggers for every search query.
-   **NLU**: The Genius Result configuration triggers when the search query's detected intent matches an [NLU model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nlu-service/nlu-models.md) intent. To use this trigger condition, you must link the NLU model and one or more of its intents to your Genius Result configuration. For instructions, see [Link an NLU model and intents to a Genius Result configuration](../task/link-nlu-model-genius-result-ais.md).

**Note:**

For an NLU trigger condition to function, the NLU model must be published. You can verify NLU model status by navigating to **All** &gt; **AI Search** &gt; **Search Query Settings** &gt; **Search Intents**.

-   **Term**: The Genius Result configuration triggers when the search query exactly matches a specified set of query terms.

**Note:** Exact matching means that the search query must contain only the specified terms in the specified order. For example, if you define `conference room` as the trigger term, a search for `conference room` triggers the Genius Result condition but searches for `hotel conference room` or `room conference` don't trigger it.


</td></tr><tr><td>

Term

</td><td>

Term that triggers the Genius Result configuration when it exactly matches the search query. This field appears only when you select **Term** from the **Trigger condition** field.

</td></tr><tr><td>

Application

</td><td>

Application scope for the Genius Result configuration. This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Option to activate the Genius Result configuration. Inactive Genius Result configurations never trigger.

</td></tr><tr><td>

Processor script template

</td><td>

Sample server-side script function. Use the code displayed in this field as a basis for your **AI Search request processor** and **AI Search response processor** scripts. This field is automatically set.

</td></tr><tr><td>

AI Search request processor

</td><td>

Server-side script function that takes a GeniusResultContext object as its parameter. The function must return a GeniusResultAnswer object that contains a search query. Up to three results from this search query display as Genius Result answer cards.**Note:** This field is required if **AI Search response processor** isn't populated. You can copy the code from the **Processor script template** to use as a starting point for your script function.

 When a search query triggers the Genius Result configuration, the system executes this script and then sends both the triggering search query and the scripted search query to the AI Search back end for computation of search results.

 To define a search query, use the GeniusResultAnswer.setTable\(\), GeniusResultAnswer.addSearchPhrases\(\), and GeniusResultAnswer.setSearchPhrase\(\) API methods.

 For details of API methods usable in this script function, including examples of use, see the [GeniusResultAnswer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GeniusResultAnswerScopedAPI.md) and [GeniusResultContext](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GeniusResultContextScopedAPI.md) scoped JavaScript API descriptions.

**Note:** The GeniusResultContext.getMatchingDocuments\(\) API method returns no results when invoked in an **AI Search request processor** script, since the script is executed before AI Search computes results for the triggering search query. Don't use this method in your request processor scripts.

</td></tr><tr><td>

AI Search response processor

</td><td>

Server-side script function that takes a GeniusResultContext object as its parameter. The function must return a GeniusResultAnswer object that defines one or more maps of key-value pairs. You can display these key-value pairs on the Genius Result answer card by specifying them as **Return fields**.**Note:** This field is required if **AI Search request processor** isn't populated. You can copy the code from the **Processor script template** to use as a starting point for your script function.

 When a search query triggers the Genius Result configuration, the system executes this script after AI Search computes search results.

 To define your map of key-value pairs, use the GeniusResultAnswer.addDataMap\(\) API method. Each key-value pair represents a field name and value that you can display on the Genius Result answer card using the **Return fields** list.

 For details of API methods usable in this script function, including examples of use, see the [GeniusResultAnswer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GeniusResultAnswerScopedAPI.md) and [GeniusResultContext](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GeniusResultContextScopedAPI.md) scoped JavaScript API descriptions.

</td></tr><tr><td>

Return fields

</td><td>

Comma-separated list of fields to display on the Genius Result answer card. This field is required if **AI Search response processor** is populated. Behavior depends on which processor script field is populated:

-   If **AI Search response processor** is populated, you must use this field to specify the names of fields defined in your GeniusResultAnswer response object that you want to display on the Genius Result answer card.
-   If **AI Search response processor** isn't populated, the Genius Result answer card automatically displays the common AI Search index fields:

    -   ai\_search\_parent\_title
    -   ai\_search\_teaser\_text
    -   ai\_search\_teaser\_title
    -   record\_class\_name
    -   sys\_id
    -   table
You can optionally use this field to specify any additional AI Search index fields that you want to display for search results shown on the Genius Result answer cards.

To view the list of AI Search index fields, see [AI Search index fields](index-fields-list-ais.md).


</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)


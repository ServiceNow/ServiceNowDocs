---
title: Configure dynamic filters in AI Search for Recommended Actions
description: Configure AI Search to preprocess contextual inputs from Recommended Actions so that search results are dynamically filtered based on the current record context.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring AI search, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configure dynamic filters in AI Search for Recommended Actions

Configure AI Search to preprocess contextual inputs from Recommended Actions so that search results are dynamically filtered based on the current record context.

## Before you begin

Role required: admin

## About this task

When search results are generated in Recommended Actions, you can make them contextually relevant to the current record by using the contextual information passed in the additional context payload of the AI Search API. Using this contextual information, you can implement preprocessing logic through the **AisDynamicFilter** extension point to filter search results based on conditions that match the current context record.

When preprocessing is implemented, AI Search considers the defined filter conditions before returning search results, ensuring that only results matching those conditions are displayed. For example, you can define a filter condition to exclude the current context record from search results, so that the record you are working on does not appear in the recommendations.

## Procedure

1.  Enable dynamic filtering for a specific search source in a search profile.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search profiles**.

    2.  Select a search source of your choice from the Search Sources related list.

2.  In the selected search source, select the **Has Dynamic Filters** check box and select **Save**.

    **Note:** There may be multiple search profiles in your instance. Enable contextual filtering only for the search sources in a profile where you need this functionality. For more information on Search source form, see [Search Source form](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/ai-search/reference/search-source-form-ais.html).

3.  Create the AisDynamicFilter implementation for search sources.

    1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

    2.  Open the **AisDynamicFilter** extension point.

    3.  Create an implementation by selecting the **Create Implementation** link.

        In the implementation:

        -   `isApplicable`: This method defines the conditions that determine if dynamic filters should be applicable for a given search source or not. Use the `additionalContext` stringified JSON with the following format in the implementation. It defines the contextual information passed to the AI Search API which is used in AI Search Dynamic filters to contextually filter out the search results.
        -   `getFilterCondition`: Use this method to define the filter criteria that AI Search applies to search results during preprocessing.
        **Note:** Do not implement the `shouldRemoveDocument` method.

        Example: The following is an example implementation of how to exclude current context record from the search results:

        ```
        isApplicable: function(searchContextConfigId, profileId, tableName, additionalContext, preprocess) {
                if (additionalContext != null && JSON.parse(additionalContext).source == 'recommended-actions' && tableName == JSON.parse(additionalContext).contextRecordTable && preprocess) {
                    return true;
                }
                return false; 
            },
            getFilterCondition: function(searchContextConfigId, profileId, tableName, additionalContext) {
                if (additionalContext != null && JSON.parse(additionalContext).source == 'recommended-actions' && tableName == JSON.parse(additionalContext).contextRecordTable) {
                    var pasedAdditionalContext = JSON.parse(additionalContext);
                    var gr = new GlideRecord(tableName);
                    gr.addEncodedQuery('sys_id!=' + pasedAdditionalContext.contextRecordId);
                    gr.query();
                    return gr;
                }
        
            }, 
        
            shouldRemoveDocument: function(searchContextConfigId, profileId, recordClass, sysId, additionalContext) {
               
            },
        ```

        The parameters in the preceding additionalContext are defined as:

        -   `contextRecordId`: Sys ID of the current context record where recommendations are surfaced.
        -   `contextRecordTable`: Table name of the current context record where recommendations are surfaced.
        -   `contextualInputs`: Inputs to the context record.
        -   `source`: Origin of the search request which is predefined as Recommended Actions. This allows you to scope your filter conditions specifically to Recommended Actions, so the filtering logic does not apply to other search contexts.

## Result

In the Search tab of the Recommended Actions context side panel, only the search results that match the exact context of the current record appear.


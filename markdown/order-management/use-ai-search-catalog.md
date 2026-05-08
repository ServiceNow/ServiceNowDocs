---
title: Use AI Search in product catalogs
description: As an agent or customer, use AI Search queries in the product catalog to find relevant product offerings or service specifications. For example, you can search by product offering characteristics or other attributes, when adding products in Sales Customer Relationship Management transactions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Product catalogs, Lead-to-cash foundation apps, Use, Sales Customer Relationship Management]
---

# Use AI Search in product catalogs

As an agent or customer, use AI Search queries in the product catalog to find relevant product offerings or service specifications. For example, you can search by product offering characteristics or other attributes, when adding products in Sales Customer Relationship Management transactions.

## Before you begin

Role required: sales agent, order agent, customer

## About this task

With AI Search, you can use semantic queries to find relevant product offerings or service specifications for a transaction. Your queries can contain terms or phrases to find catalog items. AI Search considers the context for your search, such as the user intent, to return appropriate results. As you enter your query, AI Search provides various features to make your search more efficient.

-   **Auto-complete suggestions**: When you start entering text in the search bar, AI Search displays auto-complete suggestions to help you get directly to the results you need. Suggestions may include recent search queries, recently viewed search results, or search queries or results that match the terms you're typing into the search bar. Select one of the suggestions from the list to display the product offering.
-   **Auto-correction \(typo handling\)**: If your queries are incomplete or misspelled, AI Search automatically replaces misspelled search query terms with spellings found in indexed content. Typo corrections are displayed above search results.
-   **Search result order**: You can use the Sort by filter to organize your results by Relevancy, Display name, Code or Description.

## Procedure

1.  Access the product catalog through a Sales Customer Relationship Management transaction, such as a quote created in the CSM Configurable Workspace or an order created in the Business Portal.

2.  Select the Catalog tab to open the catalog interface, then choose the appropriate catalog.

3.  In the sort filter, select how you want your search results to be listed:

    -   **Relevancy**: Lists the most relevant records first, based on rank and order. You cannot change the order of the results \(ascending or descending\). This option is selected by default.
    -   **Display name**: Lists results by the Display names for each product offering.
    -   **Code**: Lists products by a Code that was assigned to each offering, either system-created or set by the product catalog admin when the product offering was created.
    -   **Description**: Lists results by the Description for each product offering.
    You can use the ascending or descending filter to further order the results by Display name, Code, or Description.

4.  Enter a search term in the search bar, then press **Return** to generate the search results

    As you’re entering a query, auto-complete suggestions are displayed if your query matches any indexed terms. You can select one of the suggestions to display the product offering.The following table provides examples of terms, phrases, and operators that you can enter in your queries.

<table id="table_ukt_zqm_khc"><thead><tr><th>

Search query

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search by query terms

</td><td>

Specify terms and quoted phrases in the search query to find products that contain the same terms or phrases.-   Single-term search: Enter a specific term to find all catalog items that contain the term. For example, `sedan` finds any products that contain this characteristic, parent products containing child products with this characteristic, and related products that have semantic similarity to this search term or results.
-   Multi-term search: Enter multiple words in a phrase to find catalog items that contain any of the terms in a phrase. For example `connected car` returns catalog items that contain the terms `connected` and `car`.
-   Quoted phrase search: Use double quotes to return catalog items for a specific phrase, such as `"connected car"`.
**Note:** AI Search ignores letter case for search query terms and phrases.

</td></tr><tr><td>

Search using Boolean operators

</td><td>

Separate query terms and phrases with Boolean operators to override the default matching logic for the search query:-   `OR`: Enter this Boolean disjunction operator to find products that contain any of the terms or phrases separated by `OR`.
-   `-` \(hyphen\): Enter this Boolean negation operator to exclude products containing the term or phrase that immediately follows the hyphen.


</td></tr><tr><td>

Search using wild cards

</td><td>

Use wildcard operators to find records that contain indexed terms matching a wildcard pattern:-   `%`: Enter this single-character wildcard operator in a search query term to match any one character in an indexed term. For example, `fib%r` finds all products with the word `fiber`.
-   `*`: Enter this string wildcard operator in a search query term to match any string of zero or more characters in an indexed term.
-   `***`: Enter this universal wildcard operator to find all indexed terms.
**Note:** The `%` and `*` operators must follow at least three non-wildcard characters to get appropriate results. Otherwise the search returns only the catalog items that are an exact match.

</td></tr></tbody>
</table>5.  Do one of the following:

    -   If the search results returned a product that you want to add, select the product offering so that it can be added as line item to the transaction. If the product that you select is customizable, the configurator opens so that you can configure the offering.
    -   If you want to continue with another query, select **Clear** to remove the current search and sort option, then enter a new query in the search bar. The search query and sort option are cleared. The sort option is reset to Relevancy, which is the default value.

**Parent Topic:**[Using product catalogs](../concept/using-product-catalog.md)

**Related topics**  


[bundle-platadm.query-language-ais]


---
title: Zing index and search dictionary attributes
description: The following dictionary attributes either affect the way Zing indexes tables or ranks search results.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing index and search dictionary attributes

The following dictionary attributes either affect the way Zing indexes tables or ranks search results.

## Index and search dictionary attributes

Zing uses dictionary attributes set at the table or field level to configure the following settings:

-   indexing behavior
-   ranking of search results
-   the BM25 relevancy ranking algorithm

|Name|Data Type|Applies To|Applies to V3 or V4|Description|Label|Needs re-indexing?|Root Table Only|
|----|---------|----------|-------------------|-----------|-----|------------------|---------------|
|attachment\_index|boolean|Table|Both|If true, attachments on the table are indexed for search purposes.|Attachment Index|TRUE|FALSE|
|no\_text\_index|boolean|Both|Both|This attribute on a field prevents the field from being included in a text index.|No Text Index|TRUE|FALSE|
|text\_index \_attachment\_body \_weight|float|Table|V4|Specifies how much consideration \(weight, a float value\) to give a search term found in the body of an attachment. For more information on how weight value affect search result relevancy, see [Zing computes document scores using three components](../concept/c_DocumentScoring.md).|Text Index Attachment Body Weight|FALSE|TRUE|
|text\_index \_attachment\_displayed|boolean|Table|Both|Displays attachments in text search results.|Text Index Attachment Displayed|FALSE|FALSE|
|text\_index\_attachment \_title\_weight|float|Table|V4|Specifies how much consideration \(weight, a float value\) to give a search term found in the title of an attachment. For more information on how weight value affect search result relevancy, see [Zing computes document scores using three components](../concept/c_DocumentScoring.md).|Text Index Attachment Title Weight|FALSE|TRUE|
|text\_index \_auto\_stop|boolean|Table|Both|Automatically identifies stop words and doesn't index them. Based on the threshold specified in text\_index\_auto\_stop\_threshold.|Text Index Auto Stop|TRUE|TRUE|
|text\_index\_auto \_stop\_threshold|int|Table|Both|Threshold \(integer, number of occurrences\) for a word to become a stop word automatically. See text\_index\_auto\_stop.|Text Index Auto Stop Threshold|TRUE|TRUE|
|text\_index\_default \_partial\_matching\_rule|String|Table|Both|String for partial matching rule configuration. Input should be based on [Change the query mode of an indexed table](../task/configure-table-query-mode.md).|Text Index Default Partial Matching Rule|FALSE|TRUE|
|text\_index \_default\_query\_mode|String|Table|Both|String for query mode configuration. Input should be based on [Change the query mode of an indexed table](../task/configure-table-query-mode.md)|Text Index Default Query Mode|FALSE|TRUE|
|text\_index \_disable\_synonym|boolean|Table|Both|TRUE disables searching on synonyms as well as the search term.|Text Index Disable Synonym|FALSE|TRUE|
|text\_index \_enable\_idf|boolean|Table|V3|TRUE enables [TF-IDF](https://www.geeksforgeeks.org/tf-idf-model-for-page-ranking/)scoring.|Text Index Enable IDF|FALSE|TRUE|
|text\_index \_filter\_junk|boolean|Table|Both|TRUE by default, FALSE disables the junk filter for a table. By default, Zing doesn't index or search for 2-digit numbers and single character words \(unless they are Chinese or Japanese characters\). Regenerate the index after disabling the junk filter. This attribute results in a larger table index. For optimal performance, don't apply it unless it's required.|Text Index Filter Junk|TRUE|TRUE|
|text\_index \_filter\_query|An encodedQuery on the table|Table|Both|Use this attribute when you want to index the rows matching specific filter conditions. The attribute value must be an encodedQuery on the table.|Index Filter|TRUE|FALSE|
|text\_index\_filterable|boolean|Column|Both|If a field with this attribute set to true, is changed, the row is evaluated for re-indexing \(even if the field itself isn't indexable\).|Index Filterable|TRUE|FALSE|
|text\_index\_include \_stop\_word|boolean|Table|Both|if you need to index stop words in this table, set this attribute to true.|Text Index Include Stop Word|TRUE|TRUE|
|text\_index\_scorer\_bm25\_b|float|Table|V4|This attribute is the b parameter used in the BM25 algorithm. See [text\_index\_scorer\_bm25\_b](index-attributes.md#section_ppp_3gl_thb).|bm25\_b|FALSE|TRUE|
|text\_index\_scorer\_bm25\_k1|float|Table|V4|This attribute is the K1 parameter used in the BM25 algorithm. See [text\_index\_scorer\_bm25\_k1](index-attributes.md#section_wl4_4gl_thb).|bm25\_k1|FALSE|TRUE|
|text\_index\_tags|String|Table|Both|Should be set to specific String: empty/everyone\_only/all\_shared, depending on type of tags that wants to be indexed.|Text Index Tags|TRUE|FALSE|
|text\_index\_tokenizer \_language|String|Table|Both|Put "ja" \(without double quote\) when there is need to support tokenization in Japanese.|Text Index Tokenizer Language|TRUE|TRUE|
|text\_index\_translations|boolean|Table|Both|If present or true, forces indexes to be recalculated when translated strings are added. Requires sys-admin role to modify. Automatically set for indexed fields that are translated, and to fields that have a translation and are being indexed. The glide.i18n.force\_index system property, which defaults to true, overrides this attribute.|Text Index Translations|TRUE|FALSE|
|text\_search\_and\_or\_limit|int|Table|Both|Add table level custom attribute text\_search\_and\_or\_limit that overrides the global property.|Text Search And Or Limit|FALSE|FALSE|
|ts\_language|String|Column|Both|Added to allow for text indexing of only specific languages.|Text Search Language|TRUE|FALSE|
|ts\_multi\_value\_field \_splitter|String|Column|Both|If one field is a multi-value field, add the splitter in the field in this attribute to spread out index positions of the values. For example, to separate multi:value, put : for this attribute.|Text Search Multi-value Field Splitter|TRUE|TRUE|
|ts\_weight|int|Column|Both|Controls the relative importance of a match in the field for text search. For more information on how weight value affect search result relevancy, see [Zing computes document scores using three components](../concept/c_DocumentScoring.md). To learn how to set text search weight for a field, see [Set the relative weight of a field](../task/t_ControlMatchRelevanceByField.md).|Text Search Weight|FALSE|FALSE|

## no\_text\_index

For Customer Service and Support guidelines on setting the **no\_text\_index** option for different field types, see [KB0859922](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0859922) on the Now Support site.

## text\_index\_scorer\_bm25\_b

This dictionary attribute is part of the BM25 algorithm. The attribute impacts the importance of the length of a document in search results. If this attribute is 0, the length has no bearing. In this case, a document of two words would be valued equally as a document with 1000 words. Very short documents are often weighted lower than longer documents. The default is 0.75.

## text\_index\_scorer\_bm25\_k1

This dictionary attribute is part of the BM25 algorithm. The attribute helps determine term frequency saturation characteristics, that is, having the search term appear in a document increases the relevancy of the document, but the increase is less impactful as the numbers climb. For example, a search term occurring 10 times in a document makes it more relevant than a document that has only one occurrence. However, a document that has 100 occurrences of the search term may not be ten times more impactful than a document that has 10 occurrences. The relevance approaches a maximum effect asymptote. The higher the attribute value, the lower the maximum effect of multiple occurrences. Typical values are between 1.25 - 2.0.

**Parent Topic:**[Zing indexes words](../concept/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](../concept/c_PunctuationForSearchResults.md)

[Zing indexes some HTML elements](../concept/c_SearchingHTMLContent.md)

[Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)

[Configure a text index group to search across multiple tables](../task/index-multiple-tables.md)

[Regenerate a text index for a table](../task/t_RegenerateATextIndexForATable.md)

[Remove an index](../task/t_RemoveAnIndex.md)

[Remove an index for a specific field](../task/t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](../task/remove-index-child-table.md)

[Change the query mode of an indexed table](../task/configure-table-query-mode.md)

[Enable indexing of text in multi-row variable sets](../task/index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](../task/configure-tables-japanese-tokenizer.md)


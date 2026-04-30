---
title: Zing indexes some HTML elements
description: Zing indexes the contents of certain HTML elements to improve document search results. This indexing is addition to the normal indexing by word.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing indexes some HTML elements

Zing indexes the contents of certain HTML elements to improve document search results. This indexing is addition to the normal indexing by word.

|HTML element|Description|
|------------|-----------|
|Title attribute|Zing indexes the contents of the **title** attribute of any HTML element. This is separate from the **title** element, which Zing already indexes when identifying the words of the document.|
|Anchor link target|Zing indexes the target URL specified in the **href** attribute of any anchor element.|
|Alt text for an image|Zing indexes the alternative text of any image element.|

**Parent Topic:**[Zing indexes words](zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](c_PunctuationForSearchResults.md)

[Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)

[Configure a text index group to search across multiple tables](../task/index-multiple-tables.md)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](../task/t_RegenerateATextIndexForATable.md)

[Remove an index](../task/t_RemoveAnIndex.md)

[Remove an index for a specific field](../task/t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](../task/remove-index-child-table.md)

[Change the query mode of an indexed table](../task/configure-table-query-mode.md)

[Enable indexing of text in multi-row variable sets](../task/index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](../task/configure-tables-japanese-tokenizer.md)


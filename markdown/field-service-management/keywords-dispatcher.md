---
title: Configure keyword searching in Dispatcher Workspace
description: Use specific keyword formatting, powered by ServiceNow Zing, to quickly locate tasks and resources in Dispatcher Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure keyword searching in Dispatcher Workspace

Use specific keyword formatting, powered by ServiceNow® Zing, to quickly locate tasks and resources in Dispatcher Workspace.

## How Zing search works

Dispatcher Workspace uses ServiceNow® Zing, ServiceNow®'s text indexing and search engine, to deliver fast results ranked by relevance. Zing search engine logic yields fast results and emphasizes relevancy scoring. Relevancy scores include frequency and proximity weighting. Scores also include weighting for specific indexed fields such as title, short description, and metadata. For more information on Zing, see [Zing text indexing and search engine](https://www.servicenow.com/docs/access?context=c_ZingTextSearch&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Indexing scope and prerequisites

Before relying on keyword search, review how your instance indexes tables, attributes, and values and confirm that the required tables are included. For more information, see [Configure a table for indexing and searching](https://www.servicenow.com/docs/access?context=configure-single-table-for-indexing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Some fields are excluded from text indexing. For more information see the “Fields excluded from text indexing” table in [Configure a table for indexing and searching](https://www.servicenow.com/docs/access?context=configure-single-table-for-indexing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

If you use Territory planning then navigate to **All** &gt; **System Definitions** &gt; **Text index** and verify that you see the following tables:

-   `sn_tp_territory`
-   `sn_tp_territory_membership_override`

If you're using Territory planning and don't see the tables listed above, then complete Step 5e in [Configure a table for indexing and searching](https://www.servicenow.com/docs/access?context=configure-single-table-for-indexing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Language and punctuation considerations

Zing indexes words based on the language of your content. Review the rules for how Zing indexes words in [Zing indexes words](https://www.servicenow.com/docs/access?context=zing-indexes-words&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Zing indexes some punctuation marks as part of some words to improve search results for common search terms. For more information, see [Zing indexes punctuation as part of some words](https://www.servicenow.com/docs/access?context=c_PunctuationForSearchResults&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Supported keyword features in Dispatcher Workspace

Zing keywords in Dispatcher Workspace supports the following:

-   Boolean operators, like AND and OR, but they must be used in capital letters. There are more Boolean operators used as well, for more information, see [Boolean operators allow conditional search results](https://www.servicenow.com/docs/access?context=c_BooleanOperators&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Exact phrase searches denoted by quotation marks. For more information, see [Quotation marks allow exact phrase searches](https://www.servicenow.com/docs/access?context=c_PhraseSearches&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Single-character and multiple-character wildcards, denoted by characters like %. For more information, see [Wildcard characters allow searching for patterns and variations](https://www.servicenow.com/docs/access?context=c_Wildcards&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

The table below shows what tables Zing searches when you use keywords based on the setting or configuration you have.

|Table name|Only Dispatcher Workspace|Territories enabled|Crew plugin active|Equipment plugin active|Contractor plugin active|
|----------|-------------------------|-------------------|------------------|-----------------------|------------------------|
|sys\_user|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|
|sys\_user\_group|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)|
|sn\_tp\_territory| |![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)| | | |
|sn\_tp\_territory\_membership| |![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)| | | |
|sn\_fsm\_resource| | | |![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)| |
|wm\_crew| | |![](../../../reuse/icons/product-icons/circle-check-fill-24.svg)| | |

For examples on how to use Zing keywords in Dispatcher Workspace, see [Searching in Dispatcher Workspace examples](search-keyword-example.md).


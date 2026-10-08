---
title: Reindex the product offering search index
description: Reindex the Product Offering Indexed Source so that AI Search considers the product offering display name, in addition to product characteristics, when ranking search results in the product catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/reindex-product-offering-search.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [AI Search for product catalog, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Reindex the product offering search index

Reindex the Product Offering Indexed Source so that AI Search considers the product offering display name, in addition to product characteristics, when ranking search results in the product catalog.

## Before you begin

Role required: admin

## About this task

Product offerings with a display name that closely matches a search term can rank lower than other offerings that only reference them, such as a bundle that includes the offering. Reindexing the Product Offering Indexed Source adds the display name to semantic indexing so that the offering that most closely matches the search term ranks highest.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  In the **Name** field, search for `Product Offering Indexed Source` and select it.

3.  Select **Index Selected Table/s**.

4.  In the **Generate Text Index - Single Table** dialog box, select **sn\_prd\_pm\_product\_offering** from the drop-down menu and select **Index**.


## Result

When indexing is complete, the **Keyword Ingestion State** and **Semantic Ingestion State** columns show indexed in the Indexing History related list.

**Related topics**  


[Use AI Search in product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/use-ai-search-catalog.md)


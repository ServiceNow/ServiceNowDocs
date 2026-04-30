---
title: Variable types supported by AI Search indexing
description: AI Search can index searchable content and metadata from multiple variable types found on indexed source records.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Variable types supported by AI Search indexing

AI Search can index searchable content and metadata from multiple variable types found on indexed source records.

## Variable types indexed from variables column

When indexing records from any source table, AI Search retrieves searchable content from supported variable types when they're present in a source record column that has name **variables** and type **Variables**.

Supported variable types include:

-   Email
-   Multi-line text
-   Single-line text
-   URL
-   Wide single-line text

## Service Catalog variable types indexed from Catalog Items

When indexing records from the Catalog Item \[sc\_cat\_item\] table and tables that extend it, AI Search can retrieve searchable content from these Service Catalog variable types:

-   [Multiple choice](https://www.servicenow.com/docs/access?context=multiple-choice&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Select box](https://www.servicenow.com/docs/access?context=select-box&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

Other variable types aren't supported for catalog variable indexing.

Catalog variable indexing is not active in the base system, but it's activated if you've installed the Now Assist in AI Search application. To learn how to activate and configure catalog variable indexing, see [Activate indexing of catalog variable content on Catalog Item records](../task/activate-catalog-variable-indexing.md). For details on the Now Assist in AI Search application, see [Now Assist in AI Search](now-assist-ais.md).

For the full list of available Service Catalog variable types, see [Types of Service Catalog variables](https://www.servicenow.com/docs/access?context=r_VariableTypes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[AI Search reference](../concept/reference-ais.md)


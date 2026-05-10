---
title: Activate indexing of catalog variable content on Catalog Item records
description: Activate indexing of searchable content from variables on Catalog Item records. Configure the set of Catalog Items eligible for catalog variable indexing and the set of variables to index.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate indexing of catalog variable content on Catalog Item records

Activate indexing of searchable content from variables on Catalog Item records. Configure the set of Catalog Items eligible for catalog variable indexing and the set of variables to index.

## Before you begin

Role required: admin

## About this task

AI Search supports indexing of searchable content from variables on records in the Catalog Item \[sc\_cat\_item\] table and tables that extend it. By default, this functionality is not active. Administrators can activate indexing of catalog variable content and configure the set of Catalog Items and catalog variables to index content from.

For details on the catalog variable types that AI Search can index content from, see [Variable types supported by AI Search indexing](../reference/variable-types-ais-index.md).

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Activate indexing of searchable content from catalog variables that are accessible to all users.

    1.  Locate and open the **glide.ais.ingestion.index\_catalog\_variables** system property record.

        If this system property record doesn't exist, select **New**, then enter **glide.ais.ingestion.index\_catalog\_variables** as the new record's name and select **true \| false** as its type.

    2.  Set the record's value to **true**.

    3.  Select **Update**.

        If you created a new system property record, select **Submit** instead.

    AI Search indexes content from catalog variables that don't require any role to read.

3.  Activate indexing of searchable content from catalog variables that require specific roles for read access.

    **Note:** This step has no effect if **glide.ais.ingestion.index\_catalog\_variables** is set to **false**.

    1.  Open the **glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles** system property record.

        If this system property record doesn't exist, select **New**, then enter **glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles** as the new record's name and select **true \| false** as its type.

    2.  Set the record's value to **true**.

    3.  Select **Update**.

        If you created a new system property record, select **Submit** instead.

    AI Search indexes content from catalog variables that are only readable by users with specific roles.

4.  Filter the set of Catalog Item records from which AI Search indexes catalog variables.

    **Note:** This step has no effect if **glide.ais.ingestion.index\_catalog\_variables** is set to **false**.

    1.  Open the **glide.ais.ingestion.catalog\_variables\_filter\_query** system property record.

        If this system property record doesn't exist, select **New**, then enter **glide.ais.ingestion.catalog\_variables\_filter\_query** as the new record's name and select **string** as its type.

    2.  In the **Value** field, enter an encoded query string to restrict the set of Catalog Item records that AI Search indexes catalog variables from.

        As an example, enter **active=true** if you only want AI Search to index catalog variables from active Catalog Item records. For details on creating encoded query strings, see [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md).

    3.  Select **Update**.

        If you created a new system property record, select **Submit** instead.


## What to do next

After changing the values of these system properties, reindex content from the Catalog Item Table indexed source and any indexed sources for tables that extend the Catalog Item \[sc\_cat\_item\] table. For details on reindexing content from indexed sources, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md) and [Perform a full table index or reindex for multiple AI Search indexed sources](index-multiple-sources-ais.md).

**Parent Topic:**[Indexed sources in AI Search](../concept/indexed-sources-ais.md)


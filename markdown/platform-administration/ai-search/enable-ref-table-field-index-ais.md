---
title: Enable indexing of referenced table fields for an AI Search indexed source
description: Configure an indexed source to index field values from tables referenced by fields in the source table. You can index these field values for use in filters and EVAM search result configurations, index them for search, or both.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Field settings, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable indexing of referenced table fields for an AI Search indexed source

Configure an indexed source to index field values from tables referenced by fields in the source table. You can index these field values for use in filters and EVAM search result configurations, index them for search, or both.

## Before you begin

You must have an indexed source configured for the source table. For details on creating an indexed source for a table, see [Create an indexed source](create-indexed-source-ais.md).

Role required: ais\_admin

## About this task

When an indexed source table includes a reference field, AI Search defaults to indexing values for the reference field but not for other fields on the table that it references. To index values from these referenced table fields, you can create **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings on your indexed source table.

-   To use field values from referenced tables in search source filters, facet filters, and EVAM search result configurations, create a **dot\_walk\_fields** field setting.
-   To make field values from referenced tables searchable, create a **searchable\_dot\_walk\_fields** field setting.

As the value for either of these field settings, list the names of the referenced table fields you want to index, separated by commas. For example, to index the **name** and **city** fields from the table referenced by the **company** field on the indexed source table, select the **company** field and enter value `name,city`.

To dot-walk across multiple tables, you can enter field name values with dot-separated reference field prefixes. For example, enter value `company.contact.name` to index the **name** field in the table referenced by the **contact** field on the table referenced by the indexed source table's **company** reference field.

**Note:** Each dot-walk reference level imposes a performance impact on indexing. Avoid using multi-level references unless necessary.

You can create both **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings for the same reference field.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  In the Field Settings &amp; Mapping related list, select **New**.

3.  On [the Field Setting form](../reference/field-setting-form-ais.md), enter the field values shown for your use-case.

    -   To index field values from referenced tables for use in search source filters, facet filters, and EVAM search result configurations, enter the following field values.

        |Field|Value|
        |-----|-----|
        |Attribute|dot\_walk\_fields|
        |Field|&lt;name of indexed source table reference field that you want to use to dot-walk to another table&gt;|
        |Value|&lt;comma-separated list of names for fields that you want to index from the referenced table&gt;|

    -   To index field values from referenced tables as searchable text, enter the following field values.

        |Field|Value|
        |-----|-----|
        |Attribute|searchable\_dot\_walk\_fields|
        |Field|&lt;name of indexed source table reference field that you want to use to dot-walk to another table&gt;|
        |Value|&lt;comma-separated list of names for fields that you want to index from the referenced table&gt;|

    **Note:** If the **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** attributes don't appear in the **Attribute** selection list, ensure that your **Field** selection is a reference field.

4.  Select **Submit**.

    The attribute and value appear in the Field Settings &amp; Mapping related list.


**Parent Topic:**[Field settings for AI Search](../concept/field-settings-ais.md)


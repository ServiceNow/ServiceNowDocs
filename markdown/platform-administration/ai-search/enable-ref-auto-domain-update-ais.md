---
title: Enable automatic domain updates for a referenced table
description: Configure a field setting to automatically index domain field value updates for records from a referenced table.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Domain separation and AI Search, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable automatic domain updates for a referenced table

Configure a field setting to automatically index domain field value updates for records from a referenced table.

## Before you begin

Role required: ais\_admin

## About this task

This topic provides steps for configuring a **dot\_walk\_fields** field setting to enable automatic indexing of domain field values for records in referenced tables. For more general instructions on defining field settings, see [Create a field setting for an AI Search indexed source](../concept/field-settings-ais.md#).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to define a field setting for.

3.  In the Field Settings &amp; Mapping related list, select **New**.

4.  On the Field Setting form, enter the following field values.

    |Field|Value|
    |-----|-----|
    |Attribute|dot\_walk\_fields|
    |Field|&lt;reference field&gt;|
    |Value|sys\_domain,sys\_domain\_path|

    For a description of the field values, see [Field Setting form](../reference/field-setting-form-ais.md).

5.  Select **Submit**.


## Result

The new **dot\_walk\_fields** field setting appears in the Field Settings &amp; Mapping related list.

## What to do next

To make the new **dot\_walk\_fields** attribute take effect, perform a full table reindex for the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Parent Topic:**[Domain separation and AI Search](../concept/ai-search-domain-separation.md)


---
title: Create an indexed source from the AI Search Admin console
description: Create an indexed source to make the content and metadata from the ServiceNow AI Platform table records that are searchable by using AI Search.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing the indexed sources from the AI Search Admin console, Using the AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an indexed source from the AI Search Admin console

Create an indexed source to make the content and metadata from the ServiceNow AI Platform table records that are searchable by using AI Search.

## Before you begin

Role required: admin or ais\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Shared Configurations** tab, select the **Indexed Sources** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

    For a description of the field values, see [Indexed Source form](../reference/indexed-source-form-ais.md).

    **Note:**

    -   You may see more field values on the form that aren't visible on your user interface. Make sure that you fill in all the required fields and ignore the extra fields.
    -   You can't create more than one indexed source for a single ServiceNow AI Platform table.
5.  Select **Save**.


## Result

The indexed source is created with the initial status set to never indexed. After completing the indexed source configurations, start an index job to make the content searchable.

## What to do next

To control how your new indexed source processes source records and fields during indexing, configure its indexed source attributes and field settings. For more information, see [Set up a field configuration for an indexed source](ais-admin-console-setup-field-config-indexed-source.md).

To make content from internal indexed sources and source records searchable, perform a full table index for your new indexed source. For more information, see [Index the content from an indexed source for searchability](ais-admin-console-start-content-indexing.md).

**Parent Topic:**[Managing the indexed sources from the AI Search Admin console](../concept/ais-managing-indexed-source.md)


---
title: Set up an indexed source attribute for indexing the search content
description: Set up an indexed source attribute to control how AI Search indexes content for all records in a source table.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing the indexed sources from the AI Search Admin console, Using the AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up an indexed source attribute for indexing the search content

Set up an indexed source attribute to control how AI Search indexes content for all records in a source table.

## Before you begin

Role required: admin or ais\_admin

## About this task

An indexed source attribute defines how records from an indexed source table are indexed in AI Search. For example, with indexed source attributes, you can control which records to index, how to handle specific data types, such as attachments or tags, and whether to include translated fields in the index. These attributes help customize the indexing process to your needs. For more information, see [Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md#).

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Shared Configurations** tab, select **Indexed Sources**.

3.  Select the indexed source that you want to configure the attributes for.

    The selected indexed source opens in the Configuration form view.

4.  In the Advanced configurations section, select **Edit**.

5.  Select **Create**.

6.  On the form, fill in the fields.

7.  <table id="table_uq3_l34_tdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attribute

</td><td>

Options to adjust indexing settings for an AI Search indexed source. You can select an attribute from the following list of options:-   **Index tags**: Control indexing of tags from indexed records.
-   **Translated fields**: Control indexing of translated fields from indexed records.
-   **Translated reference fields**: Control the indexing of translated reference fields from the indexed records.
-   **Attachments**: Control the indexing of attachments from indexed records.


</td></tr><tr><td>

Source

</td><td>

Specific table from the indexed source that the attribute applies to.

</td></tr><tr><td>

Which tags should be indexed

</td><td>

Type of tags to be indexed. You can select either option, shared tags and globally visible tags, or only globally visible tags, This field appears only if the Index tags option is selected in the attribute field.

</td></tr><tr><td>

Action

</td><td>

Option to enable or disable the indexing of a selected attribute.This field appears for all attributes except the Index tags.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

The new indexed source attribute is added in the Advanced configurations form.

**Parent Topic:**[Managing the indexed sources from the AI Search Admin console](../concept/ais-managing-indexed-source.md)


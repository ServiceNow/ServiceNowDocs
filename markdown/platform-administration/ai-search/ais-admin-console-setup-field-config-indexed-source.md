---
title: Set up a field configuration for an indexed source
description: Set up indexed source field configurations to control how AI Search indexes content for a specific field in your source table records.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing the indexed sources from the AI Search Admin console, Using the AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up a field configuration for an indexed source

Set up indexed source field configurations to control how AI Search indexes content for a specific field in your source table records.

## Before you begin

Role required: admin or ais\_admin

## About this task

A field setting controls the indexing behavior for a specified field \(column\) on all records from an indexed source. For more information, see [Field settings for AI Search](../concept/field-settings-ais.md#).

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Shared Configurations** tab, select **Indexed Sources**.

3.  Select the indexed source that you want to configure the fields for.

    The selected indexed source opens in the Configuration form view.

4.  In the Field configurations section, select **Edit**.

5.  Select **Create**.

6.  On the form, fill in the fields.

7.  <table id="table_uq3_l34_tdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field configuration

</td><td>

Options to adjust the indexing behavior for source record fields in anAI Search indexed source. You can select a field setting from the following list of options:-   **Exclude field from index**: Option to exclude content from a specific field in your records from being searchable in AI Search.
-   **Exclude field from search**: Option to disable search matching for content that is indexed from the selected field.
-   **Include calculated field in index**: Option to enable indexing of searchable content from the calculated field values.
-   **Include dot-walk fields in index**: Index reference and display values from the reference field's source table for use in search filters and result configurations.
-   **Remap AI Search fields**: Option to map the selected field from the indexed source table to an AI Search index field. AI Search fills the index field with the value from the source field when indexing records.


</td></tr><tr><td>

Source

</td><td>

Specific table from the indexed source that the field setting applies to.

</td></tr><tr><td>

Field

</td><td>

Record field that the field setting operates on.The name of this field changes based on the selected field configuration.

-   If you have selected any of the exclude options, the field name is **Field to exclude**.
-   If you have selected the **Include calculated field in index** option, the field name changes to **Calculated field**.
-   If you have selected the **Include dot-walk fields in index** option, the field name changes to **Reference field**.


</td></tr><tr><td>

Add dot walk fields

</td><td>

Option to add a dot walk field. This field appears only if the **Include dot-walk fields in index** option is selected in the field configuration.

</td></tr><tr><td>

Searchable

</td><td>

Option to enable the field keyword searchable.This field appears only if the **Include dot-walk fields in index** option is selected in the field configuration.

</td></tr><tr><td>

Map to AI Search field

</td><td>

AI Search index field to match the specific field from your indexed source table.

</td></tr><tr><td>

Map as raw value

</td><td>

Option to map to the underlying sys\_id for a reference field.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

The new field setting appears in the Field configurations section.

## What to do next

To make the new field configurations take effect, perform a full table reindex for the indexed source. For more information, [Index the content from an indexed source for searchability](ais-admin-console-start-content-indexing.md) see

**Parent Topic:**[Managing the indexed sources from the AI Search Admin console](../concept/ais-managing-indexed-source.md)


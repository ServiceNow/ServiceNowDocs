---
title: Customize column descriptions and usage instructions
description: Create custom column descriptions and usage instructions in the Semantic Column Configuration table so that customizations can be transferred between instances via update sets.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 2
keywords: [semantic layer, column descriptions, usage instructions, query generation, dimensions, Semantic Column Configuration, update sets]
breadcrumb: [Customizing semantic metadata, Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Customize column descriptions and usage instructions

Create custom column descriptions and usage instructions in the Semantic Column Configuration table so that customizations can be transferred between instances via update sets.

## Before you begin

Role required: sn\_query\_gen.admin or higher

## About this task

The Query Generation semantic layer uses column descriptions and usage instructions to help AI understand what each field represents and how to query it. You can override the auto-generated descriptions from the `sys_documentation` table and add usage instructions that guide query construction.

This procedure uses the Semantic Column Configuration table. Customizations made this way can be transferred between instances via update sets and override descriptions and usage instructions set directly in the Dimension table. For simpler, single-instance testing, you can edit the Semantic Label and Semantic Usage Instructions fields directly in the Dimension \[sn\_query\_gen\_dimension\] table instead. Such changes might be overridden by changes to the Dimension table included in a plugin upgrade.

Use column configuration when you want to provide custom descriptions, add usage instructions for query guidance, or deactivate specific columns without removing the entire table from the semantic layer.

## Procedure

1.  Navigate to **Query Generation** &gt; **Semantic Column Configuration**.

2.  Select **New**.

3.  In the Semantic Column Configuration form, fill in the following information.

    |Field|Description|
    |-----|-----------|
    |Table Name|The table the column belongs to. Must have an active entity in the semantic layer.|
    |Column Name|The column to configure. Use the database column name, not the display label.|
    |Semantic Description|Custom description of what the column represents in business terms. Overrides the auto-generated description from `sys_documentation`. Maximum 2,000 characters.|
    |Semantic Usage Instructions|Guidance to AI on how to use this column during query generation. Include preferred operators, expected value formats, and filtering behavior. Maximum 2,000 characters.|
    |Active|Whether the column configuration is applied. When cleared, the column falls back to auto-generated state.|

4.  Select **Submit**.

    The system automatically syncs the configuration to the corresponding dimension record in the semantic layer.


## Result

The custom column configuration is active and will be used by Query Generation when processing queries that involve this column. Because this customization is stored in the Semantic Column Configuration table, it can be included in an update set and transferred to other instances. For more information, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md).

## Column configurations

The following examples show effective column descriptions and usage instructions:

|Column|Type|Semantic Description|Usage Instructions|
|------|----|--------------------|------------------|
|`creation_type`|Choice|Indicates how the dataset was produced. Values: 'Curated' \(hand-selected\), 'Derived' \(transformed from existing datasets\), 'Synthetic' \(artificially generated\).|Leave empty — choice values are auto-populated by the system|
|`dataset_creation_date`|Date|The date the dataset itself was originally created or compiled, independent of when the asset record was added to the instance.|Use date operators \(&gt;=, &lt;=, BETWEEN\) with YYYY-MM-DD format.|
|`base_datasets`|Reference|A list of other AI dataset assets this dataset is derived from or built upon, representing dataset lineage.|Reference field. Use IS EMPTY to find original/root datasets. Use IS NOT EMPTY to find derived datasets.|

## What to do next

Test your column configuration by asking questions that involve this field in Query Generation and verifying that the correct filters are generated.

**Parent Topic:**[Customizing semantic metadata](../concept/customize-semantic-metadata.md)


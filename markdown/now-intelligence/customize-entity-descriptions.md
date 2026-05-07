---
title: Customize entity descriptions for the semantic layer
description: Create custom entity descriptions in the Semantic Table Configuration table so that customizations can be transferred between instances via update sets.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 2
keywords: [semantic layer, entity descriptions, table descriptions, query generation, Semantic Table Configuration, update sets]
breadcrumb: [Customizing semantic metadata, Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Customize entity descriptions for the semantic layer

Create custom entity descriptions in the Semantic Table Configuration table so that customizations can be transferred between instances via update sets.

## Before you begin

Role required: sn\_query\_gen.admin or higher

## About this task

The Query Generation semantic layer uses natural-language descriptions to help AI understand what each table represents. By default, descriptions are auto-derived from the Field Label \[sys\_documentation\] table, but you can override these descriptions with custom descriptions that better explain the business purpose of your tables. When you clear a custom description, the system falls back to the Field Label value.

This procedure uses the Semantic Table Configuration table. Customizations made this way can be transferred between instances via update sets and override descriptions set directly in the Entity table. For simpler, single-instance testing, you can edit the Semantic Description field directly in the Entity \[sn\_query\_gen\_entity\] table instead.

**Note:** Entity labels and entity-level usage instructions can only be set in the Entity \[sn\_query\_gen\_entity\] table. The Semantic Table Configuration table supports entity descriptions only.

## Procedure

1.  Navigate to **Query Generation** &gt; **Semantic Table Configuration**.

2.  Open the record for your table, or create a record if one does not exist.

    If creating a new record, set **Table Name** to your table name and **Enable Semantic Generation** to selected. For more information, see [Add a table to the semantic data layer](../../par-for-workspace/task/add-table-semantic-layer.md#).

3.  In the **Entity Semantic Description** field, enter your custom description.

    Maximum 4,000 characters. Write the description in plain business language that explains what the table represents, who uses it, and its business purpose.

4.  Select **Update**.

    The system automatically syncs the custom description to the entity record in the semantic layer.


## Result

The custom entity description is active and will be used by Query Generation when processing queries for this table. Because this customization is stored in the Semantic Table Configuration table, it can be included in an update set and transferred to other instances. For more information, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Entity descriptions

This example shows the difference between auto-generated and custom descriptions:

<table><thead><tr><th>

Table

</th><th>

Auto-generated \(poor\)

</th><th>

Custom \(good\)

</th></tr></thead><tbody><tr><td>

incident

</td><td>

Incident table

</td><td>

IT incidents, outages, service disruptions, and IT support tickets

</td></tr><tr><td>

`alm_ai_digital_asset`

</td><td>

Tracks records for AI digital assets.

</td><td>

Base inventory table for all AI-related digital assets within the AI Control Tower \(AICT\) governance framework. Each record represents an AI artifact — model, prompt, dataset, skill, agent, or tool — tracked for governance, compliance, and lifecycle management. Governance teams, product managers, and AI platform owners use this table for centralized AI inventory oversight, audit readiness, and traceability.

</td></tr></tbody>
</table>## What to do next

Test your custom description by asking questions about the table in Query Generation and verifying that the correct table is selected.

**Parent Topic:**[Customizing semantic metadata](../concept/customize-semantic-metadata.md)


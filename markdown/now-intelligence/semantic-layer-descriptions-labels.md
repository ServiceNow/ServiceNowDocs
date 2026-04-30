---
title: Semantic descriptions and labels
description: Semantic descriptions and labels are the primary fields that AI search uses to select the right table or field. Edit these fields when the system selects incorrect tables or fields.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 1
keywords: [semantic descriptions, semantic labels, AI search, entities, dimensions]
breadcrumb: [Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Semantic descriptions and labels

Semantic descriptions and labels are the primary fields that AI search uses to select the right table or field. Edit these fields when the system selects incorrect tables or fields.

Every entity has a Semantic Description and every dimension has a Semantic Label. These fields function as search keywords that help AI search identify the correct table or field.

## When to edit descriptions and labels

Edit semantic descriptions and labels when:

-   The system selects the wrong table or cannot find one
-   A field is missing or the wrong field is selected
-   Your organization uses different terminology than the auto-generated labels

**Note:** Descriptions and labels are auto-generated and work well in their baseline state. Only edit them if selections are wrong. There are thousands of dimensions, so do not try to review them all.

## Where to edit descriptions and labels

Descriptions and labels for tables are in the Entity \[sn\_query\_gen\_entity\] table. Descriptions and labels for columns/fields are in the Dimension \[sn\_query\_gen\_dimension\] table. To edit these tables, you must have the sn\_query\_gen.admin role or higher.

## Writing effective descriptions and labels

Follow these guidelines when writing semantic descriptions and labels:

-   Keep descriptions to 1-2 sentences focused on how users refer to this data
-   Include common synonyms and abbreviations your users would say
-   Avoid full paragraphs. Concise descriptions match better than verbose ones

## Example

For an Incident entity, instead of using just "Incident table", use a description like "IT incidents, outages, service disruptions, and IT support tickets" to include terminology your users actually say.

**Parent Topic:**[Tuning the semantic layer](semantic-layer-tuning-overview.md)

**Related topics**  


[Roles, tables, and scheduled jobs included with Query Generation](../../par-for-workspace/concept/tables-sched-jobs-query-gen.md)


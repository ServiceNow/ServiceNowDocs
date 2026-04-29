---
title: Query Generation Health page
description: The health page shows the state of the Now LLM and AI Search, along with the states of Query Generation system properties, enabled products, and dependency plugins.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Query Generation Health page

The health page shows the state of the Now LLM and AI Search, along with the states of Query Generation system properties, enabled products, and dependency plugins.

## Health page overview

Navigate to **All** &gt; **Query Generation** &gt; **Health page** to see the state of Query Generation dependencies. The admin role is required.

![Health page showing Query Generation dependencies.](../image/querygen-health-page.png)

## Guide to sections

<table id="table_i22_xjq_x3c"><thead><tr><th>

Section

</th><th>

Description

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Entitlement status

</td><td>

Whether all the product entitlements for Query Generation and related products are present

</td><td>

If the status is not `Active`, contact Now Support about your licensing.

</td></tr><tr><td>

LLM and AIS status

</td><td>

The state of Query Generation skills and the LLMs they use. Also the state of AI Search

</td><td>

For Query Generation skills, if any are inactive, navigate to Now Assist Admin. Activate skills there as described in [Query Generation skills](../task/enable-query-generation.md). If you have error messages, contact Now Support.For AI Search, consult your organization's AI Search administrators.

</td></tr><tr><td>

System properties

</td><td>

The state of relevant system properties that can be modified by an administrator and that exist on the sys\_properties table

</td><td>

Navigate to the Properties \[sys\_properties\] table and change the value of the property in question. Update only the required properties that start with sn\_query\_gen. \*\*

</td></tr><tr><td>

Query Generation components

</td><td>

The health of the various Query Generation components

</td><td>

If there are no components present,run the Generate Semantic Layer job.If requests fail with `No entities and dimensions` errors, but the components are present in the entities and dimensions table and active, re-index the components.

</td></tr><tr><td>

Plugins

</td><td>

State of the plugins that are required to operate Query Generation

</td><td>

You might have to reinstall a plugin.

</td></tr><tr><td>

Query Generation enabled products

</td><td>

Installed products that use Query Generation and their statusThe Now Assist Explorer entry refers to AI Data Explorer.

</td><td>

You might have to reactivate the skill or upgrade the product.

</td></tr></tbody>
</table>**Parent Topic:**[Tuning the semantic layer](../../ai-data-explorer/concept/semantic-layer-tuning-overview.md)


---
title: Plugins installed with Service Test Management
description: Review the plugins that Service Test Management requires and the optional plugins that add characteristics, test decomposition, and conditional test groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-requirements.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [service test management plugins, requirements, product model, product inventory]
breadcrumb: [Getting started with Service Test Management, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Plugins installed with Service Test Management

Review the plugins that Service Test Management requires and the optional plugins that add characteristics, test decomposition, and conditional test groups.

## Required plugins

|Plugin ID|Description|
|---------|-----------|
|com.sn\_appss|Provides the application services that Service Test Management depends on.|
|com.sn\_tmt\_core|Provides the shared telecommunications, media, and technology framework.|

## Optional plugins

<table id="table_stm_req_optional"><thead><tr><th>

Plugin

</th><th>

Plugin ID

</th><th>

What it adds

</th></tr></thead><tbody><tr><td>

Product Model

</td><td>

com.sn\_prd\_pm

</td><td>

Adds characteristics on test definitions and test groups, characteristic mapping, test decomposition rules, test group characteristic runs, and the **Specification** field on a test group relationship.

 Without this plugin, a test group relationship uses a product model only.

</td></tr><tr><td>

Product Inventory

</td><td>

com.sn\_prd\_invt

</td><td>

Adds the **Product inventory table** and **Conditions** fields on a test group relationship, so that a test group applies only to product inventory records that meet the conditions.

</td></tr></tbody>
</table>## Relationship with Customer Service Problem Management

You can install Service Test Management without Customer Service Problem Management \(CSPM\). CSPM requires Service Test Management.

CSPM provides the API that external systems use to send test runs, test measures, threshold rule violations, and applied consequences. For details, see [Related Customer Service Problem Management information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-related-cspm-information.md).


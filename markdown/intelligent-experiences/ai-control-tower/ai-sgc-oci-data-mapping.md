---
title: Data mapping for AI Service Graph Connector for OCI
description: The AI Service Graph Connector for OCI uses separate data sources and staging tables for each asset type, per service. The staged data is transformed and loaded into target CMDB tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-sgc-oci-data-mapping.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [OCI, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Data mapping for AI Service Graph Connector for OCI

The AI Service Graph Connector for OCI uses separate data sources and staging tables for each asset type, per service. The staged data is transformed and loaded into target CMDB tables.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for OCI.

<table id="table_ex4_mvz_5jc" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td colspan="3">

Generative AI Service \(Model Track\)

</td></tr><tr><td>

SG-OCIGenAI-Model

</td><td>

sn\_ai\_oci\_disc\_ai\_model

</td><td>

cmdb\_ai\_model\_product\_modelalm\_ai\_model\_digital\_asset

cmdb\_ci\_ai\_model\_deployment

cmdb\_rel\_asset\_ci

</td></tr><tr><td colspan="3">

Generative AI Agents Service \(Agent Track\)

</td></tr><tr><td>

SG-OCIGenAIAgents-Model

</td><td>

sn\_ai\_oci\_disc\_ai\_agent\_model

</td><td>

cmdb\_ai\_model\_product\_modelalm\_ai\_model\_digital\_asset

cmdb\_ci\_ai\_model\_deployment

cmdb\_rel\_asset\_ci

</td></tr><tr><td>

SG-OCIGenAIAgents-System

</td><td>

sn\_ai\_oci\_disc\_ai\_system

</td><td>

cmdb\_ai\_system\_component\_product\_modelalm\_ai\_system\_digital\_asset

cmdb\_ci\_function\_ai

cmdb\_rel\_asset\_ci

</td></tr><tr><td>

SG-OCIGenAIAgents-Prompt

</td><td>

sn\_ai\_oci\_disc\_ai\_prompt

</td><td>

cmdb\_ai\_prompt\_product\_modelalm\_ai\_prompt\_digital\_asset

</td></tr><tr><td>

SG-OCIGenAIAgents-Tool

</td><td>

sn\_ai\_oci\_disc\_ai\_tool

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SG-OCIGenAIAgents-SystemSubcomponentM2M

</td><td>

sn\_ai\_oci\_disc\_ai\_system\_subcomponent\_m2m

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td></tr><tr><td>

SG-OCIGenAIAgents-Usage

</td><td>

sn\_ai\_oci\_disc\_ai\_usage

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr></tbody>
</table>
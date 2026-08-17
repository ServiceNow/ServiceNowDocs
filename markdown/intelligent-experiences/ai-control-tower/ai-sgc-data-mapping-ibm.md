---
title: Data mapping for AI Service Graph Connector for IBM
description: The AI Service Graph Connector for IBM uses separate data sources and staging tables for each asset type, per service. The staged data is transformed and loaded into target CMDB tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-sgc-data-mapping-ibm.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [IBM, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Data mapping for AI Service Graph Connector for IBM

The AI Service Graph Connector for IBM uses separate data sources and staging tables for each asset type, per service. The staged data is transformed and loaded into target CMDB tables.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for IBM.

<table id="table_ex4_mvz_5jc" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td colspan="3">

IBM Watsonx Runtime

</td></tr><tr><td>

SG-IBMRuntime-Agent

</td><td>

SG-IBMRuntime-Agent \[sn\_ai\_ibm\_disc\_runtime\_ai\_agent\]

</td><td>

alm\_ai\_system\_digital\_assetcmdb\_ci\_function\_ai

cmdb\_rel\_asset\_ci

cmdb\_ai\_system\_component\_product\_model

</td></tr><tr><td>

SG-IBMRuntime-Prompt

</td><td>

SG-IBMRuntime-Prompt \[sn\_ai\_ibm\_disc\_runtime\_ai\_prompt\]

</td><td>

alm\_ai\_prompt\_digital\_assetcmdb\_ai\_prompt\_product\_model

</td></tr><tr><td>

SG-IBMRuntime-Model

</td><td>

SG-IBMRuntime-Model \[sn\_ai\_ibm\_disc\_runtime\_ai\_model\]

</td><td>

alm\_ai\_model\_digital\_assetcmdb\_ai\_model\_product\_model

cmdb\_ci\_ai\_model\_deployment

cmdb\_rel\_asset\_ci

</td></tr><tr><td colspan="3">

IBM Watson Orchestrate

</td></tr><tr><td>

SG-IBMOrchestrate-System

</td><td>

SG-IBMOrchestrate-System \[sn\_ai\_ibm\_disc\_orchestrate\_ai\_system\]

</td><td>

alm\_ai\_system\_digital\_assetcmdb\_ci\_function\_ai

cmdb\_rel\_asset\_ci

cmdb\_ai\_system\_component\_product\_model

</td></tr><tr><td>

SG-IBMOrchestrate-Tool

</td><td>

SG-IBMOrchestrate-Tool \[sn\_ai\_ibm\_disc\_orchestrate\_ai\_tool\]

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SG-IBMOrchestrate-Prompt

</td><td>

SG-IBMOrchestrate-Prompt \[sn\_ai\_ibm\_disc\_orchestrate\_ai\_prompt\]

</td><td>

alm\_ai\_prompt\_digital\_assetcmdb\_ai\_prompt\_product\_model

</td></tr><tr><td>

SG-IBMOrchestrate-Model

</td><td>

SG-IBMOrchestrate-Model \[sn\_ai\_ibm\_disc\_orchestrate\_ai\_model\]

</td><td>

alm\_ai\_model\_digital\_assetcmdb\_ai\_model\_product\_model

</td></tr><tr><td>

SG-IBMOrchestrate-Usage

</td><td>

SG-IBMOrchestrate-Usage \[sn\_ai\_ibm\_disc\_orchestrate\_ai\_usage\]

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

SG-IBMOrchestrate-SystemSubcomponentM2M

</td><td>

SG-IBMOrchestrate-SystemSubcomponentM2M \[sn\_ai\_ibm\_disc\_orchestrate\_ai\_system\_subcomponent\_m2m\]

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td></tr></tbody>
</table>
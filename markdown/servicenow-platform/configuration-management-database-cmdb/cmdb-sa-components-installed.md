---
title: Components installed with CMDB success advisor
description: Several types of components are installed with activation of the CMDB success advisor plugin, including tables and scheduled jobs.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with CMDB success advisor

Several types of components are installed with activation of the CMDB success advisor plugin, including tables and scheduled jobs.

## Scheduled jobs installed

<table id="table_f5b_q5v_f2c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB success advisor data collection for HAM

</td><td>

Identifies Hardware Asset Management CI records and collects data for their corresponding indicators.

</td></tr></tbody>
</table>## Tables installed

<table id="table_kt1_hhq_ybc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB Advisor CI attribute coverage

 \[sn\_cmdb\_advisor\_ci\_attribute\_coverage\]

</td><td>

Details of configuration item \(CI\) attributes for a specific ingestion source, version, CI class, and selected attributes in CMDB success advisor using a Service Graph Connector or Discovery pattern.

</td></tr><tr><td>

CMDB Advisor Content Template

 \[sn\_cmdb\_advisor\_content\_template\]

</td><td>

Product-specific model categories used by CMDB success advisor to generate data quality insights.

</td></tr><tr><td>

CMDB Advisor settings

 \[sn\_cmdb\_advisor\_settings\]

</td><td>

Details of CMDB success advisor settings, including product association, access roles, and remediation guidance.

</td></tr><tr><td>

CMDB Advisor suggested attribute

 \[sn\_cmdb\_advisor\_suggested\_attribute\]

</td><td>

Attribute suggestions for CMDB success advisor based on the selected product and CI class context.

</td></tr><tr><td>

CMDB Advisor suggested ingestion source

 \[sn\_cmdb\_advisor\_suggested\_ingestion\_source\]

</td><td>

Ingestion source suggestions for CMDB success advisor based on the associated Service Graph Connectors, Discovery patterns, and product.

</td></tr><tr><td>

CMDB Advisor targeted product

 \[sn\_cmdb\_advisor\_targeted\_product\]

</td><td>

Targeted product definitions for CMDB success advisor, including icon, display name, and display order.

</td></tr></tbody>
</table>**Parent Topic:**[CMDB success advisor reference](../concept/cmdb-sa-reference.md)


---
title: Components installed with CMDB success advisor
description: Several types of components are installed with activation of the CMDB success advisor plugin, including tables and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-components-installed.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
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

**CMDB Advisor - Auto Setup**

</td><td>

On-demand scheduled job that automatically configures the Data Foundations advisor dashboard on first install or upgrade. Applies the recommended principal class scope, creates the content template, and triggers initial data collection. Runs only when setup is not yet complete.

</td></tr><tr><td>

**CMDB Advisor - Check Job Completion and Notify**

</td><td>

Periodically checks whether Performance Analytics data collector jobs have completed after auto-setup, and sends dashboard-ready notifications to users with the sn\_cmdb\_admin role. Activates automatically when auto-setup completes and deactivates itself once it sends all product notifications.

</td></tr><tr><td>

**CMDB Advisor - DF Daily Data Collection**

</td><td>

Runs daily to refresh pre-aggregated indicator data for the Data Foundations product and invoke the Performance Analytics data collector jobs. Populates the charts and metrics on the Data Foundations advisor dashboard.

</td></tr><tr><td>

**CMDB Advisor - HAM Daily Data Collection**

</td><td>

Runs daily to refresh pre-aggregated indicator data for the Hardware Asset Management \(HAM\) product and invoke the Performance Analytics data collector jobs. Populates the charts and metrics on the HAM advisor dashboard.

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

Scope configuration for each product dashboard, storing principal classes or model categories used by CMDB success advisor to generate data quality insights. The default value is 200.

**Note:** Increasing the value might impact the performance.

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

</td></tr><tr><td>

CMDB Advisor Aggregate Data

 \[sn\_cmdb\_advisor\_aggregate\_data\]

</td><td>

Stores pre-aggregated indicator data to populate charts and metrics on the advisor dashboards. Groups CI counts by principal class, discovery source, or model category for each active product. Records follow a draft, ready, and retired state life cycle.

</td></tr><tr><td>

CMDB Advisor Notification

 \[sn\_cmdb\_advisor\_notification\]

</td><td>

Stores dashboard-ready notifications for users with the sn\_cmdb\_admin role when data collection completes after auto-setup. Each record stores the recipient, notification content, and an action link to the relevant advisor dashboard. The **CMDB Advisor - Check Job Completion and Notify** scheduled job creates each record.

</td></tr><tr><td>

CMDB Advisor selected context

 \[sn\_cmdb\_advisor\_selected\_context\]

</td><td>

Scope selections for each product dashboard, including principal classes in the Data Foundations advisor scope and model categories in the HAM advisor scope. Each record stores the product, associated content template, selected context item, context table, and whether the selection is manual or automatic.

</td></tr></tbody>
</table>**Parent Topic:**[CMDB success advisor reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-reference.md)


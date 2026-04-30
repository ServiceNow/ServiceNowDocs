---
title: SAFe-EAP migration request form
description: Learn about the fields of SAFe-EAP migration form. Use this form to submit a request to migrate Scaled Agile Framework data to Enterprise Agile Planning.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# SAFe-EAP migration request form

Learn about the fields of SAFe-EAP migration form. Use this form to submit a request to migrate Scaled Agile Framework data to Enterprise Agile Planning.

<table id="table_gbz_xtl_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request name

</td><td>

A unique name for the migration request.

</td></tr><tr><td>

EAP configuration

</td><td>

Configuration in EAP that matches with your SAFe configuration.For example, if you're using Portfolio SAFe in your ServiceNow instance, select **Portfolio configuration**.

</td></tr><tr><td>

SAFe table

</td><td>

Data from the SAFe table that you want to migrate to EAP.-   If you select **Portfolio**, the data from SAFe Portfolio tables, their immediate child ARTs, SAFe teams, and the iterations and work items associated with them will be migrated.
-   If you select **ART**, the data from ART tables, their parent Portfolios, child SAFe teams, and the iterations and work items associated with them will be migrated.

</td></tr><tr><td>

Filter records

</td><td>

SAFe portfolios/ARTs that match the filter conditions will be displayed for selection.

</td></tr><tr><td>

Records available for migration

</td><td>

Records that match the filter conditions that you applied in the previous field are displayed in the Available list for you to choose from.Only the records that are moved to the Selected list are considered for migration.

</td></tr><tr><td>

PIs starting on or after

</td><td>

Program Increments with planned start date falling on or after the selected date are migrated.

</td></tr><tr><td>

Work items update after

</td><td>

Epics, Features and Stories updated after the selected date are migrated.

</td></tr><tr><td>

Status

</td><td>

Status of the migration request.

</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Agile Planning reference](eap-reference.md)

**Related topics**  


[Start migration of SAFe data to EAP](../task/migrate-safe-data-to-eap.md)

[Migrating from SAFe to EAP](../concept/migrating-from-safe-to-eap.md)


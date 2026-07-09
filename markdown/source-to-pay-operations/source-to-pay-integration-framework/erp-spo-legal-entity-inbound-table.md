---
title: Legal Entity Stage inbound staging table
description: The Legal entity stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table temporarily stores important data about legal entities before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-legal-entity-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Legal Entity Stage inbound staging table

The Legal entity stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table temporarily stores important data about legal entities before this data is sent to the primary table.

The following table lists the fields for the Legal Entity Stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table.

<table id="table_erp_spo_legal_entity_inbound_table"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

City

</td><td>

String

</td><td>

City where the legal entity is located.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Country where the legal entity is located.

</td></tr><tr><td>

ERP company code

</td><td>

String

</td><td>

Company code of the supplier in the ERP system.This is a mandatory field.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.This is a mandatory field.

</td></tr><tr><td>

Global company

</td><td>

String

</td><td>

Global company that the entity is linked to.

</td></tr><tr><td>

Industry

</td><td>

String

</td><td>

Industry type of the legal entity.

</td></tr><tr><td>

Legal name

</td><td>

String

</td><td>

Legal name of the entity that corresponds to its operating location.

</td></tr><tr><td>

Local currency

</td><td>

String

</td><td>

Local currency that corresponds to the entity's operating location.

</td></tr><tr><td>

Street

</td><td>

String

</td><td>

Street where the legal entity is located.

</td></tr></tbody>
</table>
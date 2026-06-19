---
title: Legal entity
description: Field descriptions for the \[sn\_fin\_legal\_entity\] table, which stores internal legal entities that request purchases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/legal-entity.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, finance automation]
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Legal entity

Field descriptions for the \[sn\_fin\_legal\_entity\] table, which stores internal legal entities that request purchases.

## sn\_fin\_legal\_entity table

The table refers to internal legal entity that requests for purchase.

<table id="table_zjb_j32_1yb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Legal name

</td><td>

String

</td><td>

Legal name of the entity corresponding to the location in which it operates.

</td></tr><tr><td>

ERP company code

</td><td>

String

</td><td>

Company code of the entity in the ERP system.

</td></tr><tr><td>

Region

</td><td>

Choice list

</td><td>

Area of the entity. The values are: -   AMS
-   APAC
-   LATAM
-   EMEA

</td></tr><tr><td>

Local currency

</td><td>

Reference

</td><td>

Local currency of the entity.

</td></tr><tr><td>

Reporting currency

</td><td>

Reference

</td><td>

Reporting currency of the entity.

</td></tr></tbody>
</table>**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)


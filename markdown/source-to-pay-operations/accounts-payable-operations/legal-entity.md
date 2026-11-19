---
title: Legal entity
description: View the legal entity corresponding to a purchase.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/legal-entity.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Legal entity

View the legal entity corresponding to a purchase.

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
</table>**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)


---
title: Third-party Registration outbound staging table
description: The Third-party Registration \[sn\_spend\_intg\_third\_party\_registration\] outbound staging table stores important data about the third-party registrations created so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables Sourcing Procurement, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Third-party Registration outbound staging table

The Third-party Registration \[sn\_spend\_intg\_third\_party\_registration\] outbound staging table stores important data about the third-party registrations created so that an ERP integrator can export this data to a third-party ERP system.

## Third-party Registration outbound staging table

The following table lists the key fields for the Third-party Registration \[sn\_spend\_intg\_third\_party\_registration\] outbound staging table.

<table id="table_n1l_1ts_pcc"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow multi location order

</td><td>

Boolean

</td><td>

Supplier allows orders to be split for multi-location shipping.

</td></tr><tr><td>

Allow purchase order revision

</td><td>

Boolean

</td><td>

Supplier allows purchase orders to be revised after confirmation.

</td></tr><tr><td>

Customer id

</td><td>

String

</td><td>

Unique identifier for the customer.

</td></tr><tr><td>

Import availability update

</td><td>

Boolean

</td><td>

Supplier is allowed to import availability updates.

</td></tr><tr><td>

Import catalog

</td><td>

Boolean

</td><td>

Supplier is allowed to import catalog, which includes price and availability.

</td></tr><tr><td>

Import invoice

</td><td>

Boolean

</td><td>

Supplier is allowed to import invoices.

</td></tr><tr><td>

Import price update

</td><td>

Boolean

</td><td>

Supplier is allowed to import price updates.

</td></tr><tr><td>

Import shipment

</td><td>

Boolean

</td><td>

Supplier is allowed to import shipments.

</td></tr><tr><td>

Post order

</td><td>

Boolean

</td><td>

Supplier is allowed to post orders.

</td></tr><tr><td>

Provider name

</td><td>

String

</td><td>

Unique identifier for the supplier.

</td></tr><tr><td>

Punchout connection type

</td><td>

String

</td><td>

Punchout connection type:-   Start URL: Outbound URL to start punchout purchases.
-   Order request URL: Outbound URL to request orders.
-   Order confirmation URL: Inbound URL for order confirmation data from the third-party site.
-   Shipping confirmation URL: Inbound URL for shipping confirmation data from the third-party site.

</td></tr><tr><td>

Punchout connection url

</td><td>

URL

</td><td>

Unique URLs for the punchout group members with punchout credentials, specifically for Start URL and Order request URL connection types.

</td></tr><tr><td>

Punchout credentials

</td><td>

Reference

</td><td>

Unique set of credentials for punchout group members.

</td></tr><tr><td>

Punchout group

</td><td>

Reference

</td><td>

Users or members involved with this punchout supplier group, including shoppers, procurement specialists, and approvers.

</td></tr><tr><td>

Supplier

</td><td>

Reference

</td><td>

Name of the supplier in the ServiceNow records.

</td></tr></tbody>
</table>
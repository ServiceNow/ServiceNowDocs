---
title: Reference data synchronization
description: For a successful integration of Coupa with Software Asset Management, you must synchronize the following reference data types on both the ServiceNow Procurement application and Coupa.
locale: en-US
release: zurich
product: Procurement
classification: procurement
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a requisition on Coupa through Procurement application, Integrating with Coupa, Integrating with external procurement applications, Procurement, IT Asset Management]
---

# Reference data synchronization

For a successful integration of Coupa with Software Asset Management, you must synchronize the following reference data types on both the ServiceNow Procurement application and Coupa.

|Coupa Requisition field|ServiceNow Procurement Purchase Order field|Description|
|-----------------------|-------------------------------------------|-----------|
|Requested by|Requested by|The email address that is associated with the Requested by record is used to find the corresponding reference record in Coupa.|

<table id="table_jdh_cpf_twb"><thead><tr><th>

Coupa Requisition Line fields

</th><th>

ServiceNow Procurement Purchase Order Line Item fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Supplier

</td><td>

Vendor

</td><td>

The supplier or vendor from which the software product should be ordered.

</td></tr><tr><td>

unit-price

</td><td>

Cost

</td><td>

The cost or price of a single product model, including discounts.

</td></tr><tr><td>

Currency

</td><td>

Cost

</td><td>

Currency is a reference field on Coupa. For a successful integration, verify that the currency codes on Coupa and ServiceNow match.

</td></tr><tr><td>

Item

</td><td>

Catalog Item

</td><td>

The Coupa items and ServiceNow Procurement catalog items must share the same display name. **Note:** This field is only used for catalog requests.

</td></tr><tr><td>

Description

</td><td>

Product Model

</td><td>

The model of the purchase order line item. **Note:** This field is only used for non-catalog requests.

</td></tr></tbody>
</table>
---
title: Purchase order lines
description: Purchase order lines provide information of the individual lines under a purchase requisition or a sourcing request for the referenced supplier.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Master data table for Accounts Payable Operations, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Purchase order lines

Purchase order lines provide information of the individual lines under a purchase requisition or a sourcing request for the referenced supplier.

## sn\_shop\_purchase\_order\_line table

You can add or associate a purchase order with a purchase order line.

<table id="table_dzw_yl1_1yb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase order

</td><td>

Reference

</td><td>

ERP PO number as unique identifier of the purchase order.

</td></tr><tr><td>

Supplier

</td><td>

Reference

</td><td>

Supplier for which the shopper places the order.

</td></tr><tr><td>

Product name

</td><td>

String

</td><td>

Name of the product or service purchased from a supplier.

</td></tr><tr><td>

Product type

</td><td>

Choice list

</td><td>

Defines whether product purchased is classified as goods or services. The values are:-   Good
-   Service
-   Handling fee

</td></tr><tr><td>

Goods receipt required

</td><td>

Choice list

</td><td>

Applicable only if product type is “Good”. The values are: -   Yes
-   No

</td></tr><tr><td>

Acknowledgement type

</td><td>

Choice list

</td><td>

Applicable only if product type is “Service” or “Handling fee”. The values are: -   Milestones
-   Service acknowledgement
-   Two way match

</td></tr><tr><td>

Expected delivery date

</td><td>

Date

</td><td>

Applicable only if product type is “Good".

</td></tr><tr><td>

ERP line number

</td><td>

String

</td><td>

A unique identifier generated within an ERP system for the purchase order line.

</td></tr><tr><td>

Start date

</td><td>

Date

</td><td>

The date on which service is expected to be rendered. This is applicable only if Product type is “Service”.

</td></tr><tr><td>

End date

</td><td>

Date

</td><td>

The date on which service is expected to end. This is applicable only if Product type is “Service”.

</td></tr><tr><td>

Purchase quantity

</td><td>

String

</td><td>

The quantity of the goods or service purchased.

</td></tr><tr><td>

Unit

</td><td>

Choice list

</td><td>

The unit of rate at which product or service is sold by supplier. The values are: -   Fixed fee
-   Individual unit

</td></tr><tr><td>

Unit price

</td><td>

currency

</td><td>

The price of each individual unit purchased.

</td></tr><tr><td>

Total line amount

</td><td>

currency

</td><td>

Total amount of purchased goods and services including estimated tax and shipping.

</td></tr><tr><td>

Recipient

</td><td>

Reference

</td><td>

The person to whom goods or services are being delivered.

</td></tr><tr><td>

Address

</td><td>

 

</td><td>

Street address where goods will be shipped or where services will be provided.

</td></tr><tr><td>

City

</td><td>

 

</td><td>

City where goods will be shipped or where the services are provided.

</td></tr><tr><td>

State or Province

</td><td>

 

</td><td>

State or Province where goods will be shipped or where the services are provided.

</td></tr><tr><td>

Country

</td><td>

 

</td><td>

Country where goods will be shipped or where the services are provided.

</td></tr><tr><td>

Zip or Postal code

</td><td>

 

</td><td>

Zip or Postal code where goods will be shipped or where the services are provided.

</td></tr><tr><td>

General Ledger Account

</td><td>

 

</td><td>

The account to which capital or operational expenses will be posted.

</td></tr></tbody>
</table>**Parent Topic:**[Master data table for Accounts Payable Operations](master-data-table-apo.md)


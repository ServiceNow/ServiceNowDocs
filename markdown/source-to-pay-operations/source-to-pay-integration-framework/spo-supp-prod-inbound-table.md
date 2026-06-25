---
title: Supplier Product Stage inbound staging table
description: The Supplier Product Stage inbound \[sn\_spend\_intg\_supplier\_product\_stage\] staging table temporarily stores important data about supplier products before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/spo-supp-prod-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier Product Stage inbound staging table

The Supplier Product Stage inbound \[sn\_spend\_intg\_supplier\_product\_stage\] staging table temporarily stores important data about supplier products before this data is sent to the primary table.

The following table lists the mandatory fields for the Supplier Product Stage inbound \[sn\_spend\_intg\_supplier\_product\_stage\] staging table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capex account

</td><td>

String

</td><td>

General ledger account where capital expenses are posted on purchase.

</td></tr><tr><td>

Currency

</td><td>

String

</td><td>

Currency format associated with the supplier

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Detailed description of the product for the buyer.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source used by the organization.

</td></tr><tr><td>

Expense account

</td><td>

String

</td><td>

General ledger account where operational expenses are posted on purchases.

</td></tr><tr><td>

Goods receipt required

</td><td>

String

</td><td>

Indicates if a receipt is required in addition to the invoice.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the company that the supplier is linked to.

</td></tr><tr><td>

Prepaid account

</td><td>

String

</td><td>

General ledger account where purchases of this product are posted when they are prepaid.

</td></tr><tr><td>

Product category

</td><td>

String

</td><td>

Category to which this product belongs.

</td></tr><tr><td>

Product model

</td><td>

String

</td><td>

Standardized definition for this product across suppliers.**Note:** For creating a product bundle, enter the name of the product model of type bundle in this field.

</td></tr><tr><td>

Product type

</td><td>

String

</td><td>

Type of product. The options are Good or Service.

</td></tr><tr><td>

Published

</td><td>

String

</td><td>

Option for specifying if the product is to be listed on the ShoppingHub portal.

</td></tr><tr><td>

Services acknowledgement

</td><td>

String

</td><td>

All the service acknowledgments associated with the supplier.

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Brief description of the product for the buyer.

</td></tr><tr><td>

Sourcing required

</td><td>

Boolean

</td><td>

Option to mark if sourcing is required for this product. This is determined based on if there is an active contractual price for this supplier product or not.

</td></tr><tr><td>

Sourcing time in days

</td><td>

String

</td><td>

Estimated number of days to process the sourcing request.

</td></tr><tr><td>

Spend categorization

</td><td>

String

</td><td>

Product that is addressable for negotiation. You can select one of these options:-   Addressable: Can be considered for negotiation.
-   Not Addressable: Cannot be considered for negotiation.

</td></tr><tr><td>

Supplier

</td><td>

String

</td><td>

Name of the supplier.

</td></tr><tr><td>

Supplier delivers to

</td><td>

String

</td><td>

Countries where the suppliers can deliver the product.

</td></tr><tr><td>

Supplier part number

</td><td>

String

</td><td>

Unique number that is used by the supplier to identify this product.

</td></tr><tr><td>

Units

</td><td>

String

</td><td>

Unit or rate in which the product is sold by the supplier.

</td></tr></tbody>
</table>**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table]()

[CMDB Service Model Stage inbound staging table]()

[CMN Location Stage inbound staging table]()

[Catalog Import staging table]()

[Catalog Error staging table]()

[Cost Center Stage inbound staging table]()

[Department Stage inbound staging table]()

[ERP Plant Address Mapping Stage inbound staging table]()

[FX Currency Stage inbound staging table]()

[FX Rate Stage inbound staging table]()

[Fixed asset details stage inbound table]()

[GL Account Stage inbound staging table]()

[Import Availability Updates inbound staging table]()

[Availability Error staging table]()

[Cost Allocation inbound staging table \(Deprecated\)]()

[Invoice inbound staging table]()

[Purchase Order inbound staging table]()

[Purchase Order Line inbound staging table]()

[Receipt inbound staging table]()

[Legal Entity Stage inbound staging table]()

[Office Location Stage inbound staging table]()

[Order Acknowledgement staging table]()

[Order Acknowledgement Error staging table]()

[Payment Terms Stage inbound staging table]()

[Price Import staging table]()

[Price Error outbound staging table]()

[Product Model Stage inbound staging table]()

[Purchase Entity Stage inbound staging table]()

[Purchase Line Stage inbound staging table]()

[Purchase Requisition staging table]()

[Spend Shipment Import inbound staging table]()

[Shipment Error staging table]()

[Third Party Sourcing Registration staging table]()

[Third Party Unit Mapping staging table]()

[Third Party Unit staging table]()

[Unit of Measure inbound staging table]()


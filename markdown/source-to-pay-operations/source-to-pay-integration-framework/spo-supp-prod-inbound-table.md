---
title: Supplier Product Stage inbound staging table
description: The Supplier Product Stage inbound \[sn\_spend\_intg\_supplier\_product\_stage\] staging table temporarily stores important data about supplier products before this data is sent to the primary table.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
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
</table>**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](../concept/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table](spo-prod-cate-inbound-table.md)

[CMDB Service Model Stage inbound staging table](spo-serv-mod-inbound-table.md)

[CMN Location Stage inbound staging table](spo-loc-inbound-table.md)

[Catalog Import staging table](catalog-import-staging-table.md)

[Catalog Error staging table](catalog-error.md)

[Cost Center Stage inbound staging table](spo-cost-center-inbound-table.md)

[Department Stage inbound staging table](spo-dept-inbound-table.md)

[ERP Plant Address Mapping Stage inbound staging table](spo-erp-plant-address-inbound-table.md)

[FX Currency Stage inbound staging table](spo-fx-currency-inbound-table.md)

[FX Rate Stage inbound staging table](spo-fx-rate-inbound-table.md)

[Fixed asset details stage inbound table](fixed-asset-details-stage-inbound-table.md)

[GL Account Stage inbound staging table](spo-gl-account-inbound-table.md)

[Import Availability Updates inbound staging table](spo-import-avail-inbound-table.md)

[Availability Error staging table](availability-error-staging-table.md)

[Inbound Cost Allocation staging table](spo-cost-alloc-inbound-table.md)

[Inbound Invoice staging table](spo-inbound-invoice-table.md)

[Inbound Purchase Order staging table](spo-inbound-pur-order-table.md)

[Inbound Purchase Order Line staging table](spo-inbound-pol-table.md)

[Inbound Receipt staging table](spo-inbound-receipt-table.md)

[Legal Entity Stage inbound staging table](spo-legal-entity-inbound-table.md)

[Office Location Stage inbound staging table](spo-office-loc-inbound-table.md)

[Order Acknowledgement staging table](order-acknowledgement-staging-table.md)

[Order Acknowledgement Error staging table](order-acknowledgement-error.md)

[Payment Terms Stage inbound staging table](spo-pay-terms-inbound-table.md)

[Price Import staging table](price-import-staging-table.md)

[Price Error outbound staging table](price-error-staging-table.md)

[Product Model Stage inbound staging table](spo-prod-mod-inbound-table.md)

[Purchase Entity Stage inbound staging table](spo-purch-entity-inbound-table.md)

[Purchase Line Stage inbound staging table](spo-purch-line-stage-inbound-table.md)

[Purchase Requisition staging table](purchase-requisition-staging-table.md)

[Spend Shipment Import inbound staging table](spend-shipment-import-inbound-table.md)

[Shipment Error staging table](shipment-error-staging-table.md)

[Third Party Sourcing Registration staging table](third-party-sourcing-registration-staging-table.md)

[Third Party Unit Mapping staging table](third-party-unit-mapping-staging-table.md)

[Third Party Unit staging table](third-party-unit-staging-table.md)

[Unit of Measure inbound staging table](unit-measure-inbound-staging-table.md)


---
title: Purchase Line Stage inbound staging table
description: The Purchase Entity Stage inbound \[sn\_spend\_intg\_purchase\_line\] staging table temporarily stores important data about purchase entities before this data is sent to the primary table.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Line Stage inbound staging table

The Purchase Entity Stage inbound \[sn\_spend\_intg\_purchase\_line\] staging table temporarily stores important data about purchase entities before this data is sent to the primary table.

## Purchase Line Stage inbound staging table

The following table lists both the mandatory and optional fields for the Purchase Line Stage inbound \[sn\_spend\_intg\_purchase\_line\] staging table.

<table id="table_mq2_qrt_ncc"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account assignment category

</td><td>

String

</td><td>

Account assignment category of the purchase line.

</td></tr><tr><td>

Acknowledgement type

</td><td>

String

</td><td>

Acknowledgment type of the purchase line. Applicable only if product type is Service or Handling fee. The values are:-   Milestones
-   Service acknowledgement
-   Two way match

</td></tr><tr><td>

Active

</td><td>

String

</td><td>

Indicates if the purchase line is active or not.

</td></tr><tr><td>

Additional comments

</td><td>

String

</td><td>

Additional notes about the purchase line, if any.

</td></tr><tr><td>

Address

</td><td>

String

</td><td>

Address of the purchase line.

</td></tr><tr><td>

After the fact

</td><td>

String

</td><td>

Indicates if the purchase requisition is after the fact or not.

</td></tr><tr><td>

Asset category

</td><td>

String

</td><td>

Asset category of the purchase line.

</td></tr><tr><td>

Awarded

</td><td>

String

</td><td>

Indicates who is the awarded supplier for the purchase line.

</td></tr><tr><td>

Awarded in third party

</td><td>

String

</td><td>

Indicates who is the third-party awarded supplier for the purchase line.

</td></tr><tr><td>

Business owner

</td><td>

String

</td><td>

An individual or group who owns the purchase line.

</td></tr><tr><td>

Capex account

</td><td>

String

</td><td>

Ledger account to post the capital expenses of this product after the purchase completion.

</td></tr><tr><td>

Cart line id

</td><td>

String

</td><td>

Shopping cart line ID of the purchase line.

</td></tr><tr><td>

City

</td><td>

String

</td><td>

City of the purchase line.

</td></tr><tr><td>

Contract price

</td><td>

String

</td><td>

Contract price of the purchase line.

</td></tr><tr><td>

Cost center

</td><td>

String

</td><td>

Cost center that incurs the cost of the purchase line.

</td></tr><tr><td>

Cost plan

</td><td>

String

</td><td>

Cost plan for the purchase line.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Name of the country of the purchase line.

</td></tr><tr><td>

Country code

</td><td>

String

</td><td>

Country code of the purchase line.

</td></tr><tr><td>

Estimated shipping

</td><td>

String

</td><td>

Shipping cost estimate for the product based on the delivery location.

</td></tr><tr><td>

Estimated tax

</td><td>

String

</td><td>

Tax estimate for the product based on the price and delivery location.

</td></tr><tr><td>

Expense account

</td><td>

String

</td><td>

Expense account associated with the purchase line.

</td></tr><tr><td>

General ledger account

</td><td>

String

</td><td>

General Ledger \(GL\) account associated with the purchase line.

</td></tr><tr><td>

Goods receipt required

</td><td>

String

</td><td>

Indicates if a receipt is required in addition to the invoice.

</td></tr><tr><td>

Individual unit cost

</td><td>

String

</td><td>

Cost of the individual unit.

</td></tr><tr><td>

Internal order number

</td><td>

String

</td><td>

Internal order number of the purchase line.

</td></tr><tr><td>

Legal entity

</td><td>

String

</td><td>

Internal legal entity that incurs the cost of this purchase line.

</td></tr><tr><td>

Line source

</td><td>

String

</td><td>

Line source associated with the purchase line.

</td></tr><tr><td>

Manual handling fee

</td><td>

String

</td><td>

Manual charges added for a specific supplier when a rule is triggered as a result of certain configurable conditions for a purchase requisition being met.

</td></tr><tr><td>

Maximum budget

</td><td>

String

</td><td>

Maximum budget that the shopper provides for this purchase.

</td></tr><tr><td>

Milestone payout type

</td><td>

String

</td><td>

Indicates the type of milestone payout. The options available are Amount and Percentage.

</td></tr><tr><td>

Negotiated by

</td><td>

String

</td><td>

Indicates who is responsible for negotiation.

</td></tr><tr><td>

Negotiated savings

</td><td>

String

</td><td>

Total savings through negotiation. This is calculated as: \(Starting unit cost - Negotiated unit cost\) x Supplier's quantity.

</td></tr><tr><td>

Negotiated unit cost

</td><td>

String

</td><td>

Cost per unit of the product after negotiation.

</td></tr><tr><td>

Negotiation

</td><td>

String

</td><td>

Negotiation associated with this purchase line.

</td></tr><tr><td>

Net amount

</td><td>

String

</td><td>

Amount included as a cost allocation on the purchase order. This doesn’t include any estimates.

</td></tr><tr><td>

Non catalog purchase?

</td><td>

String

</td><td>

Indicates if the purchase is non catalog or not.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

System-generated unique identifier of the purchase line.

</td></tr><tr><td>

Parent line

</td><td>

String

</td><td>

Parent line of the purchase line.

</td></tr><tr><td>

Part requirement

</td><td>

String

</td><td>

Part requirement associated with the purchase line.

</td></tr><tr><td>

Payment allocations

</td><td>

String

</td><td>

Payment allocations of the purchase line.

</td></tr><tr><td>

Payment method

</td><td>

String

</td><td>

Indicates the payment method to the supplier.

</td></tr><tr><td>

Payment schedule

</td><td>

String

</td><td>

Indicates the schedule of payments to the supplier.

</td></tr><tr><td>

Preferred currency

</td><td>

String

</td><td>

Payment method preferred by the supplier legal entity.

</td></tr><tr><td>

Pre-paid account

</td><td>

String

</td><td>

General ledger account where purchases of this product are posted when they are prepaid.

</td></tr><tr><td>

Pre-payments required

</td><td>

String

</td><td>

Option to mark if pre-payments is required for this product.

</td></tr><tr><td>

Pricing obtained on

</td><td>

String

</td><td>

Date on which the pricing is obtained for the purchase line.

</td></tr><tr><td>

Product category

</td><td>

String

</td><td>

Product category that is sourced through this purchase line.

</td></tr><tr><td>

Product example

</td><td>

String

</td><td>

Reference URL that the shopper provides.

</td></tr><tr><td>

Product name

</td><td>

String

</td><td>

Name of the supplier product.

</td></tr><tr><td>

Product type

</td><td>

String

</td><td>

Type of the product associated with the purchase line.

</td></tr><tr><td>

Project

</td><td>

String

</td><td>

Project associated with the purchase line.

</td></tr><tr><td>

Purchase

</td><td>

String

</td><td>

Parent purchase associated with this purchase line.

</td></tr><tr><td>

Purchase order

</td><td>

String

</td><td>

Purchase order associated with the purchase line.

</td></tr><tr><td>

Purchase order line

</td><td>

String

</td><td>

Purchase order line associated with the purchase line.

</td></tr><tr><td>

Purchase reason

</td><td>

String

</td><td>

Reason for purchasing the product.

</td></tr><tr><td>

Purchase requisition

</td><td>

String

</td><td>

Purchase requisition associated with this purchase line.

</td></tr><tr><td>

Purchased quantity

</td><td>

String

</td><td>

Quantity that has been purchased by the shopper.

</td></tr><tr><td>

Recipient

</td><td>

String

</td><td>

Recipient of the purchase line.

</td></tr><tr><td>

Requested delivery date

</td><td>

String

</td><td>

Requested delivery date of the purchased product.

</td></tr><tr><td>

Requested end date

</td><td>

String

</td><td>

Requested end date of the purchase line order.

</td></tr><tr><td>

Requested start date

</td><td>

String

</td><td>

Requested start date of the purchase line order.

</td></tr><tr><td>

Shipping method

</td><td>

String

</td><td>

Details of the carrier, the applicable suppliers, and the valid delivery location countries for those suppliers.

</td></tr><tr><td>

Shopper's original choice

</td><td>

String

</td><td>

Original or first choice of the shopper.

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Brief description about the purchase line.

</td></tr><tr><td>

Sourcing request

</td><td>

String

</td><td>

Sourcing request associated with this purchase line.

</td></tr><tr><td>

Specific requirements

</td><td>

String

</td><td>

Requirements that the shopper specifies.

</td></tr><tr><td>

Spend categorization

</td><td>

String

</td><td>

Indicates whether negotiation with the supplier is addressable or not.

</td></tr><tr><td>

Starting unit cost

</td><td>

String

</td><td>

Cost per unit of the product prior to negotiation.

</td></tr><tr><td>

State

</td><td>

String

</td><td>

State of the purchase line.

</td></tr><tr><td>

State or province

</td><td>

String

</td><td>

State or province of the purchase line.

</td></tr><tr><td>

Street

</td><td>

String

</td><td>

Street address of the purchase line.

</td></tr><tr><td>

Supplier

</td><td>

String

</td><td>

Supplier for which the shopper places the order.

</td></tr><tr><td>

Supplier case

</td><td>

String

</td><td>

Indicates if a supplier case is created for the supplier or not.

</td></tr><tr><td>

Supplier contact

</td><td>

String

</td><td>

Name of the supplier contact of the purchase line.

</td></tr><tr><td>

Supplier contact email

</td><td>

String

</td><td>

Registered email ID for this supplier contact.

</td></tr><tr><td>

Supplier contact first name

</td><td>

String

</td><td>

First name of the supplier contact.

</td></tr><tr><td>

Supplier contact job title

</td><td>

String

</td><td>

Job title of the supplier contact.

</td></tr><tr><td>

Supplier contact last name

</td><td>

String

</td><td>

Last name of the supplier contact.

</td></tr><tr><td>

Supplier contacted?

</td><td>

String

</td><td>

Indicates if the supplier has been contacted or not.

</td></tr><tr><td>

Supplier notes

</td><td>

String

</td><td>

Additional notes about the supplier, if any.

</td></tr><tr><td>

Supplier part auxiliary ID

</td><td>

String

</td><td>

Auxiliary ID associated with the supplier part.

</td></tr><tr><td>

Supplier product

</td><td>

String

</td><td>

Supplier product for which the purchase line is created.

</td></tr><tr><td>

Supplier's lead time \(days\)

</td><td>

String

</td><td>

Number of days that the supplier takes to deliver the goods or provide the service. Based on this, the delivery date for goods and the start and end dates for services vary.

</td></tr><tr><td>

Supplier's quantity

</td><td>

String

</td><td>

Quantity that the supplier can provide.

</td></tr><tr><td>

Tags

</td><td>

String

</td><td>

Tag names for the purchase line.

</td></tr><tr><td>

Term length

</td><td>

String

</td><td>

Duration of the term.

</td></tr><tr><td>

Term value

</td><td>

String

</td><td>

Type of the term. The options are Days, Weeks, Months, and Years.

</td></tr><tr><td>

Third party Category

</td><td>

String

</td><td>

Third-party category of the purchase line.

</td></tr><tr><td>

Total bid amount

</td><td>

String

</td><td>

Supplier's quantity multiplied by negotiated unit cost. It reflects the total bid amount from that particular supplier for that purchase line.

</td></tr><tr><td>

Total individual units

</td><td>

String

</td><td>

Number of fixed assets that are created depends on this value.

</td></tr><tr><td>

Total line amount

</td><td>

String

</td><td>

Total price of the purchased goods and services, including estimated tax and shipping.

</td></tr><tr><td>

Type

</td><td>

String

</td><td>

Type of the purchase line.

</td></tr><tr><td>

Unit

</td><td>

String

</td><td>

Unit of rate at which the customer purchases the product.

</td></tr><tr><td>

Upcoming date

</td><td>

String

</td><td>

Upcoming date for the purchase line.

</td></tr><tr><td>

WBS element

</td><td>

String

</td><td>

WBS element associated with the purchase line.

</td></tr><tr><td>

Zip or postal code

</td><td>

String

</td><td>

Zip code of the purchase line.

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

[Purchase Requisition staging table](purchase-requisition-staging-table.md)

[Spend Shipment Import inbound staging table](spend-shipment-import-inbound-table.md)

[Shipment Error staging table](shipment-error-staging-table.md)

[Supplier Product Stage inbound staging table](spo-supp-prod-inbound-table.md)

[Third Party Sourcing Registration staging table](third-party-sourcing-registration-staging-table.md)

[Third Party Unit Mapping staging table](third-party-unit-mapping-staging-table.md)

[Third Party Unit staging table](third-party-unit-staging-table.md)

[Unit of Measure inbound staging table](unit-measure-inbound-staging-table.md)


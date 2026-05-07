---
title: Outbound Order Line staging table
description: The Outbound Order Line \[sn\_spend\_intg\_outbound\_purchase\_order\_line\] staging table stores important data about the purchase order lines created so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Outbound staging tables Sourcing Procurement, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound Order Line staging table

The Outbound Order Line \[sn\_spend\_intg\_outbound\_purchase\_order\_line\] staging table stores important data about the purchase order lines created so that an ERP integrator can export this data to a third-party ERP system.

The following table lists the key fields for the Outbound Order Line \[sn\_spend\_intg\_outbound\_purchase\_order\_line\] staging table.

**Note:** There are no mandatory fields for this table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

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

Account assignment category of the purchase order line.

</td></tr><tr><td>

Asset category

</td><td>

String

</td><td>

Asset category of the purchase order line.

</td></tr><tr><td>

City

</td><td>

String

</td><td>

City of the purchase order line.

</td></tr><tr><td>

Contract number

</td><td>

String

</td><td>

Contract number of the purchase order line.

</td></tr><tr><td>

Cost center

</td><td>

String

</td><td>

Cost center that incurs the cost of the purchase order line.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Name of the country of the purchase order line.

</td></tr><tr><td>

Enroll in ABM

</td><td>

String

</td><td>

Option to enroll the purchase order line for an Apple Business Manager \(ABM\) account.

</td></tr><tr><td>

ERP line number

</td><td>

String

</td><td>

Purchase order line number from the ERP system.

</td></tr><tr><td>

Expected delivery date

</td><td>

String

</td><td>

Expected delivery date of the purchased product.

</td></tr><tr><td>

GL account

</td><td>

String

</td><td>

General Ledger \(GL\) account associated with the purchase order line.

</td></tr><tr><td>

Integration status

</td><td>

String

</td><td>

Current status of the purchase order line integration.

</td></tr><tr><td>

Location name

</td><td>

String

</td><td>

Location of the purchase order line.

</td></tr><tr><td>

Manufacturer part number \(MPN\)

</td><td>

String

</td><td>

Manufacturer or publisher’s unique identifier for the product, which the customer desires to purchase.

</td></tr><tr><td>

Model number

</td><td>

String

</td><td>

Unique model number of the product.

</td></tr><tr><td>

Organization ID

</td><td>

String

</td><td>

Organization ID of the purchase order line.

</td></tr><tr><td>

Processing message

</td><td>

String

</td><td>

A message that describes the current processing status of the purchase order line.

</td></tr><tr><td>

Product category

</td><td>

String

</td><td>

Product category that the purchase order line belongs to.

</td></tr><tr><td>

Product name

</td><td>

String

</td><td>

Name of the product associated with the purchase order line.

</td></tr><tr><td>

Product type

</td><td>

String

</td><td>

Type of the product associated with the purchase order line.

</td></tr><tr><td>

Purchase order

</td><td>

String

</td><td>

Purchase order associated with the purchase order line.

</td></tr><tr><td>

Purchase order line number

</td><td>

String

</td><td>

Line number of the purchase order line.

</td></tr><tr><td>

Purchase order line status

</td><td>

String

</td><td>

Current status of the purchase order line.

</td></tr><tr><td>

Purchased quantity

</td><td>

String

</td><td>

Quantity purchased as part of the purchase order line.

</td></tr><tr><td>

Recipient

</td><td>

String

</td><td>

Recipient of the purchase order line.

</td></tr><tr><td>

Service end date

</td><td>

String

</td><td>

Date on which service is expected to end.This is applicable only if the Product type is Service.

</td></tr><tr><td>

Service start date

</td><td>

String

</td><td>

Date on which service is expected to be rendered.This is applicable only if the Product type is Service.

</td></tr><tr><td>

Ship to

</td><td>

String

</td><td>

Shipping location of the purchase order line.

</td></tr><tr><td>

Short text

</td><td>

String

</td><td>

Brief description about the purchase order line.

</td></tr><tr><td>

State

</td><td>

String

</td><td>

State or province of the purchase order line.

</td></tr><tr><td>

Street

</td><td>

String

</td><td>

Street address of the purchase order line.

</td></tr><tr><td>

Supplier part number

</td><td>

String

</td><td>

The supplier’s unique identifier for the product, which the customer desires to purchase.

</td></tr><tr><td>

Unit

</td><td>

String

</td><td>

Unit of rate at which the customer purchases the product.

</td></tr><tr><td>

Unit price

</td><td>

String

</td><td>

The price of each individual unit is purchased.

</td></tr><tr><td>

Unit price currency

</td><td>

String

</td><td>

The currency in which the order is placed.

</td></tr><tr><td>

Zip code

</td><td>

String

</td><td>

Zip code of the purchase order line.

</td></tr></tbody>
</table>
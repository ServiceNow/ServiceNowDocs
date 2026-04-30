---
title: Supplier inbound staging table
description: The Supplier inbound \[sn\_fcms\_intg\_imp\_supplier\] staging table temporarily stores important data about the supplier before this data is sent to the Supplier \[sn\_fin\_supplier\] primary table.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Inbound staging tables for Supplier Lifecycle Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier inbound staging table

The Supplier inbound \[sn\_fcms\_intg\_imp\_supplier\] staging table temporarily stores important data about the supplier before this data is sent to the Supplier \[sn\_fin\_supplier\] primary table.

## Supplier inbound staging table

The following table lists fields for the Supplier inbound \[sn\_fcms\_intg\_imp\_supplier\] staging table.

<table id="table_e4l_dr5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accepted purchasing currency

</td><td>

String

</td><td>

Currency value in which purchase orders for this supplier must be created.

</td></tr><tr><td>

City

</td><td>

String

</td><td>

City where the supplier is located.

</td></tr><tr><td>

Company overall rating

</td><td>

String

</td><td>

Overall rating of the company.

</td></tr><tr><td>

Company type

</td><td>

String

</td><td>

Industry type of the supplier.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Country where the supplier is located.

</td></tr><tr><td>

Country of registration

</td><td>

String

</td><td>

Country where the supplier is registered.

</td></tr><tr><td>

County / District

</td><td>

String

</td><td>

County or district where the supplier is located.

</td></tr><tr><td>

Customer number

</td><td>

String

</td><td>

Unique identifier for the organization to the supplier.

</td></tr><tr><td>

Domain

</td><td>

String

</td><td>

Domain name of the supplier.

</td></tr><tr><td>

Duns

</td><td>

String

</td><td>

Unique 9-digit identifier for a supplier.

</td></tr><tr><td>

Employee number

</td><td>

String

</td><td>

Employee number of the supplier contact.

</td></tr><tr><td>

ERP company code

</td><td>

String

</td><td>

Company code of the supplier in the ERP system.

</td></tr><tr><td>

ERP company code

</td><td>

String

</td><td>

Company code of the supplier in the ERP system.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source used by the organization.

</td></tr><tr><td>

Fax number

</td><td>

String

</td><td>

Number to which documents can be faxed to the supplier.

</td></tr><tr><td>

Founded year

</td><td>

String

</td><td>

Year the organization was founded.

</td></tr><tr><td>

General ledger account

</td><td>

String

</td><td>

Accounts payable reconciliation account for the supplier.

</td></tr><tr><td>

Goods shipped from

</td><td>

String

</td><td>

Location from where the supplier ships out the products.

</td></tr><tr><td>

Incoterm

</td><td>

String

</td><td>

Set of 11 internationally recognized rules that define the responsibilities of sellers and buyers.It specifies who is responsible for paying for and managing the shipment, insurance, documentation, customs clearance, and other logistical activities. Select one of these options:

-   Carriage and Insurance Paid to \(CIP\)
-   Carriage Paid to \(CPT\)
-   Cost and Freight \(CFR\)
-   Cost, Insurance, and Freight \(CIF\)
-   Delivered at Place \(DAP\)
-   Delivered at Terminal \(DAT\)
-   Delivered Duty Paid \(DDP\)
-   Ex Works \(EXW\)
-   Free Alongside Ship \(FAS\)
-   Free Carrier \(FCA\)
-   Free on Board \(FOB\)

</td></tr><tr><td>

Industry

</td><td>

String

</td><td>

Industry type of the supplier.

</td></tr><tr><td>

Legal entities

</td><td>

String

</td><td>

Name of the legal entity.

</td></tr><tr><td>

Legal name

</td><td>

String

</td><td>

Legal name of the supplier that corresponds to its operating location.

</td></tr><tr><td>

Locations count

</td><td>

String

</td><td>

Number of places where the supplier operates.

</td></tr><tr><td>

Logo URL

</td><td>

String

</td><td>

Image URL of the supplier’s logo.

</td></tr><tr><td>

Long description

</td><td>

String

</td><td>

Detailed description of the supplier.

</td></tr><tr><td>

Off-boarded date

</td><td>

String

</td><td>

Date of the supplier's termination from the organization.

</td></tr><tr><td>

Onboarded

</td><td>

String

</td><td>

Indicates whether the supplier is onboarded into the ERP system.

</td></tr><tr><td>

On-boarded by

</td><td>

String

</td><td>

Employee responsible for onboarding the supplier.

</td></tr><tr><td>

On-boarded date

</td><td>

String

</td><td>

Onboarding date of the supplier.

</td></tr><tr><td>

Parent company

</td><td>

String

</td><td>

Parent company of the supplier.

</td></tr><tr><td>

Payment term

</td><td>

String

</td><td>

Agreed upon time and conditions for payment to the supplier.

</td></tr><tr><td>

PO box number

</td><td>

String

</td><td>

Post office box number where the supplier correspondence and payments are made.

</td></tr><tr><td>

Posting Block

</td><td>

String

</td><td>

Postal block where the supplier is located.

</td></tr><tr><td>

Primary phone number

</td><td>

String

</td><td>

Primary phone number.

</td></tr><tr><td>

Purchasing entities

</td><td>

String

</td><td>

Purchasing entities that are allowed to purchase from the supplier.

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Brief description about the supplier.

</td></tr><tr><td>

State / Province

</td><td>

String

</td><td>

State or province where the supplier is located.

</td></tr><tr><td>

Status

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Street address

</td><td>

String

</td><td>

Street where the supplier is located.

</td></tr><tr><td>

Sustainability rating

</td><td>

String

</td><td>

The business relationship designated to the entity.

</td></tr><tr><td>

Tax id

</td><td>

String

</td><td>

Tax ID of the organization.

</td></tr><tr><td>

Tax jurisdiction

</td><td>

String

</td><td>

Taxation authority that imposes the taxes.

</td></tr><tr><td>

Twitter

</td><td>

String

</td><td>

Twitter account of the supplier.

</td></tr><tr><td>

URL

</td><td>

String

</td><td>

URL of the supplier.

</td></tr><tr><td>

Wikipedia

</td><td>

String

</td><td>

Wikipedia page of the supplier.

</td></tr><tr><td>

YouTube

</td><td>

String

</td><td>

Youtube channel of the supplier.

</td></tr><tr><td>

Zip / Postal code

</td><td>

String

</td><td>

Zip code or postal code where the supplier is located.

</td></tr></tbody>
</table>**Parent Topic:**[Inbound staging tables for Supplier Lifecycle Operations](../concept/slo-inbound-staging-tables.md)

**Related topics**  


[Supplier Contact inbound staging table](slo-supp-contact-inbound-table.md)

[Supplier Legal Entity mapping inbound staging table](slo-legal-entity-inbound-table.md)

[Supplier Location inbound staging table](slo-supp-location-inbound-table.md)

[Supplier Payment inbound staging table](slo-supp-payment-inbound-table.md)


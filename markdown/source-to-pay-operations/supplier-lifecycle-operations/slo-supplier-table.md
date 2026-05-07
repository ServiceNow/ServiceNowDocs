---
title: Supplier table
description: The Supplier \[sn\_fin\_supplier\] table stores important information about a supplier.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Primary data tables for Supplier Lifecycle Operations, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier table

The Supplier \[sn\_fin\_supplier\] table stores important information about a supplier.

## Supplier \[sn\_fin\_supplier\] table

The Supplier \[sn\_fin\_supplier\] table contains the following fields.

<table id="table_e4l_dr5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Legal Name

</td><td>

String

</td><td>

Legal name of the supplier that corresponds to its operating location.

</td></tr><tr><td>

DUNS number

</td><td>

Integer

</td><td>

Unique, 9-digit identifier for a supplier.

</td></tr><tr><td>

ERP supplier code

</td><td>

Integer

</td><td>

Company code of the supplier in the ERP system.

</td></tr><tr><td>

Parent entity

</td><td>

Reference

</td><td>

Parent organization of the supplier.

</td></tr><tr><td>

Global company

</td><td>

Reference

</td><td>

Global company that the supplier is linked to \(top-level entity of the supplier's corporate group\).**Note:** In contrast, Related company is a reference to the company record most relevant to this supplier for risk management and reporting purposes, often a child entity.

</td></tr><tr><td>

Industry

</td><td>

String

</td><td>

Industry to which the supplier belongs.

</td></tr><tr><td>

Website

</td><td>

URL

</td><td>

Website of the supplier.

</td></tr><tr><td>

Image

</td><td>

Image

</td><td>

Image of the supplier’s logo.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Detailed description of the supplier.

</td></tr><tr><td>

Relationship manager

</td><td>

String

</td><td>

Person responsible for managing the relationship with this supplier.

</td></tr><tr><td>

Relationship status

</td><td>

List

</td><td>

Business relationship that is designated to the supplier. The options are Strategic, Valued, Tactical, or Excluded.

</td></tr><tr><td>

Onboarded

</td><td>

Boolean

</td><td>

Status of whether the supplier is onboarded into the ERP system. The options are Yes or No.

</td></tr><tr><td>

Valid NDA

</td><td>

Boolean

</td><td>

Status of whether the supplier has a valid non-disclosure agreement. The options are Yes or No.

</td></tr><tr><td>

Valid risk assessment

</td><td>

Boolean

</td><td>

Status of whether a valid risk assessment has been performed for the supplier. The options are Yes or No.

</td></tr><tr><td>

Customer number

</td><td>

String

</td><td>

Unique identifier for the organization to the supplier.

</td></tr><tr><td>

On-boarded by

</td><td>

String

</td><td>

The person responsible for onboarding the supplier.

</td></tr><tr><td>

On-boarded date

</td><td>

String

</td><td>

Onboarding date of the supplier.

</td></tr><tr><td>

Off-boarded date

</td><td>

String

</td><td>

Termination date of the supplier from the organization.

</td></tr><tr><td>

Preferred

</td><td>

Boolean

</td><td>

Whether the supplier is preferred. The options are Yes or No.

</td></tr><tr><td>

PO box number

</td><td>

String

</td><td>

Post office box number where the supplier correspondence and payments are made.

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

Parent entity

</td><td>

String

</td><td>

Parent organization of the supplier.

</td></tr><tr><td>

Street address

</td><td>

String

</td><td>

Street where the supplier is located.

</td></tr><tr><td>

City

</td><td>

String

</td><td>

City where the supplier is located.

</td></tr><tr><td>

State/Province

</td><td>

String

</td><td>

State or province where the supplier is located.

</td></tr><tr><td>

County/District

</td><td>

String

</td><td>

County or district where the supplier is located.

</td></tr><tr><td>

ZIP/Postal code

</td><td>

String

</td><td>

Zip code or postal code where the supplier is located.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Country where the supplier is located.

</td></tr><tr><td>

Region

</td><td>

String

</td><td>

Region where the supplier is operating. Options are AMS, APAC, EMEA, or LATAM.

</td></tr><tr><td>

Primary phone number

</td><td>

String

</td><td>

Phone number of the primary contact from the supplier side.

</td></tr><tr><td>

Fax number

</td><td>

String

</td><td>

Number to which documents can be faxed to the supplier.

</td></tr></tbody>
</table>For more information, see [Supplier Lifecycle Operations data model](slo-data-model.md).

**Parent Topic:**[Primary data tables for Supplier Lifecycle Operations](slo-primary-data-tables.md)


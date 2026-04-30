---
title: Supplier Location inbound staging table
description: The Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table temporarily stores important data about the geographical location of a supplier before this data is sent to the Supplier Location \[sn\_slm\_m2m\_location\] and Location \[cmn\_location\] primary tables.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Inbound staging tables for Supplier Lifecycle Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier Location inbound staging table

The Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table temporarily stores important data about the geographical location of a supplier before this data is sent to the Supplier Location \[sn\_slm\_m2m\_location\] and Location \[cmn\_location\] primary tables.

## Supplier location inbound staging table

The following table lists the mandatory fields for the Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

String

</td><td>

The category that the supplier location belongs to. The choices are:-   Contracting address
-   Delivery address
-   Facility \(default\)
-   Headquarters
-   Invoice address
-   Service center

</td></tr><tr><td>

City

</td><td>

String

</td><td>

City of the supplier location.

</td></tr><tr><td>

Company

</td><td>

String

</td><td>

Name of the company that the supplier location is linked to.

</td></tr><tr><td>

Contact

</td><td>

String

</td><td>

Contact details of the supplier location.

</td></tr><tr><td>

Coordinates retrieved on

</td><td>

String

</td><td>

Coordinates of the supplier location that was retrieved on a specific date.

</td></tr><tr><td>

Country 

</td><td>

String

</td><td>

Country of the supplier location.

</td></tr><tr><td>

Duplicate 

</td><td>

String

</td><td>

Indicates whether the supplier location is a duplicate or not.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported.

</td></tr><tr><td>

Fax phone

</td><td>

String

</td><td>

Fax phone details of the supplier location.

</td></tr><tr><td>

Full name

</td><td>

String

</td><td>

Full name of the supplier location.

</td></tr><tr><td>

Integration status

</td><td>

String

</td><td>

Latitude coordinates of the supplier location.

</td></tr><tr><td>

Latitude

</td><td>

String

</td><td>

Latitude coordinates of the supplier location.

</td></tr><tr><td>

Location source

</td><td>

String

</td><td>

Source of the supplier location.

</td></tr><tr><td>

Location type

</td><td>

String

</td><td>

Type of the supplier location.

</td></tr><tr><td>

Longitude

</td><td>

String

</td><td>

Longitude coordinates of the supplier location.

</td></tr><tr><td>

Managed by group

</td><td>

String

</td><td>

Name of the group that manages the supplier location.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the supplier.

</td></tr><tr><td>

Primary

</td><td>

String

</td><td>

Indicates whether the supplier is primary or not.

</td></tr><tr><td>

Primary location

</td><td>

String

</td><td>

Primary location of the supplier.

</td></tr><tr><td>

Phone

</td><td>

String

</td><td>

Phone number of the supplier.

</td></tr><tr><td>

Phone territory

</td><td>

String

</td><td>

Phone territory of the supplier.

</td></tr><tr><td>

Processing message

</td><td>

String

</td><td>

A message that describes the current processing status.

</td></tr><tr><td>

State / Province

</td><td>

String

</td><td>

State of the supplier location.

</td></tr><tr><td>

Stock room

</td><td>

String

</td><td>

Stock room details of the supplier location.

</td></tr><tr><td>

Street address

</td><td>

String

</td><td>

Street address of the supplier location.

</td></tr><tr><td>

Time zone 

</td><td>

String

</td><td>

Timezone of the supplier location.

</td></tr><tr><td>

Zip/Postal code

</td><td>

String

</td><td>

Zip code of the supplier location.

</td></tr></tbody>
</table>**Parent Topic:**[Inbound staging tables for Supplier Lifecycle Operations](../concept/slo-inbound-staging-tables.md)

**Related topics**  


[Supplier Contact inbound staging table](slo-supp-contact-inbound-table.md)

[Supplier inbound staging table](slo-supplier-inbound-table.md)

[Supplier Legal Entity mapping inbound staging table](slo-legal-entity-inbound-table.md)

[Supplier Payment inbound staging table](slo-supp-payment-inbound-table.md)


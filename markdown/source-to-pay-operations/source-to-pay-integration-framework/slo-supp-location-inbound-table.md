---
title: Supplier location inbound staging table
description: The Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table temporarily stores important data about the geographical location of a supplier before this data is sent to the Supplier Location \[sn\_slm\_m2m\_location\] and Location \[cmn\_location\] primary tables.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Supplier Lifecycle Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier location inbound staging table

The Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table temporarily stores important data about the geographical location of a supplier before this data is sent to the Supplier Location \[sn\_slm\_m2m\_location\] and Location \[cmn\_location\] primary tables.

## Supplier location inbound staging table

The following table lists the mandatory fields for the Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Company|String|Name of the company that the supplier is linked to.|
|Zip/Postal code|String|The zip code of the supplier location.|
|ERP source|String|ERP source from which data is imported.|

**Parent Topic:**[Inbound staging tables for Supplier Lifecycle Operations](../concept/slo-inbound-staging-tables.md)

**Related topics**  


[Supplier contact inbound staging table](slo-supp-contact-inbound-table.md)

[Supplier inbound staging table](slo-supplier-inbound-table.md)

[Supplier legal entity mapping inbound staging table](slo-legal-entity-inbound-table.md)

[Supplier payment inbound staging table](slo-supp-payment-inbound-table.md)


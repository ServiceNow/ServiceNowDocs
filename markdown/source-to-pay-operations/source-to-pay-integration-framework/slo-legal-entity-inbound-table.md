---
title: Supplier legal entity mapping inbound staging table
description: The Supplier legal entity mapping inbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_inbound\] staging table temporarily stores important data about the legal entities of a supplier before this data is sent to the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) primary table.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Supplier Lifecycle Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier legal entity mapping inbound staging table

The Supplier legal entity mapping inbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_inbound\] staging table temporarily stores important data about the legal entities of a supplier before this data is sent to the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) primary table.

## Supplier legal entity mapping inbound staging table

The following table lists the mandatory fields for the Supplier legal entity mapping inbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_inbound\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Legal entity|String|Name of the legal entity of the supplier.|
|Supplier|String|Name of the supplier.|

**Parent Topic:**[Inbound staging tables for Supplier Lifecycle Operations](../concept/slo-inbound-staging-tables.md)

**Related topics**  


[Supplier contact inbound staging table](slo-supp-contact-inbound-table.md)

[Supplier inbound staging table](slo-supplier-inbound-table.md)

[Supplier location inbound staging table](slo-supp-location-inbound-table.md)

[Supplier payment inbound staging table](slo-supp-payment-inbound-table.md)


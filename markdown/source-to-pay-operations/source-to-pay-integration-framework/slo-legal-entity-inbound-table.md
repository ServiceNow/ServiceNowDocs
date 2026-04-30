---
title: Supplier Legal Entity mapping inbound staging table
description: The Supplier legal entity mapping inbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_inbound\] staging table temporarily stores important data about the legal entities of a supplier before this data is sent to the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) primary table.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Supplier Lifecycle Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier Legal Entity mapping inbound staging table

The Supplier legal entity mapping inbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_inbound\] staging table temporarily stores important data about the legal entities of a supplier before this data is sent to the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) primary table.

## Supplier legal entity mapping inbound staging table

The following table lists the mandatory fields for the Supplier legal entity mapping inbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_inbound\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Legal entity|String|Name of the legal entity of the supplier.|
|Supplier|String|Name of the supplier.|

**Parent Topic:**[Inbound staging tables for Supplier Lifecycle Operations](../concept/slo-inbound-staging-tables.md)

**Related topics**  


[Supplier Contact inbound staging table](slo-supp-contact-inbound-table.md)

[Supplier inbound staging table](slo-supplier-inbound-table.md)

[Supplier Location inbound staging table](slo-supp-location-inbound-table.md)

[Supplier Payment inbound staging table](slo-supp-payment-inbound-table.md)


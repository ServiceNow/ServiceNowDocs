---
title: Supplier payment inbound staging table
description: The Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table temporarily stores important data about the payment information of a supplier before this data is sent to the Supplier Payment Information \[sn\_fin\_supplier\_payment\] primary table.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Supplier Lifecycle Operations, Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier payment inbound staging table

The Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table temporarily stores important data about the payment information of a supplier before this data is sent to the Supplier Payment Information \[sn\_fin\_supplier\_payment\] primary table.

## Supplier payment inbound staging table

The following table lists the mandatory fields for the Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Supplier|Reference|The supplier that the payment information is for.|
|Bank name|String|Name of the bank.|
|Account number|Password2|Account number of the beneficiary.|

**Parent Topic:**[Inbound staging tables for Supplier Lifecycle Operations](../concept/slo-inbound-staging-tables.md)

**Related topics**  


[Supplier contact inbound staging table](slo-supp-contact-inbound-table.md)

[Supplier inbound staging table](slo-supplier-inbound-table.md)

[Supplier legal entity mapping inbound staging table](slo-legal-entity-inbound-table.md)

[Supplier location inbound staging table](slo-supp-location-inbound-table.md)


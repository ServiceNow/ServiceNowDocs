---
title: Supplier Payment inbound staging table
description: The Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table temporarily stores important data about the payment information of a supplier before this data is sent to the Supplier Payment Information \[sn\_fin\_supplier\_payment\] primary table.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Supplier Lifecycle Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier Payment inbound staging table

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


[Supplier Contact inbound staging table](slo-supp-contact-inbound-table.md)

[Supplier inbound staging table](slo-supplier-inbound-table.md)

[Supplier Legal Entity mapping inbound staging table](slo-legal-entity-inbound-table.md)

[Supplier Location inbound staging table](slo-supp-location-inbound-table.md)


---
title: Supplier Payment inbound staging table
description: The Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table temporarily stores important data about the payment information of a supplier before this data is sent to the Supplier Payment Information \[sn\_fin\_supplier\_payment\] primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-slo-supp-payment-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier Payment inbound staging table

The Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table temporarily stores important data about the payment information of a supplier before this data is sent to the Supplier Payment Information \[sn\_fin\_supplier\_payment\] primary table.

The following table lists the fields for the Supplier Payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Supplier|Reference|The supplier that the payment information is for.|
|Bank name|String|Name of the bank.|
|Account number|Password2|Account number of the beneficiary.|


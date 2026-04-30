---
title: Supplier payment outbound staging table
description: The Supplier payment outbound \[sn\_spend\_intg\_supplier\_payment\_outbound\_stage\] staging table temporarily stores important data about the payment information of a supplier so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Supplier Lifecycle Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier payment outbound staging table

The Supplier payment outbound \[sn\_spend\_intg\_supplier\_payment\_outbound\_stage\] staging table temporarily stores important data about the payment information of a supplier so that an ERP integrator can export this data to a third-party ERP system.

## Supplier payment outbound staging table

The following table lists the mandatory fields for the Supplier payment outbound \[sn\_spend\_intg\_supplier\_payment\_outbound\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|ABA routing number|String|Unique, nine-digit number used to identify banks and financial institutions.|
|Account number|String|Account number of the beneficiary for the supplier payment.|
|Active|String|Indicates whether the supplier is active or not.|
|Bank identification number|String|Bank identification number for the supplier payment.|
|Bank name|String|Name of the bank for the supplier payment.|
|Beneficiary name on account|String|Beneficiary name on the account for the supplier payment.|
|Branch code|String|Branch code for the supplier payment.|
|BSB code|String|Bank State Branch is a six-digit number that is used to identify a bank code and its associated branch in Australia.|
|Country|String|Name of the country of the supplier.|
|Currency|String|Three-digit ISO currency code used for a given country.|
|Domain|String|Domain name of the supplier.|
|ERP company code|String|Company code of the entity in the ERP system.|
|ERP source|String|ERP source used by the organization.|
|IBAN|String|International Bank Account Number used for international payments.|
|IFSC code|String|Indian Financial System Code \(IFSC\) is a unique 11-digit alphanumeric code that is used for online fund transfer transactions in India.|
|Integration status|String|Current status of the supplier payment integration.|
|Primary|String|Indicates whether this account is the primary account.|
|Processing message|String|A message that describes the current processing status.|
|Sort code or transit code|String|Sort code or transit code of the supplier's bank.|
|Supplier|String|Name of the supplier that the payment information is for.|
|SWIFT code|String|Bank Identifier Code \(also known as SWIFT code\) of the bank of the supplier.|


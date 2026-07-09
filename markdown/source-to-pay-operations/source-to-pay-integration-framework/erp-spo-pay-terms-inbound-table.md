---
title: Payment Terms Stage inbound staging table
description: The Payment Terms Stage inbound \[sn\_fcms\_intg\_payment\_term\_stage\] staging table temporarily stores important data about payment terms before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-pay-terms-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Payment Terms Stage inbound staging table

The Payment Terms Stage inbound \[sn\_fcms\_intg\_payment\_term\_stage\] staging table temporarily stores important data about payment terms before this data is sent to the primary table.

The following table lists the fields for the Payment Terms Stage inbound \[sn\_fcms\_intg\_payment\_term\_stage\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Discount days|Integer|Specific days or periods during which you receive discounts on products.|
|Discount percentage|Decimal|Cash discount percentage rate.|
|ERP source|String|ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.|
|Name|String|The name or code of the payment term. Example: Net 060.|
|Net days to pay|Integer|Number of days within which payment is due after receiving an invoice.|
|Payment term|String|Term for making the payment.|
|Short description|String|A short explanation of the payment term. Example: 2%14, Net 60.|
|Type|String|Type of the payment term.|


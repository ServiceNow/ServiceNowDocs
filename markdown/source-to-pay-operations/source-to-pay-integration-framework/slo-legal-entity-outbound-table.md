---
title: Supplier legal entity mapping outbound staging table
description: The Supplier legal entity mapping outbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_outbound\] staging table temporarily stores important data about the legal entities of a supplier so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Supplier Lifecycle Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Supplier legal entity mapping outbound staging table

The Supplier legal entity mapping outbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_outbound\] staging table temporarily stores important data about the legal entities of a supplier so that an ERP integrator can export this data to a third-party ERP system.

## Supplier legal entity mapping outbound staging table

The following table lists the mandatory fields for the Supplier legal entity mapping outbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_outbound\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Active|String|Indicates if the supplier legal entity is active or not.|
|Bank details|String|Bank details of the supplier legal entity.|
|Domain|String|Domain name of the supplier legal entity.|
|ERP company code|String|Company code of the entity in the ERP system.|
|ERP source|String|ERP source used by the organization.|
|General ledger account|String|The account to which capital or operational expenses will be posted.|
|Hold payment|String|Indicates that the invoice payment is put on hold for the supplier.|
|Hold posting|String|Indicates that the invoice posting is put on hold for the supplier.|
|Integration status|String|Current status of the supplier legal entity integration.|
|Legal entity|String|Name of the legal entity of the supplier.|
|Onboarded|String|Indicates if a user has completed the onboarding process.|
|Payment method|String|Payment method preferred by the supplier legal entity.|
|Payment term|String|Agreed time and conditions for payment to the supplier legal entity.|
|Processing message|String|A message that describes the current processing status.|
|Remit to city|String|City to which the payment is made.|
|Remit to country|String|Country to which the payment is made.|
|Remit to state|String|State to which the payment is made.|
|Remit to street address|String|Street address to which the payment is made.|
|Remit to zipcode|String|Zip code to which the payment is made.|
|Supplier|String|Name of the supplier.|


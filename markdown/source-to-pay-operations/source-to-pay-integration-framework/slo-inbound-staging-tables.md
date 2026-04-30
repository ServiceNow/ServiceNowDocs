---
title: Inbound staging tables for Supplier Lifecycle Operations
description: The inbound staging tables for Supplier Lifecycle Operations temporarily store supplier data before it is sent to the SLO primary data tables.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Inbound staging tables for Supplier Lifecycle Operations

The inbound staging tables for Supplier Lifecycle Operations temporarily store supplier data before it is sent to the SLO primary data tables.

-   **[Supplier contact inbound staging table](../reference/slo-supp-contact-inbound-table.md)**  
The Supplier contact inbound \[sn\_fcms\_intg\_supplier\_contact\_inbound\] staging table temporarily stores important data about a supplier contact before this data is sent to the Supplier Contact \[vm\_vdr\_contact\] primary table.
-   **[Supplier inbound staging table](../reference/slo-supplier-inbound-table.md)**  
The Supplier inbound \[sn\_fcms\_intg\_imp\_supplier\] staging table temporarily stores important data about the supplier before this data is sent to the Supplier \[sn\_fin\_supplier\] primary table.
-   **[Supplier legal entity mapping inbound staging table](../reference/slo-legal-entity-inbound-table.md)**  
The Supplier legal entity mapping inbound \[sn\_fcms\_intg\_supplier\_legal\_entity\_inbound\] staging table temporarily stores important data about the legal entities of a supplier before this data is sent to the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) primary table.
-   **[Supplier location inbound staging table](../reference/slo-supp-location-inbound-table.md)**  
The Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table temporarily stores important data about the geographical location of a supplier before this data is sent to the Supplier Location \[sn\_slm\_m2m\_location\] and Location \[cmn\_location\] primary tables.
-   **[Supplier payment inbound staging table](../reference/slo-supp-payment-inbound-table.md)**  
The Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\] staging table temporarily stores important data about the payment information of a supplier before this data is sent to the Supplier Payment Information \[sn\_fin\_supplier\_payment\] primary table.

**Parent Topic:**[Inbound staging tables for Source-to-Pay Operations](../../sourcing-procurement-operations/concept/s2p-inbound-staging-tables.md)

**Related topics**  


[Inbound staging tables for Sourcing and Procurement Operations](../../sourcing-procurement-operations/concept/spo-inbound-staging-tables.md)

[Inbound staging tables for Accounts Payable Operations](../../accounts-payable-operations/concept/inbound-staging-tables-for-apo.md)


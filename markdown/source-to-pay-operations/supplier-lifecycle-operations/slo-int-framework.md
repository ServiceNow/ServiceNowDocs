---
title: Supplier Lifecycle Operations integration framework
description: The Supplier Lifecycle Operations \(SLO\) integration framework enables you to exchange supplier data with any third-party ERP system.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier Lifecycle Operations integration framework

The Supplier Lifecycle Operations \(SLO\) integration framework enables you to exchange supplier data with any third-party ERP system.

**Important:** Check your entitlements to determine whether you have access to Supplier Lifecycle Operations integration framework.

The SLO integration framework facilitates inbound and outbound integration with third-party applications and ERP systems.

## SLO integration framework flow

For inbound flow:

Import supplier data from a third-party ERP system by populating the SLO inbound staging tables, and then run transform maps to update the supplier data into SLO primary tables.

For outbound flow:

-   As soon as the SLO primary tables are updated, the SLO outbound tables are automatically updated using subflows.
-   An ERP integrator can refer to the outbound tables and export the required data into any third-party ERP system.

## SLO inbound staging tables

The following table lists the SLO inbound staging tables and the application they belong to.

|Application|SLO inbound table|
|-----------|-----------------|
|ERP Integration Framework​ \(com.sn\_fcms\_integrations\)|sn\_fcms\_intg\_imp\_supplier​|
| |sn\_fcms\_intg\_supplier\_location\_inbound|
| |sn\_fcms\_intg\_supplier\_contact\_inbound​|
| |sn\_fcms\_intg\_supplier\_payment\_inbound\_stage|
| |sn\_fcms\_intg\_supplier\_legal\_entity\_inbound|

## SLO outbound staging tables

The following table lists the SLO outbound staging tables and the application they belong to.

|Application|SLO outbound table|
|-----------|------------------|
|Source-to-Pay Integration Framework​ \(com.sn\_spend\_intg​\)|sn\_spend\_intg\_outbound\_supplier​|
| |sn\_spend\_intg\_supplier\_location\_outbound​|
| |sn\_spend\_intg\_supplier\_contact\_outbound​|
| |sn\_spend\_intg\_supplier\_payment\_outbound\_stage​|

The same set of fields exist in both the SLO inbound and SLO outbound staging tables. For more information about the mandatory fields in the staging tables and their descriptions, see [Inbound staging tables for Supplier Lifecycle Operations](slo-inbound-staging-tables.md).

-   **[Add supplier inbound data in an Excel file](../task/import-external-data-into-slo.md)**  
You can import supplier inbound table data in an Excel file.
-   **[Load supplier data](../task/load-supplier-data.md)**  
Load the supplier data from the excel template into the supplier inbound​ staging tables.

**Parent Topic:**[Integrate Supplier Lifecycle Operations with other applications](integrate-slo.md)

**Related topics**  


[Craft.co Integration for Supplier Lifecycle Operations](craft-integration.md)

[News Integration for Supplier Lifecycle Operations](supp-news-integration.md)

[Relish Integration for Supplier Lifecycle Operations](relish-slo-connector.md)

[Add supplier inbound data in an Excel file](../task/import-external-data-into-slo.md)

[Load supplier data](../task/load-supplier-data.md)


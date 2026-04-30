---
title: Use schedule flows in SAP ECC and SAP S4 HANA
description: Use the schedule flows that interact with SAP ECC and SAP S4 HANA to pull information on purchase requisition, purchase order, receipt, invoice, and sourcing.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-02-18"
reading_time_minutes: 3
breadcrumb: [Using Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use schedule flows in SAP ECC and SAP S4 HANA

Use the schedule flows that interact with SAP ECC and SAP S4 HANA to pull information on purchase requisition, purchase order, receipt, invoice, and sourcing.

You can either use the subflows to perform the required tasks or you can create a copy of the subflows and then customize it according to your requirements. The Source-to-Pay with SAP ECC and SAP S4 HANA integration supports the following subflows:

## Primary Data Integration with SAP ECC and SAP S4 HANA

The Primary Data Integration with SAP ECC and SAP S4 HANA integration supports the following subflows:

|Subflow|Description|
|-------|-----------|
|Fetch GL Accounts|Use this subflow to fetch and sync all GL accounts from SAP S4 HANA OData system.|
|Fetch Legal Entities|Use this subflow to fetch and sync all legal entities from SAP S4 HANA OData system.|
|Fetch Invoices|Use this subflow to fetch and sync all Invoices from SAP S4 HANA OData system|
|Fetch Suppliers|Use this subflow to fetch and sync all supplier details from SAP S4 HANA OData system.|
|Fetch Plant Addresses|Use this subflow to Fetch Plant Addresses from SAP S4 HANA OData system.|
|Fetch Purchasing Group|Use this subflow to fetch and sync all Purchasing Group from SAP S4 HANA OData system.|
|Fetch Payment Terms|Use this subflow to fetch and sync all payment terms from SAP S4 HANA OData system.|
|Fetch Materials|Use this subflow to fetch and sync all Materials from SAP S4 HANA OData system.|
|Fetch FX Rates|Use this subflow to fetch and sync all FX rates from SAP S4 HANA OData system.|
|Fetch Currencies|Use this subflow to fetch and sync all Currencies from SAP S4 HANA OData system.|
|Fetch Purchasing Organizations|Use this subflow to fetch and sync all Purchasing Organizations from SAP S4 HANA OData system.|
|Fetch Cost Center|Use this subflow to fetch and sync all cost centers from SAP S4 HANA OData system.|
|Fetch Unit of Measure|Use this subflow to fetch base unit of measure from SAP S4 HANA OData system.|
|Fetch Material Group|Use this subflow to fetch and sync all Material Groups from SAP S4 HANA OData system.|

**Important:**

These subflows are read only. To modify a flow or subflow, create a copy and then apply the required changes.

## Supplier Lifecycle Operations Integration with SAP ECC and SAP S4 HANA

The Supplier Lifecycle Operations Integration with SAP ECC and SAP S4 HANA supports the following subflows:

|Flow|Description|
|----|-----------|
|Create or update supplier|Creates or updates or deactivates supplier in SAP ECC and SAP S4 HANA.|
|Deactivate supplier bank details|Deactivates the supplier bank details in SAP ECC and SAP S4 HANA.|
|Create or update supplier payment information|Creates or updates supplier payment information in SAP ECC and SAP S4 HANA.|

**Important:**

These subflows are read-only. To modify a flow or subflow, create a copy and then apply the required changes.

## Sourcing and Procurement Operations Integration with SAP ECC and SAP S4 HANA

The Sourcing and Procurement Operations Integration with SAP ECC and SAP S4 HANA supports the following subflows:

|Flow|Description|
|----|-----------|
|Create or update purchase order|Creates or updates purchase order in SAP ECC and SAP S4 HANA.|
|Create Goods Receipts|Creates Goods Receipts in SAP S4 HANA and SAP S4 HANA|

## Accounts Payable Operations Integration with SAP ECC and SAP S4 HANA

The Accounts Payable Operations Integration with SAP ECC and SAP S4 HANA supports the following subflows:

|Flow|Description|
|----|-----------|
|Create Invoice|Creates invoice in SAP ECC and SAP S4 HANA.|
|Create Non-Purchase Order Invoice|Create Non-Purchase Order Invoice in in SAP ECC and SAP S4 HANA.|

-   **[Use a flow or subflow in SAP ECC and SAP S4 HANA \(Outbound\)](../task/use-flow-or-subflow-sap.md)**  
A flow or subflow can be executed in SAP ECC and SAP S4 HANA using the Workflow Studio. Follow these steps to run a flow or subflow.
-   **[Copy a flow or subflow in SAP ECC and SAP S4 HANA](../task/copy-flow-or-subflow-sap.md)**  
You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.

**Parent Topic:**[Using Source-to-Pay integration with SAP ECC and SAP S4 HANA](using-source-to-pay-sap-integration.md)


---
title: Use flows in SAP Ariba
description: Use flows to retrieve information from SAP Ariba, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, supplier bids, and legal entities.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use flows in SAP Ariba

Use flows to retrieve information from SAP Ariba, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, supplier bids, and legal entities.

You can either use the subflows to perform the required tasks or you can create a copy of the subflows and then customize it according to your requirements. The Source-to-Pay with SAP Ariba integration supports the following subflows.

## Supplier Lifecycle Operations Integration with SAP Ariba

The Supplier Lifecycle Operations integration with SAP Ariba supports the following flows and subflows:

|Flow/Subflow|Description|
|------------|-----------|
|Flow|
|Create Supplier in SAP Ariba|Creates suppliers in SAP Ariba|
|Update supplier contact in SAP Ariba.|Updates supplier contact details in SAP Ariba|
|Update supplier info in SAP Ariba.|Updates supplier information in SAP Ariba|
|Update supplier legal entities in SAP Ariba.|Updates supplier's legal entity details inSAP Ariba|
|Update supplier location in SAP Ariba.|Updates supplier location details in SAP Ariba|
|Update supplier payment information in SAP Ariba.|Updates supplier payment information in SAP Ariba|
|Subflow|
|Create supplier in SAP Ariba.|Creates suppliers in SAP Ariba|
|Update supplier details in SAP Ariba.|Updates supplier detailsSAP Ariba|
|Update supplier details to in process.|Updates supplier details to in process.|

**Important:**

These flows and subflows are read only. To modify a flow or subflow, create a copy and then apply the required changes.

## Sourcing and Procurement Operations Integration with SAP Ariba

The Sourcing and Procurement Operations Integration with SAP Ariba supports the following subflows:

|Flow/Subflow|Description|
|------------|-----------|
|Flow|
|Award Sourcing Event in SAP Ariba REST|Awards sourcing events in SAP Ariba REST|
|Create or Update Sourcing Event in SAP Ariba|Creates or updates sourcing event in SAP Ariba|
|Create Receipt in ERP|Creates receipts in ERP|
|Fetch Supplier Bids for Sourcing Event from SAP Ariba REST|Fetches supplier bids for sourcing event from SAP Ariba REST|
|Subflow|
|Award Sourcing Event in SAP Ariba REST|Awards sourcing events in SAP Ariba REST|
|Create Receipt in SAP Ariba|Creates receipts in SAP Ariba|
|Creating or Updating of Sourcing Event in SAP Ariba|Creates or updates sourcing event in SAP Ariba|
|Fetch Supplier Bids for Sourcing Event for SAP Ariba|Fetches supplier bids for sourcing event from SAP Ariba|
|Fetch Supplier Bids for Sourcing Event Service Ariba|Fetches supplier bids for sourcing event service|

## Accounts Payable Operations Integration with SAP Ariba

The Accounts Payable Operations Integration with SAP Ariba supports the following subflows:

|Flow|Description|
|----|-----------|
|Fetches invoices from SAP Ariba REST|Fetches accounts payable invoices inSAP Ariba.|
|Update invoice statuses as Rejected in SAP Ariba REST|Updates invoice statuses as rejected in SAP Ariba|
|Fetch invoices from SAP Ariba REST service|Fetches invoices from SAP Ariba REST service|

-   **[Manually trigger flows or subflows in SAP Ariba \(Inbound\)](../task/manually-trigger-subflows-sap-ariba.md)**  
You can manually trigger flows or subflows in SAP Ariba on demand.
-   **[Use a flow or subflow in SAP Ariba \(Outbound\)](../task/use-subflow-sap-ariba.md)**  
Execute a flow or subflow in SAP Ariba using the Workflow Studio.
-   **[Copy a flow or subflow in SAP Ariba](../task/copy-subflow-sap-ariba.md)**  
You can create a copy of the a flow or subflow, and modify based on your requirements.

**Parent Topic:**[Use Source-to-Pay integration with SAP Ariba](using-source-to-pay-sap-ariba-integration.md)


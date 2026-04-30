---
title: Use flows in SAP Ariba
description: Use flows to retrieve information from SAP Ariba, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, supplier bids, and legal entities.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-22"
reading_time_minutes: 1
breadcrumb: [Using Source-to-Pay integration with SAP Ariba, Source-to-Pay integration with SAP Ariba, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use flows in SAP Ariba

Use flows to retrieve information from SAP Ariba, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, supplier bids, and legal entities.

You can either use the subflows to perform the required tasks or you can create a copy of the subflows and then customize it according to your requirements. The Source-to-Pay with SAP Ariba integration supports the following subflows.

## Sourcing and Procurement Operations Integration with SAP Ariba

The Sourcing and Procurement Operations Integration with SAP Ariba supports the following subflows:

|Flow/Subflow|Description|
|------------|-----------|
|Flow|
|Create or Update Sourcing Event in SAP Ariba|Creates or updates sourcing event in SAP Ariba|
|Create Receipt in ERP|Creates receipts in ERP|
|Fetch Supplier Bids for Sourcing Event from SAP Ariba REST|Fetches supplier bids for sourcing event from SAP Ariba REST|
|Subflow|
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

**Parent Topic:**[Using Source-to-Pay integration with SAP Ariba](using-source-to-pay-sap-ariba-integration.md)


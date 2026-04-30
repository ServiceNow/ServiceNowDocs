---
title: Use schedule flows in Oracle EBS
description: Use the schedule flows to retrieve information from Oracle EBS, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-02-18"
reading_time_minutes: 2
breadcrumb: [Using Source-to-Pay integration with Oracle EBS, Source-to-Pay integration with Oracle EBS, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use schedule flows in Oracle EBS

Use the schedule flows to retrieve information from Oracle EBS, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.

You can either use the subflows to perform the required tasks or you can create a copy of the subflows and then customize it according to your requirements. The Source-to-Pay with Oracle EBS integration supports the following subflows:

## Source-to-Pay Integration with Oracle EBS

The Source-to-Pay with Oracle EBS integration supports the following subflows:

|Subflow|Description|
|-------|-----------|
|Create or update or cancel purchase order|Creates or updates or cancels purchase order in Oracle EBS.|
|Create goods receipt|Creates goods receipts in Oracle EBS.|

**Important:**

These subflows are read only. To modify a flow or subflow, create a copy and then apply the required changes.

## Supplier Lifecycle Operations Integration with Oracle EBS

The Supplier Lifecycle Operations Integration with Oracle EBS supports the following subflows:

|Flow|Description|
|----|-----------|
|Create or update or deactivate supplier|Creates or updates or deactivates supplier in Oracle EBS.|
|Create or update supplier location|Creates or updates supplier location in Oracle EBS.|
|Create or update supplier payment information|Creates or updates supplier payment information in Oracle EBS.|

**Important:**

These subflows are read-only. To modify a flow or subflow, create a copy and then apply the required changes.

## Sourcing and Procurement Operations Integration with Oracle EBS

The Sourcing and Procurement Operations Integration with Oracle EBS supports the following subflows:

|Flow|Description|
|----|-----------|
|Create or updates or cancels purchase order|Creates or updates or cancels purchase order in Oracle EBS.|

## Accounts Payable Operations Integration with Oracle EBS

The Accounts Payable Operations Integration with Oracle EBS supports the following subflows:

|Flow|Description|
|----|-----------|
|Create AP invoice|Creates AP invoice in Oracle EBS.|

-   **[Manually trigger flows or subflows in Oracle EBS \(Inbound\)](../task/manually-trigger-subflows-oracle-ebs.md)**  
You can manually trigger flows or subflows in Oracle EBS on demand. Follow these steps to manually trigger a flow or subflow.
-   **[Use a flow or subflow in Oracle EBS \(Outbound\)](../task/use-flow-or-subflow-oracle-ebs.md)**  
A flow or subflow can be executed in Oracle EBS using the Workflow Studio. Follow these steps to run a flow or subflow.
-   **[Copy a flow or subflow in Oracle EBs](../task/copy-flow-or-subflow-oracle-ebs.md)**  
You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.

**Parent Topic:**[Using Source-to-Pay integration with Oracle EBS](using-source-to-pay-oracle-ebs-integration.md)


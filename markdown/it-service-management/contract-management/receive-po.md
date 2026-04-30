---
title: Receive a purchase order for contract assets
description: Receive the purchase order for assets covered in the contract by using the Renewal purchase order task. This task is available if you have added at least one hardware asset, created an entitlement, or selected an existing entitlement that is in the Build state.
locale: en-US
release: zurich
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Contract renewal workflow, Contract Management, Asset Management, IT Service Management]
---

# Receive a purchase order for contract assets

Receive the purchase order for assets covered in the contract by using the Renewal purchase order task. This task is available if you have added at least one hardware asset, created an entitlement, or selected an existing entitlement that is in the Build state.

## Before you begin

This task is not created if you haven't selected or added any hardware assets or entitlements or the Procurement plugin \(com.snc.procurement\) is not active. You must instead manually track the financial expenses.

Role required: procurement\_user

## Procedure

1.  On the Contract Renewal Request form, select the **Open Tasks** tab.

2.  Select the contract renewal request number.

3.  Select the **Purchase orders** tab.

4.  Select the purchase order number to capture the financial transactions of the contract.

    For every asset record covered under a contract, a purchase order line item is created. The cost of each purchase order is the renewal cost of each asset covered.

    The purchase order line items are created for the entitlements that are in the Build state. Each entitlement added in the Planned Entitlements tab corresponds to a unique purchase order line.

5.  Select **Order**.

6.  Select **Receive** to receive the purchase order for assets covered by the contract.

    Receiving the purchase order only updates the assets and does not create an entitlement.


## Result

The draft entitlement is published and the status is set to In use.

The purchase order receipt is listed in the **Receiving Slips** tab.

The status of the purchase order and purchase order line items shows as Received. The state of the Renewal purchase order task automatically changes to Closed Complete. The contract renewal request flow is complete.

The substate of the old contract is set to Renewed. A contract history record is created that displays the start and end dates of the old contract and the renewed contract, and the renewal date. You can view the entire history of the contract by selecting the Contract History tab in the Related Links section.

After you receive the purchase order, the state of the renewal contract is no longer Draft and the contract becomes active. If the start date of the renewed contract has been reached but the purchase order has not been received, the status of the contract renewal request remains set to Draft. After the new contract becomes active, the old contract becomes expired and the covered assets have an end date.


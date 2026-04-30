---
title: Contract renewal workflow
description: Use the contract renewal workflow to renew contracts that are nearing their expiry date or are already expired. This workflow enables you to renew contracts through a streamlined and managed process.
locale: en-US
release: xanadu
product: Contract Management
classification: contract-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Contract Management, Asset Management, IT Service Management]
---

# Contract renewal workflow

Use the contract renewal workflow to renew contracts that are nearing their expiry date or are already expired. This workflow enables you to renew contracts through a streamlined and managed process.

Renew your contracts by creating, validating, approving, and activating a contract record that references the original contract. This workflow enables you to manage related entities like hardware assets, software entitlements, terms and conditions, and rate cards.

**Note:** The contract renewal workflow supports Software license, Subscription contract, Maintenance, and Warranty contract models.

Complete the following tasks in the contract renewal workflow to renew your contracts:

1.  [Contract renewal request](../task/create-contract-renew-req.md): Create a contract renewal request for contracts that are nearing their expiry date or are already expired.
2.  [Contract selection](../task/select-contract.md): Renew multiple child contracts under the parent contract.
3.  [Build renewal](../task/fill-cont-renew-info.md): Supply the contract renewal information.
4.  [Asset selection](../task/select-hw-asset.md): Add or remove hardware or enterprise assets from the contract renewal process, and view the assets carried over to the new contract.
5.  [Software assets selection](../task/select-sw-asset.md): Add or remove software entitlements that you want to include in the contract renewal process, and view the entitlements carried over to the new contract.
6.  [Terms and conditions](../task/update-terms-conditions.md): Update the terms and conditions in your new contract, and view the terms and conditions carried over to the new contract.
7.  [Rate cards](../task/update-rate-card.md): Add rate card details to the new contract to track contract expenses.
8.  [Renewal confirmation](../task/confirm-cont-renewal.md): Review the renewal details after completing all the details of a contract.
9.  [Renewal approval](../task/approve-cont-renew.md): Approve or reject a contract renewal request for all Contract Renewal Request Lines.
10. [Renewal purchase order](../task/receive-po.md): Receive the purchase order for assets covered in the contract.

**Note:**

-   You can't edit a task after you close it.
-   You can cancel a contract renewal process for a Contract, Contract Renewal Request, Contract Renewal Request Lines, and Contract Renewal tasks. For more information, see [Results of canceling a contract renewal process](../reference/cancel-contract-renewal.md).

## Prerequisites

Before using the contract renewal workflow, you must complete the following prerequisites:

-   Activate the Software Asset Management Professional \(com.snc.samp\) plugin on your ServiceNow instance.

    If you want to manage hardware or enterprise assetcontracts, request and install the Hardware Asset Management orEnterprise Asset Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) instead.

-   Enable the **sn\_contract\_enable\_renewal\_flow** system property.

    **Note:** If you’re already using Software Asset Management, Hardware Asset Management, or both, this system property is set to false. If you’re a new user, this system property is set to true.


## Domain separation

Domain separation with data separation is supported for the contract renewal workflow with the following requirements:

-   The request is created in the domain of the contract that initiated the renewal process.
-   Request lines are in the domain of the contract of the request line.
-   Tasks are created in the domain of the contract being renewed.

The **sn\_contract\_enable\_renewal\_flow** system property also supports domain separation.


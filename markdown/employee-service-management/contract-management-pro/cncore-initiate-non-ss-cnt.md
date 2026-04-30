---
title: Initiate a non-self-served contract request
description: As a case owner or fulfiller, initiate the submission of contracts when you want third-party based contract documents to be sent for review.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Initiating a contract request, Use Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Initiate a non-self-served contract request

As a case owner or fulfiller, initiate the submission of contracts when you want third-party based contract documents to be sent for review.

## About this task

The initiated contract is assigned according to an assignment rule or manually by a contract fulfiller or a group manager. The contract administrator can modify the assignment rule to specify the group to which the contract request should be assigned.

## Before you begin

Ensure that the initiate contract button has been added to your workspace. For more information, see [Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md).

Role required: sn\_cm\_core.contract\_user, sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to your workspace.

2.  Open the case for which you want to initiate a contract.

3.  Select **Initiate contract**.

4.  In the **Type of paper** drop-down list, select **Third-party paper**.

5.  In the **Signature type** drop-down list, select the signature type for the contract document.

6.  In the **Start date** field, specify the contract start date.

7.  In the **End date** field, specify the contract end date.

    The End date should be later than the Start date.

8.  Select **Initiate**.


## Result

A contract request is initiated and opens in a new tab displaying the contract request details.

If there are validation errors, the contract request is created in the Draft state. If there are no validation errors, the contract request is created in the Work in progress state.

<table id="table_nhc_qrw_f1c"><thead><tr><th>

Field

</th><th>

Values

</th></tr></thead><tbody><tr><td>

State

</td><td>

A contract request is created in Draft state.

</td></tr><tr><td>

Contract Status

</td><td>

The contract status is set to Draft.

</td></tr><tr><td>

Parent

</td><td>

Parent request that initiated the contract request.

</td></tr><tr><td>

Requested for

</td><td>

User who was assigned the parent request.

</td></tr><tr><td>

Opened by

</td><td>

User who initiates the contract request.

</td></tr><tr><td>

Assignment group

</td><td>

User group assigned according to the assignment rule.

</td></tr><tr><td>

Signature type

</td><td>

Type of signature.-   Electronic signature: The signatory electronically signs the contract.
-   Wet signature: The signatory manually signs the physical version of the contract.

The default signature type is Electronic Signature.

</td></tr></tbody>
</table>## What to do next

Add contract documents and submit the contract request. For more information, see [Add contract documents to non-self-served contract request](cncore-nss-add-cont-doc.md).

**Parent Topic:**[Initiating a contract request](cncore-initiate-contract.md)


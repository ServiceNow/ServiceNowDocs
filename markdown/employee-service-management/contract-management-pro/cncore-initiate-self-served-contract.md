---
title: Initiate a self-served contract request
description: As a case owner or fulfiller, initiate a self-served contract for the case you are working on. Self-served contracts are submitted when you want own paper based contract documents to be sent for review.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Initiating a contract request, Use Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Initiate a self-served contract request

As a case owner or fulfiller, initiate a self-served contract for the case you are working on. Self-served contracts are submitted when you want own paper based contract documents to be sent for review.

## Before you begin

Before initiating a self-serve contract request, ensure you have created contract types and templates for them. For more information, see [Create a contract type](cncore-create-contract-type.md) and [Configure contract templates for a contract request](../concept/cncore-document-templates.md).

Ensure that the initiate contract button has been added to your workspace. For more information, see [Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md).

Role required: sn\_cm\_core.contract\_user or sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to your workspace.

2.  Open the case for which you want to initiate a contract.

3.  Select **Initiate contract**.

4.  In the **Type of paper** drop-down list, select **Own paper**.

5.  In the **Contract type** drop-down list, select the type of contract you want to generate.

    **Note:** Only active contract types are displayed in the list.

6.  In the **Signature type** drop-down list, select the signature type for the contract document.

7.  In the **Start date** field, specify the contract start date.

8.  In the **End date** field, specify the contract end date.

    The End date should be later than the Start date.

9.  Select **Initiate**.

    If you do not have an active contract template for the selected contract type, an error is displayed.


## Result

A contract request is initiated and opens on a new tab displaying the contract request details.

If there are validation errors, the contract request is created in **Draft** state. If there are no validation errors, the contract request is created in **Work in progress** state.

On the Contract request form, you can assign the contract request, add collaborators, add users to the watch list, change the signature type, and also update the start date and end date.

## What to do next

The next steps depend on whether there were validation errors:

-   If there were validation errors, complete the signatory details and resubmit the contract request. For more information, see [Resolve the failure to submit a self-serve contract](cncore-sync-signatories-fulfiller.md).
-   If there were no validation errors, you can proceed to work on the contract request. For more information see, [Work on a self-served contract request](cncore-work-ss-cntr-request-fulfiller.md) and [Work on a self-served contract request](cncore-work-ss-cntr-request-fulfiller.md).

**Parent Topic:**[Initiating a contract request](cncore-initiate-contract.md)


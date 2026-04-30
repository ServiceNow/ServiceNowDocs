---
title: Initiate an amendment request
description: Initiate an amendment request from your workspace.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Initiating a contract or amendment request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate an amendment request

Initiate an amendment request from your workspace.

## About this task

A sample workflow while submitting on an amendment request would be:

1.  Initiate an amendment request from the workspace using the Initiate contract option.
2.  Enter amendment details and submit the request.

The initiated amendment is assigned according to an assignment rule or manually by a contract fulfiller or a group manager. The contract administrator can modify the assignment rule to specify the group to which the contract request should be assigned.

## Before you begin

-   Amendment requests can only be submitted for contracts in the Active state. If a contract is in Draft state and Awaiting Review substate, manually approve it before submitting an amendment request. For more information on how to approve a contract, see [Approve contracts to allow amendments](cmpro-approve-draft-cntr.md).
-   Verify that the initiate contract button has been added to your workspace. For more information, see [Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md).
-   To copy field values from the parent contract request to the amendment request, configure the ContractManagementExt extension point. For more information, see [Copy fields from parent request to amendment request](cncore-cpy-fld-parent-amedreq.md).
-   Verify you have a contract configuration with the request type set as amendment to copy values from amendment request to the contract repository. For more information, see [Create a contract configuration](cncore-contract-config.md).
-   Verify you have a contract template rule to identify the amendment document template to be used for generating the contract document for an amendment request. For more information, see [Configure contract template rules](cncore-config-template-rules.md).

Role required: sn\_cm\_core.contract\_user, sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to your workspace.

2.  Open the case for which you want to initiate a contract.

3.  Select **Initiate contract**.

4.  In the **Request type** dropdown, select Amendment.

5.  Select type of paper in the **Type of paper** field.

    -   For own paper based amendment request, select **Own paper**.
    -   For third party paper based amendment request, select **Third Party Paper**. Amendment is supported for third-party contracts with a single contract type.
6.  In the **Contract type** field, select the type of contract for which the contract request is created.

    ![Use initiate contract modal from the workspace to submit an contract amendment request](../image/cmpro-amend-initiate.png)

7.  In the **Signature type** drop-down list, select the signature type for the contract document.

    For more information on the signature flow, see [Signature workflow for a contract request](../concept/cncore-signature-workflow.md)

8.  In the **Amendment description** field, enter the details of the changes required to the existing contract document and any other details.

9.  In the **Effective date** field, select a date within the existing contract’s start and end dates to indicate when the amendment takes effect.

10. Select **Initiate**.

11. For third-party paper amendment request, attach contract documents and submit the request.

    1.  In the Contract Document tab, select **Attach Document**.

    2.  Select **Attach file** link.

    3.  Select the file to be attached.

    4.  Select **Attach**.

    5.  Select **Submit**.

    For own paper based amendment request, Version 1.0 of the amendment document is generated and listed in the Contract Document tab and the request moved to New state.


## Result

An amendment request is submitted in the New state and a contract request is created for the contract fulfiller to work on it.

**Parent Topic:**[Initiating a contract or amendment request](cncore-initiate-contract.md)


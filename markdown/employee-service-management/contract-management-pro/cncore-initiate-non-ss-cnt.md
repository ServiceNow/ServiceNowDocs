---
title: Initiate a non-self-served contract request
description: As a case owner or fulfiller, initiate the submission of contracts when you want third-party based contract documents to be sent for review.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Initiating a contract or amendment request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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

    ![Initiate contract window to populate the contract request details.](../image/cmpro-initiate-tpc.png "Initiate own-paper contract")

5.  In the **Type** field, specify whether the contract request is for single contract or multiple contracts.

    If you select **Single contract**, the **Contract type** field appears.

6.  In the **Contract type** field, select the type of contract for which the contract request is created.

7.  In the **Signature type** drop-down list, select the signature type for the contract document.

8.  In the **Start date** field, specify the contract start date.

9.  In the **End date** field, specify the contract end date.

    The End date should be later than the Start date.

10. Select **Initiate**.


## Result

A contract request is initiated and opens in a new tab displaying the contract request details.

If there are validation errors, the contract request is created in the Draft state. If there are no validation errors, the contract request is created in the New state.

## What to do next

Add contract documents and submit the contract request. For more information, see [Add contract documents to non-self-served contract request](cncore-nss-add-cont-doc.md).

**Parent Topic:**[Initiating a contract or amendment request](cncore-initiate-contract.md)


---
title: Initiate a third-party paper contract request
description: Initiate a third-party paper contract request linked to a parent record such as a purchase requisition or sourcing event. Third-party paper contracts are external contracts uploaded for review and signature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-initiate-non-ss-cnt.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-09-20"
reading_time_minutes: 2
breadcrumb: [Parent-linked contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate a third-party paper contract request

Initiate a third-party paper contract request linked to a parent record such as a purchase requisition or sourcing event. Third-party paper contracts are external contracts uploaded for review and signature.

## About this task

After you submit a standalone contract request, it is automatically assigned to a group or user based on the default assignment rule. A contract fulfiller can assign a contract request to themselves. A group manager can assign a contract request to any member of the assignment group.

## Before you begin

Role required: sn\_cm\_core.contract\_user, sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Open the parent record \(purchase requisition or sourcing event\).

2.  Select **Initiate Contract**.

    The Initiate Plug and Play modal opens.

3.  In the **Request type** field, select **New contract**.

4.  In the **Company** list, select the company.

5.  In the **Type of paper** drop-down list, select **Third-party paper**.

    \[Omitted image "cmpro-initiate-tpc.png"\] Alt text: Initiate contract window to populate the contract request details.

6.  In the **Type** field, specify whether the contract request is for single contract or multiple contracts.

    If you select **Single contract**, the **Contract type** field appears.

7.  In the **Contract type** field, select the type of contract for which the contract request is created.

8.  In the **Signature type** drop-down list, select the signature type for the contract document.

9.  In the **Start date** field, specify a future date as the contract start date.

10. In the **End date** field, specify the contract end date.

    The End date should be later than the Start date.

11. Select **Initiate**.

    A contract request is initiated and opens in a new tab displaying the contract request details.

12. Add contract documents.

    1.  In the Contract Document tab, select **Attach document**.

    2.  For multiple contract type request, in the **Select contract type** drop-down, select the type of contract.

    3.  Select **Attach file** link.

    4.  Select the file to be attached.

    5.  Select **Attach**.

    The selected file is attached and listed in the Contract Documents related list.

13. Select **Submit** to submit the request.


## Result

The contract request is created in the New state.

## What to do next

Add contract documents and submit the contract request. For more information, see [Add contract documents to non-self-served contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-nss-add-cont-doc.md).

**Parent Topic:**[Parent-linked contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-contract.md)


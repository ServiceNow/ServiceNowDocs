---
title: Initiate a renewal request from a parent record
description: Initiate a renewal request linked to a parent record such as a purchase requisition or sourcing event. Renewal requests extend or replace existing contracts that are active or expired.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-initiate-renewal.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 3
keywords: [Renewal request, Initiate renewal, Plug and play, Previous contract]
breadcrumb: [Parent-linked contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate a renewal request from a parent record

Initiate a renewal request linked to a parent record such as a purchase requisition or sourcing event. Renewal requests extend or replace existing contracts that are active or expired.

## About this task

Use the **Initiate contract** modal to create a renewal request. When you select **Renewal** as the request type, the modal lets you identify the contract that is being renewed and set the effective dates of the renewed contract. A contract management request \(CMR\) with the request type **Renewal** is created when you initiate the request.

## Before you begin

-   A contract is available for renewal only when it is in the Active or Expired state and has an end date. Cancelled and draft contracts, and active contracts without an end date, cannot be selected as the previous contract.
-   Verify you have a contract configuration with the request type set as renewal to copy values from renewal request to the contract repository. For more information, see [Create a contract configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-contract-config.md).
-   Verify you have a active contract template rule to identify an active published renewal document template to be used for generating the contract document for a renewal request. For more information, see [Configure contract template rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-config-template-rules.md).

Role required: sn\_cm\_core.contract\_user, sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Open the parent record \(purchase requisition or sourcing event\).

2.  Select **Initiate Contract**.

    The Initiate Plug and Play modal opens.

3.  In the **Request type** list, select **Renewal**.

4.  In the **Company** list, select the company.

5.  In the **Previous Contract** field, search for and select the contract that is being renewed.

    -   This field is optional.
    -   The list displays active contracts with an end date and expired contracts. If a company is specified, the list shows contracts for that company only; otherwise, all eligible contracts are listed.
    -   A contract with a renewal already in progress, or a completed renewal, is listed but can't be selected.
    -   If you do not select a contract now, a contract fulfiller can link the previous contract later.
6.  In the **Type of paper** list, select **Own paper** or **Third party paper**.

    A renewal supports a single contract for third-party paper.

7.  In the **Contract type** list, verify or select the type of contract.

    When you select a previous contract, the contract type is populated automatically. If you do not select a previous contract, select the contract type manually.

8.  In the **Signature type** list, select the signature type for the contract document.

    For more information about the signature flow, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

9.  In the **Start date** field, select the date on which the renewed contract takes effect.

    If you selected a previous contract, the start date is automatically set to the day after that contract's end date. Otherwise, enter a start date later than the previous contract's end date.

10. In the **End date** field, select the date on which the renewed contract ends.

    The end date must be later than the start date.

11. Select **Initiate**.

    A CMR is created with the request type **Renewal**. The Previous contract field is automatically populated with the contract record selected while initiating the request.

    For own paper based renewal request, Version 1.0 of the renewal document is generated and listed in the Contract Document tab and the request moved to Work in progress state.

    For third party paper, request is created in Draft state. Add documents and submit the request to move the request to New state.

12. For third-party paper renewal request, attach contract documents and submit the request.

    1.  In the Contract Document tab, select **Attach Document**.

    2.  Select **Attach file** link.

    3.  Select the file to be attached.

    4.  Select **Attach**.

    5.  Select **Submit**.


## Result

A renewal request is submitted for the contract fulfiller to work on it.

**Parent Topic:**[Parent-linked contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-contract.md)


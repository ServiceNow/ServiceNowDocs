---
title: Initiate an amendment request
description: Initiate an amendment request linked to a parent record such as a purchase requisition or sourcing event. Amendment requests modify existing active contracts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-initiate-amedment.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 4
breadcrumb: [Parent-linked contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate an amendment request

Initiate an amendment request linked to a parent record such as a purchase requisition or sourcing event. Amendment requests modify existing active contracts.

## About this task

A sample workflow while submitting on an amendment request would be:

1.  Initiate an amendment request from the workspace using the Initiate contract option.
2.  Enter amendment details and submit the request.

The initiated amendment is assigned according to an assignment rule or manually by a contract fulfiller or a group manager. The contract administrator can modify the assignment rule to specify the group to which the contract request should be assigned.

## Before you begin

-   Amendment requests can only be submitted for contracts in the Active state. If a contract is in Draft state and Awaiting Review substate, manually approve it before submitting an amendment request. For more information on how to approve a contract, see [Approve contracts to allow amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cmpro-approve-draft-cntr.md).
-   To copy field values from the parent contract request to the amendment request, configure the ContractManagementExt extension point. For more information, see [Copy fields from parent request to amendment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-cpy-fld-parent-amedreq.md).
-   Verify you have a contract configuration with the request type set as amendment to copy values from amendment request to the contract repository. For more information, see [Create a contract configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-contract-config.md).
-   Verify you have a contract template rule to identify the amendment document template to be used for generating the contract document for an amendment request. For more information, see [Configure contract template rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-config-template-rules.md).

Role required: sn\_cm\_core.contract\_user, sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Open the parent record \(purchase requisition or sourcing event\).

2.  Select **Initiate Contract**.

    The Initiate Plug and Play modal opens.

3.  In the **Request type** dropdown, select Amendment.

4.  In the **Company** list, select the company.

5.  In the **Contract** field, search for and select the contract to amend.

    This field is optional. Only active contracts for the selected company are listed, and contracts with an ongoing amendment are disabled from selection. When you select a contract, the contract type is automatically set. If you do not select a contract now, a contract fulfiller can link the parent contract later.

6.  Select type of paper in the **Type of paper** field.

    -   For own paper based amendment request, select **Own paper**.
    -   For third party paper based amendment request, select **Third Party Paper**. Amendment is supported for third-party contracts with a single contract type.
7.  When no contract was selected, select the type of contract for which the contract request is created in the **Contract type** field.

    This field is automatically populated when you select a contract in the **Contract** field. If you did not select a contract, select the contract type manually.\[Omitted image "cmpro-amend-initiate.png"\] Alt text: Use initiate contract modal from the workspace to submit an contract amendment request

8.  In the **Signature type** drop-down list, select the signature type for the contract document.

    For more information on the signature flow, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-signature-workflow.md)

9.  In the **Amendment description** field, enter the details of the changes required to the existing contract document and any other details.

10. In the **Effective date** field, select a date to indicate when the amendment takes effect.

    The effective date must be a future date and before the contract end date.

11. Select **Initiate**.

    -   A CMR is created with the request type **Amendment**. The Parent contract field is automatically populated with the contract record selected while initiating the request.
    -   For own paper based amendment request, Version 1.0 of the amendment document is generated and listed in the Contract Document tab and the request moved to New state.
    -   For third party paper, request is created in Draft state. Add contract documents and submit the request to move the request to Work in progress.
    -   Field values from the parent contract request are copied to the amendment request as per the configuration in the ContractManagementExt extension point.
12. For third-party paper amendment request, attach contract documents and submit the request.

    1.  In the Contract Document tab, select **Attach Document**.

    2.  Select **Attach file** link.

    3.  Select the file to be attached.

    4.  Select **Attach**.

    5.  Select **Submit**.


## Result

An amendment request is submitted for the contract fulfiller to work on it.

**Parent Topic:**[Parent-linked contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-contract.md)


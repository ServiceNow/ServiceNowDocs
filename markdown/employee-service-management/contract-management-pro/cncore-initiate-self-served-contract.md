---
title: Initiate an own paper contract request
description: Initiate an own paper contract request linked to a parent record such as a purchase requisition or sourcing event. Own paper contracts use predefined templates to generate contract documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-initiate-self-served-contract.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-09-20"
reading_time_minutes: 2
breadcrumb: [Parent-linked contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate an own paper contract request

Initiate an own paper contract request linked to a parent record such as a purchase requisition or sourcing event. Own paper contracts use predefined templates to generate contract documents.

## Before you begin

Before submitting a contract request, verify the following configurations are available and active:

-   Contract type
-   Published contract template
-   Contract template rule

For more information, see [Create a contract type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-create-contract-type.md), [Configure templates for a contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-document-templates.md), and [Configure contract template rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-config-template-rules.md).

Role required: sn\_cm\_core.contract\_user or sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Open the parent record \(purchase requisition or sourcing event\).

2.  Select **Initiate Contract**.

    The Initiate Plug and Play modal opens.

3.  In the **Request type** field, select **Contract**.

4.  In the **Company** list, select the company.

5.  In the **Type of paper** drop-down list, select **Own paper**.

    \[Omitted image "cmpro-initiate-own-paper.png"\] Alt text: Initiate contract window to populate the contract request details.

6.  In the **Contract type** drop-down list, select the type of contract you want to generate.

7.  In the **Signature type** drop-down list, select the signature type for the contract document.

8.  In the **Start date** field, specify a future date as the contract start date.

9.  In the **End date** field, specify the contract end date.

    The End date should be later than the Start date.

10. Select **Initiate**.

    If you do not have an active contract template for the selected contract type, an error is displayed.


## Result

A contract request is initiated and opens on a new tab displaying the contract request details.

If there are validation errors, the contract request is created in **Draft** state. If there are no validation errors, the contract request is created in **Work in progress** state.

A contract fulfiller can assign a contract request to themselves. A group manager can assign a contract request to any member of the assignment group. A contract fulfiller can also users to Collaborators and Watch list.

## What to do next

The next steps depend on whether there were validation errors:

-   If there were validation errors, complete the details and resubmit the contract request. For more information, see [Resolve the failure to submit a self-serve contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sync-signatories-fulfiller.md).
-   If there were no validation errors, you can proceed to work on the contract request. For more information see, [Work on self-served contract requests as a contract user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-work-ss-cntr-request-user.md) and [Work on requests as a contract fulfiller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-work-ss-cntr-request-fulfiller.md).

**Parent Topic:**[Parent-linked contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-contract.md)


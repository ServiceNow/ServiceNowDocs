---
title: Contract, amendment and renewal requests
description: Contract Management Pro supports initiation of Own paper and Third-Party paper based new contract, amendment and renewal requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-expl-ss-nss-contracts.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-10-06"
reading_time_minutes: 3
keywords: [Own paper contract, Third party paper contract, Self-served contract, Non-self served contract, Contract templates]
breadcrumb: [Explore, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract, amendment and renewal requests

Contract Management Pro supports initiation of Own paper and Third-Party paper based new contract, amendment and renewal requests.

## Contract requests

Contract requests are either standalone or linked to a parent record.

-   **Standalone requests**

    Contract requests initiated directly without a parent record. Entry points include the Contract Workspace, contract request listing pages, the Employee Center, and business unit workspaces.

-   **Parent-linked requests**

    Contract requests tied to a business unit entity. Entry points include purchase requisitions and sourcing events.


Regardless of the entry point, you can submit a new contract, amendment, or renewal request using own paper or third-party paper workflows.

## Request types

-   **New contract requests**

    Submit a request to create a new contract.

-   **Amendment requests**

    Modify, add, or remove specific terms or clauses in an active contract due to business or regulatory changes. Amendment requests can only be submitted for contracts in the Active state. If a contract is in Draft state, approve it before submitting an amendment request. The amendment request is automatically linked to the original contract.

-   **Renewal requests**

    Extend a contract that is approaching or past its expiration date, with the option to update terms. You can submit a renewal request for an expired or active contract with an end date. The renewal request is automatically linked to the previous contract.


Both amendment and renewal workflows support own paper and third-party paper requests. While submitting a request, select the **Type of paper** from the intake form.

**Note:** Third-party amendments and renewals are supported only for contract requests with a single contract type. Multi-contract type requests aren't supported.

For more information, see:

-   [Contract amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-amend-landing.md)
-   [Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-renewal-landing.md)

The **Request type** field identifies the request as **New contract**, **Amendment**, or **Renewal**. The field appears in the contract details and list view pages.

\[Omitted image "cmpro-amend-req-type-field.png"\] Alt text: Request type field in the contract details page

\[Omitted image "cmpro-amend-list-reqtype.png"\] Alt text: Request type field in the contract list view

The **Request type** field is also available in the following base system configurations \(when demo data is installed\) to indicate whether the configuration applies to a new contract, amendment, or renewal request:

-   Contract Template Rules
-   Contract Configurations

## Types of paper supported

-   **Own paper**

    Own paper contract requests use contract templates based on the company's own paper. Templates save time, reduce manual drafting, and help maintain consistency with the company's contract guidelines. For example, you can create a template to generate a non-disclosure agreement. For more information, see [Own paper contract requests]().

-   **Third-party paper**

    Third-party paper contract requests don't use contract templates. You can submit third-party contract documents for review without creating or configuring templates. A single request supports review of multiple contract and supporting documents. For more information, see [Third-Party paper contract request]().


## Parallel amendment and renewal requests

You can submit both amendment and renewal requests for the same contract, and both are processed in parallel without blocking each other.

When both requests are active on the same contract, review the following to avoid conflicts:

-   Contract dates to prevent overlapping effective periods between the amended contract and the renewed contract
-   Terms and pricing changes in both requests
-   Effective dates and expiration dates

You must manually reconcile any conflicts between the amended original contract and the renewed contract.

For more information about how amendment and renewal requests interact, see [Amendment and renewal interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-amend-renewal-int.md).


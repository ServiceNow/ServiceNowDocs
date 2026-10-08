---
title: Contract renewals
description: The contract renewal workflow enables you to initiate, manage, and track the renewal of an existing contract as a dedicated request type, and to maintain the link between a previous contract and its renewed contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/legal-service-delivery/snlc-renewal-landing.html
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [Renewal request, Renew contract, Renewal workflow, Previous contract, Renewal history]
breadcrumb: [Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Contract renewals

The contract renewal workflow enables you to initiate, manage, and track the renewal of an existing contract as a dedicated request type, and to maintain the link between a previous contract and its renewed contract.

You can renegotiate, review, approve, and sign expiring contracts through the workflow. The system tracks each renewed contract as a new contract record and links it to the parent contract, giving all end-to-end visibility of the renewal process.

When contract is signed for a renewal request, a new contract record is created automatically. Field values are populated according to the contract configuration mapping for the request, and users who had access to the renewal request receive equivalent access to the new contract record.

You can use the **Contract Amendment and Renewal request** intake form available in the Employee Center to submit an renewal request.

\[Omitted image "lsd-renew-rp.png"\] Alt text: Use the Amendment request record producer from Employee Center to submit an contract renewal request

## Distinguish request types

The **Request type** field identifies the type of contract request: **New contract** for contract requests, **Amendment** for amendment requests, and **Renewal** for renewal requests.

The Request type field is displayed in the contract details and list view pages making it easy to differentiate between the request types.

\[Omitted image "cmpro-amend-req-type-field.png"\] Alt text: Request type field to differentiate between different requests

\[Omitted image "cmpro-amend-list-reqtype.png"\] Alt text: Request type field to distinguish between requests.

This field is also available in the following base system configurations \(when demo data is installed\) to indicate the request type the configuration is applicable to:

-   Contract Template Rules
-   Contract Configurations

## Types of paper for renewal

The renewal workflow supports both own-paper and third-party paper renewal requests.

**Note:** Third-party paper renewals are supported only for single contracts. Multi-contract third-party paper renewals are not supported.

While submitting a renewal request, you can select the **Type of paper** on the intake form.

\[Omitted image "lsd-renew-type.png"\] Alt text: Select renewal type

## View contract renewal details

The following tabs are available within the contract repository record to provide renewal details:

-   Contract documents: Provides access to all signed documents related to the contract, including those generated or updated as part of renewal processes.
-   Contract requests: Displays all contract, amendment and renewal requests associated with the contract.
-   Contract history: Displays contract renewal history, including linked contracts, dates, and status for each contract.

\[Omitted image "cmpro-renew-tabs-cntr.png"\] Alt text: Contract repository record showing renewal related details

## ServiceNow Otto for Contract Management Pro features for renewals

Existing ServiceNow Otto for Contract Management Pro features work for renewal requests when the corresponding use case mapping is configured for the Renewal request type. When demo data is installed, the base system use case mappings for contract analysis, metadata extraction, and obligation extraction include the Renewal request type. Contract analysis, metadata extraction, obligation extraction, contract summarization, smart Q&amp;A, and conversational search are available on renewal requests and renewed contract records in the applicable states. For more information, see [AI capabilities in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md).

## Amendment and renewal interactions

You can submit both amendment and renewal requests for the same contract. The system allows parallel processing without blocking either request type. When you submit a renewal request while an amendment is in progress, or submit an amendment request while a renewal is in progress, the system displays warnings about potential conflicts.

For more information about how amendment and renewal requests interact, see [Amendment and renewal interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-amend-renewal-int.md).

## Renewal tasks

-   [Submit a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-initiate-req.md)
-   [View and track a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-view-details.md)
-   [Manage the signature of a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-sign.md)
-   [Work on a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-work.md)

-   **[Submit a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-initiate-req.md)**  
Submit a renewal request from the Employee Center to extend or replace an existing contract.
-   **[View and track a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-view-details.md)**  
View the details of a renewal request from the Employee Center ticket page, and view the renewal history and contract details in the executed contract record after signing is complete.
-   **[Manage the signature of a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-sign.md)**  
Send an own-paper renewal request for signature, resend or cancel the signature request, and upload the signed contract from the Employee Center ticket page.
-   **[Work on a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-work.md)**  
Review and work on a renewal request for an existing contract, from assignment through review, approval, and signature to the executed renewed contract.

**Parent Topic:**[Use Contract Management Pro for Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-use-sn-legal-cont-landing.md)

**Related topics**  


[Non-disclosure agreement requests]()

[Third-party contract review requests]()

[Contract amendments]()

[Linking parent-child contracts]()

[Internal review overview]()

[Signature workflow for a request]()

[Cancel a legal request]()

[View and download a signed contract document]()

[Manage Contract Management Pro for Legal Service Delivery]()


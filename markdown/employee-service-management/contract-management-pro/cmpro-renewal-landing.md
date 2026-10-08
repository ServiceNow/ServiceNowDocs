---
title: Contract renewals
description: The contract renewal workflow enables you to initiate, manage, and track the renewal of an existing contract as a dedicated request type, and to maintain the link between a previous and renewed contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-renewal-landing.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Renewal request, Renew contract, Renewal workflow, Previous contract, Renewal history]
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract renewals

The contract renewal workflow enables you to initiate, manage, and track the renewal of an existing contract as a dedicated request type, and to maintain the link between a previous and renewed contract.

You can renegotiate, review, approve, and sign expiring contracts through the workflow. The system tracks each renewed contract as a new contract record and links it to the parent contract, giving all end-to-end visibility of the renewal process.

When contract is signed for a renewal request, a new contract record is created automatically. Field values are populated according to the contract configuration mapping for the request, and users who had access to the renewal request receive equivalent access to the new contract record.

## Types of paper for renewal

The renewal workflow supports both own-paper and third-party paper renewal requests.

**Note:** Third-party paper renewals are supported only for single contracts. Multi-contract third-party paper renewals are not supported.

While submitting a renewal request, you can select the **Type of paper** on the intake form.

\[Omitted image "cmpro-renew-type-paper-initiate.png"\] Alt text: Type of paper options for a renewal request

## View contract renewal details

The following tabs are available within the contract repository record to provide renewal details:

-   Contract documents: Provides access to all signed documents related to the contract, including those generated or updated as part of renewal processes.
-   Contract requests: Displays all renewed and subsequent amendment requests on the renewed contract.
-   Contract history: Displays contract renewal history, including linked contracts, dates, and status for each contract. The current contract repository record is highlighted.

\[Omitted image "cmpro-renew-tabs-cntr.png"\] Alt text: Contract repository record showing renewal-related details

## ServiceNow Otto for Contract Management Pro features for renewals

Existing ServiceNow Otto for Contract Management Pro features work for renewal requests when the corresponding use case mapping is configured for the Renewal request type. When demo data is installed, the base system use case mappings for contract analysis, metadata extraction, and obligation extraction include the Renewal request type. Contract analysis, metadata extraction, obligation extraction, contract summarization, smart Q&amp;A, and conversational search are available on renewal requests and renewed contract records in the applicable states. For more information, see [AI capabilities in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md).

## Amendment and renewal interactions

You can submit both amendment and renewal requests for the same contract. The system allows parallel processing without blocking either request type. When you submit a renewal request while an amendment is in progress, or submit an amendment request while a renewal is in progress, the system displays warnings about potential conflicts.

For more information about how amendment and renewal requests interact, see [Amendment and renewal interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-amend-renewal-int.md).

## Renewal action items

-   [Submit a standalone renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-renewal.md)
-   [View renewal details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-renewal-history.md)
-   [Manage signature in own-paper requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-own-send-sign.md)
-   [Work on a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-renewal-fulfiller.md)

-   **[Work on a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-renewal-fulfiller.md)**  
Review and work on a renewal request for an existing contract, from assignment through review, approval, and signature to the executed renewed contract.
-   **[View renewal details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-renewal-history.md)**  
View the renewal details in the contract repository record.
-   **[Amendment and renewal interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-amend-renewal-int.md)**  
Understand how amendment and renewal requests interact on the same contract, and the messages that guide you when they occur in sequence or in parallel.

**Parent Topic:**[Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-use-cmpro.md)


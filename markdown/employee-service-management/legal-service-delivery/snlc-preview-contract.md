---
title: View and download a signed contract document
description: View and download a signed contract document.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# View and download a signed contract document

View and download a signed contract document.

When all signatories have signed a contract document, it’s considered as the final contract document and is stored in the Legal Contract \[sn\_lg\_cnt\_repository\] table.

Access to a contract document is based on the following user roles and conditions:

-   Group manager, Assigned to user and collaborator have edit access to the contract repository.
-   Contract fulfiller belonging to the same assignment group has view access to the contract repository.
-   Contract fulfiller not in assignment group do not have access to the to the contract repository.
-   A Contracts Fulfiller can view and update contract repository record
-   Only a Contracts Administrator can delete contract repository record.
-   Requesters can view only the contract documents for which they submitted the legal request.
-   Users can view only contract documents for which they have been added to the watch list of the corresponding legal requests.

When multiple contract documents are attached, a separate contract repository record is created for each contract type.

-   **[View and download a signed contract document as a legal fulfiller](snlc-preview-contract-fulfiller.md)**  
View and download a signed contract document as a legal fulfiller.
-   **[View and download a signed contract document as a legal user](snlc-preview-contract-user.md)**  
View and download a signed contract document as a legal user.

**Parent Topic:**[Use Contract Management Pro for Legal Service Delivery](../concept/snlc-use-sn-legal-cont-landing.md)

**Related topics**  


[Non-disclosure agreement requests](../concept/snlc-request-nda-1.md)

[Third-party contract review requests](../concept/snlc-request-third-party-contract-1.md)

[Contract amendments](../concept/snlc-amend-req-landing.md)

[Linking parent-child contracts](../concept/snlc-linking-parent-child.md)

[Internal review overview](snlc-expert-review.md)

[Cancel a legal request](snlc-cancel-request-tpc.md)

[View contract requests](snlc-view-contract-requests.md)

[Manage Contract Management Pro for Legal Service Delivery](../concept/snlc-manage-sn-legal-contracts.md)


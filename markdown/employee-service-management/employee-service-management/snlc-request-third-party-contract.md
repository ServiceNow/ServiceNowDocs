---
title: Third-party contract review requests
description: Employees can submit legal requests for review of third-party contracts by the legal team.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Third-party contract review requests

Employees can submit legal requests for review of third-party contracts by the legal team.

## Features

Third-party review requests include the following features:

-   Ability to submit a third-party document for review.
-   Ability to upload multiple contract and supporting documents for review.
-   Get review and feedback from the internal subject matter experts on contract documents
-   Electronic signature integrations with Adobe Acrobat Sign and Docusign.
-   Support for storing contract documents in your ServiceNow instance or external storage systems such as Microsoft OneDrive and Google Drive.
-   Legal contracts repository containing the metadata of signed contract documents.
-   Support for a configurable system property to generate a certification of completion.

## Third-party contract review request workflow

As a legal fulfiller on the legal team, you work on assigned third-party review requests by completing the following activities:

1.  The legal user creates a third-party contract review request.
2.  The legal user uploads a single or multiple contracts and their supporting documents and classifies them.
3.  The contract fulfiller reviews the contract document attached to the legal request.
4.  If necessary, the contract fulfiller reclassifies the contract and supporting documents.
5.  If an expert review or feedback is required from internal teams, the contract fulfiller initiates internal review process.
    1.  The contract fulfiller submits a review task for internal review.

        **Note:** You can create parallel review tasks for the same contract document for different reviewer groups. However, you cannot create a review task for the same document with the same reviewer group if another active task already exists.

    2.  The contract reviewer is assigned the review task
    3.  If the information is incomplete, the contract reviewer requests more information from the contract fulfiller.
    4.  If a request for more information was submitted, the contract fulfiller shares the information.
    5.  The contract reviewer reviews the document, accept, reject, or proposes edits, and adds comments.
    6.  The contract reviewer reviews the contract and provides feedback. If a revised document is available, it is also shared with the contract fulfiller.
    7.  The contract fulfiller receives updated document and makes the necessary changes based on the feedback.
        -   For internal storage - If any changes are required, a new document version is created after finalizing the document.
        -   For external storage - Reviewers collaborate on the contract document revision online in real time. Once the review is complete, the fulfiller can finalize the contract document that is available online or create a new offline version with the changes.
6.  The contract fulfiller uploads the revised contract to the contract request.
7.  The contract fulfiller emails the revised contract document to third-party contacts.
8.  View responses from third-party contacts in the activity stream of the contract request.

    Multiple iterations of revisions between your company and the third party might be necessary before the contract document is finalized by all parties. The review process may be conducted again with different reviewer groups.

9.  The contract fulfiller initiates an ad-hoc approval from the stakeholders. If the review reveals any required changes, the changes are made and a new document revision is created. The contract document can be sent for signature only when it has been approved.
10. The contract fulfiller prepares for signatures by specifying the order in case of multiple contract documents, adding fields required in case of e-signature and sends the contract document for signature.
11. Signatories review the contract document.
    -   If no change is required, the contract document is signed by all the signatories.
    -   If any changes are required, signature is declined, the user who is working on the contract request generates a new document and resends it for signature.
12. The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the contracts repository.

For e-signatures, after all signatories have signed the contract document, it’s stored on the ServiceNow instance or an external storage system. If an external storage is configured, the signed contract is stored in it and referenced in the contract repository.

For wet signatures, after all signatories have signed and returned the contract document, the legal fulfiller uploads the signed contract to the contract request. The document is then stored in the contract repository.

The requester and legal department members can access the signed contract document from the Legal Contracts repository.


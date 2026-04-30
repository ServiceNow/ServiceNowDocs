---
title: Use non-self-served contract request
description: Use Contract Management Pro to submit non self-served contract requests for review of contracts based on third-party templates.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Use non-self-served contract request

Use Contract Management Pro to submit non self-served contract requests for review of contracts based on third-party templates.

## Features

Non-self-served contract requests include the following features:

-   Ability to submit a third-party document for review.
-   Ability to upload multiple contract and supporting documents for review.
-   Get review and feedback from the internal subject matter experts on contract documents.
-   Electronic signature integrations with Adobe Acrobat Sign and Docusign.
-   Support for storing contract documents in your ServiceNow instance or external storage systems such as Microsoft OneDrive and Google Drive.
-   Contracts repository containing the metadata of signed contract documents.
-   Support for a configurable system property to generate a certification of completion.

## Non-self-served contracts request workflow

A workflow for non-self-served contract request might progress as follows:

1.  The Contract requester initiates a contract request from the workspace. For more information, see [Initiating a contract or amendment request](../task/cncore-initiate-contract.md).
2.  A contract request is created in the Draft state.
3.  The Contract requester uploads a single contract or multiple contracts and their supporting documents and classifies them.
4.  The contract fulfiller views the contract document attached to the contract request.
5.  If necessary, the contract fulfiller reclassifies the contract and supporting documents.
6.  If an expert review or feedback is required from internal teams, the contract fulfiller initiates an internal review process.
    1.  The contract fulfiller submits a review task for internal review.

        **Note:** You can create parallel review tasks for the same contract document for different reviewer groups. However, you cannot create a review task for the same document with the same reviewer group if another active task exists.

    2.  The contract reviewer is assigned the review task
    3.  If the information is incomplete, the contract reviewer requests more information from the contract fulfiller.
    4.  If a request for more information was submitted, the contract fulfiller shares the information.
    5.  The contract reviewer reviews the document, accept, reject, or proposes edits, and adds comments.
    6.  The contract reviewer reviews the contract and provides feedback. If a revised document is available, it is also shared with the contract fulfiller.
    7.  The contract fulfiller receives an updated document and makes the necessary changes based on the feedback.
        -   For internal storage - If any changes are required, a new document version is created after finalizing the document.
        -   For external storage - Reviewers collaborate on the contract document revision online in real time. Once the review is complete, the fulfiller can finalize the contract document that is available online or create a new offline version with the changes.
7.  The contract fulfiller uploads the revised contract to the contract request.
8.  The contract fulfiller emails the revised contract document to third-party contacts.
9.  The contract fulfiller views the responses from the third-party contacts in the activity stream of the contract request.

    Multiple iterations of revisions between your company and the third party might be necessary before the contract document is finalized by all parties. The review process may be conducted again with different reviewer groups.

10. The contract fulfiller initiates an ad-hoc approval from the stakeholders. If the review reveals any required changes, the changes are made and a new document revision is created. The contract document can be sent for signature only when it has been approved.
11. If there are multiple contract documents, the contract fulfiller prepares for signatures by specifying the order. If there's an e-signature, the contract fulfiller adds the required fields and sends the contract document for signature.
12. Signatories review the contract document.
    -   If no change is required, the contract document is signed by all the signatories.
    -   If any changes are required, the signature is declined, and the user who is working on the contract request generates a new document and resends it for signature.
13. The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the contracts repository.


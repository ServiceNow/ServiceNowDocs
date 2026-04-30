---
title: Use self-served contract request
description: Use Contract Management Pro to submit contract requests that will generate contract documents using a predefined contract template and template rules.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Use self-served contract request

Use Contract Management Pro to submit contract requests that will generate contract documents using a predefined contract template and template rules.

## Features

-   Contract templates with metadata, clauses, tables, and create business rules for selecting the most relevant template for a request.
-   Contract templates in Microsoft Word format enable easier contract review and editing for the contract fulfiller.
-   Electronic signature integrations with Adobe Acrobat Sign and Docusign.
-   Wet signature support for manual signing.
-   External storage integrations with Google Drive and Microsoft OneDrive for storing signed contract documents.
-   Centralized contracts repository containing the metadata of signed contract documents.
-   System property to generate a certification of completion for an electronically signed contract.

## Self-served contracts workflow

When a requester submits a self-served contract request, a contract document is created using a standard contract template based on the information from the request. The information from the request is inserted at the appropriate places in the template.

If needed, requesters can request specific changes in the generated contract document. The fulfiller can manage and process these requested changes to make necessary revisions to the contract document from a centralized location. Because contract documents are in Microsoft Word format, reviewing, editing, and finalizing the contract documents is easier than for documents in PDF or HTML format.

If the generated contract document doesn’t require any changes, the requester can send it to the signatories for an electronic signature. After all signatories have signed the contract document, it’s stored on the ServiceNow instance or an external storage system based on the configuration. The requester and contracts department members can access the signed contract document from the contracts repository.

A workflow for a self-served contract request might progress as follows:

1.  The Contract requester initiates a contract request. For more information, see [Initiating a contract or amendment request](../task/cncore-initiate-contract.md).
    -   If there are no validation errors, a contract request is created in the Work in progress state.
    -   If there are any signatory validation errors, the contract requester resolves them and resubmits the contract request.
2.  A contract document is generated from a contract template and the metadata, clauses, signatories, and tables are added dynamically according to predefined conditions.
3.  The contract requester edits the requests for any changes and creates a new version of the contract document by using the **Regenerate** or **Sync document** option.
4.  The contract requester views the contract document and does one of the following actions:
    1.  If no changes are required, the document is sent for signature.
    2.  If any changes are required, the contract requester submits a change request.
5.  Based on the change request, the contract fulfiller can take the following actions:
    1.  Initiates an internal review process.
        1.  The contract fulfiller submits a review task for an internal review.

            **Note:** The contract fulfiller can create parallel review tasks for the same contract document for different reviewer groups. However, the contract fulfiller can't create a review task for the same document with the same reviewer group if another active task already exists.

        2.  A contract reviewer group manager can assign the review task, or a contract reviewer can self-assign it.
        3.  The assigned contract reviewer starts working on the contract document.
        4.  If the information is incomplete, the contract reviewer requests more information from the contract fulfiller.
        5.  If a request for more information was submitted, the contract fulfiller shares the information.
        6.  The contract reviewer reviews the document, accepts or rejects redlines, proposes edits, and adds comments.
        7.  The contract reviewer completes the review and shares the updated contract document if available.
        8.  The contract fulfiller receives the updated document and makes the necessary changes based on the feedback.
            -   For internal storage: If any changes are required, a new document version is created after finalizing the document.
            -   For external storage: Reviewers collaborate on the contract document revision online in real time. After the review is complete, the fulfiller can finalize the contract document that is available online or create a new offline version with the changes.
    2.  The contract fulfiller initiates an ad-hoc approval from the stakeholders. If the review reveals any required changes, the changes are made and a new document revision is created.
    3.  After the document is finalized, the fulfiller sends the document to the requester.
6.  The contract requester previews the generated contract and, if no changes are required, sends it to the signatories. If changes are required, the review and revision process continues.
7.  If external storage is configured, contract documents are stored in it. Otherwise, they are stored in the ServiceNow instance.
8.  If any signatory declines the document, it is sent back to the requester to be reworked and the revision is sent for signature.
9.  The signed contract is attached to the contract request record.
10. The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the Contracts repository.

**Note:**

The contract requester can cancel a contract request when the state is in Draft, New, Awaiting Approval, Awaiting signature, or Work in progress.


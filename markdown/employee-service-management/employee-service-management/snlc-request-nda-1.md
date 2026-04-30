---
title: Non-disclosure agreement requests
description: Employees can submit legal requests for creating non-disclosure agreement \(NDA\) contracts with third parties such as vendors, customers, and partners. The legal department can manage and process these requested changes from a centralized location.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Non-disclosure agreement requests

Employees can submit legal requests for creating non-disclosure agreement \(NDA\) contracts with third parties such as vendors, customers, and partners. The legal department can manage and process these requested changes from a centralized location.

## Features

-   Contract templates with metadata and business rules for selecting the most relevant template for a request.
-   Microsoft Word format contract templates to enable easier editing for the contract fulfiller.
-   Self-service capability for creating and executing standardized NDA contracts.
-   Electronic signature integrations with Adobe Acrobat Sign and Docusign.
-   Wet signature support for manual signing.
-   External storage integrations with Google Drive and Microsoft OneDrive for storing signed contract documents.
-   Centralized legal contracts repository containing the metadata of signed contract documents.

## Non-disclosure agreement contract request workflow

When a requester submits a legal request, an NDA contract document is created using a standard contract template based on the information from the request. The information from the request is inserted at the appropriate places in the template.

Because contract documents are in Microsoft Word format, reviewing, editing, and finalizing the contract documents is easier than documents in PDF or HTML format.

If the generated NDA document doesn’t require any changes, the requester can send it to the signatories for an electronicor wetsignature. After all signatories have signed the contract document, it’s stored on the ServiceNow instance or an external storage system based on the configuration. The requester and legal department members can access the signed contract document from the Contracts repository.

A sample workflow for a non-disclosure agreement \(NDA\) contract request might progress as follows:

1.  Legal configurator sets up the foundation data for submitting an NDA request. For more information, see [Configure Contract Management Pro for Legal Service Delivery](snlc-config-sn-legal-contracts.md).
2.  Legal requester fills out the NDA intake request form.
3.  A contract request is initiated.
4.  Contract document is generated from a contract template and content is added dynamically per predefined conditions.
5.  Contract user edits the requests for any changes and creates a new version of the contract document using the **Regenerate** or **Sync document** option.
6.  The Contract requester views the contract document.
    1.  If no changes are required, the document is sent for signature.
    2.  If any changes are required, the contract requester submits a change request, which is sent to the contract fulfiller.
7.  Based on the change request, the contract fulfiller can take the following actions.
    1.  The contract fulfiller initiates an internal review process.
        1.  The contract fulfiller submits a review task for internal review.

            **Note:** You can create parallel review tasks for the same contract document for different reviewer groups. However, you cannot create a review task for the same document with the same reviewer group if another active task already exists.

        2.  A contract reviewer group manager can assign the review task, or a contract reviewer can self-assign it.
        3.  The assigned contract reviewer starts working on the contract document.
        4.  If the information is incomplete, the contract reviewer requests more information from the contract fulfiller.
        5.  If a request for more information was submitted, the contract fulfiller shares the information.
        6.  The contract reviewer reviews the document, accept or reject redlines, proposes edits, and adds comments.
        7.  The contract reviewer completes the review and shares the updated contract document if available.
        8.  The contract fulfiller receives updated document and makes the necessary changes based on the feedback.
            -   For internal storage - If any changes are required, a new document version is created after finalizing the document.
            -   For external storage - Reviewers collaborate on the contract document revision online in real time. Once the review is complete, the fulfiller can finalize the contract document that is available online or create a new offline version with the changes.
    2.  The contract fulfiller initiates an ad-hoc approval from the stakeholders. If the review reveals any required changes, the changes are made and a new document revision is created.
    3.  Once the document is finalized, fulfiller sends document to requester.
8.  The contract requester previews the generated contract and, if no changes are required, sends it to the signatories.
9.  All signatories submit the required signatures.
10. The signed contract is attached to the legal request record.
11. If an external storage is configured, the signed contract is stored in it and referenced in the contract repository.

-   **[Submit a legal request for a non-disclosure agreement](../task/snlc-submit-nda-request.md)**  
Submit a legal request for a non-disclosure agreement \(NDA\) with third parties such as vendors, customers, or partners.
-   **[Modify a non-disclosure agreement legal request](../task/snlc-modify-nda-req.md)**  
As a requester, modify the legal request for a non-disclosure agreement \(NDA\).
-   **[View and track non-disclosure agreement requests as a legal user](../task/snlc-view-legal-req-details.md)**  
View the details of a non-disclosure agreement request after it has been submitted and track the activities in the request.
-   **[Work on NDA legal requests](../task/snlc-work-on-contract-request.md)**  
As a member of the legal contracts support team, work on the legal request. Upload the revised document to the request and send the document to the requester from within the request.

**Parent Topic:**[Use Contract Management Pro for Legal Service Delivery](snlc-use-sn-legal-cont-landing.md)

**Related topics**  


[Third-party contract review requests](snlc-request-third-party-contract-1.md)

[Contract amendments](snlc-amend-req-landing.md)

[Linking parent-child contracts](snlc-linking-parent-child.md)

[Internal review overview](../task/snlc-expert-review.md)

[Cancel a legal request](../task/snlc-cancel-request-tpc.md)

[View and download a signed contract document](../task/snlc-preview-contract.md)

[View contract requests](../task/snlc-view-contract-requests.md)

[Manage Contract Management Pro for Legal Service Delivery](snlc-manage-sn-legal-contracts.md)


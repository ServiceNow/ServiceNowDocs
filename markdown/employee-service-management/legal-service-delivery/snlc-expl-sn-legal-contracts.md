---
title: Explore Contract Management Pro for Legal Service Delivery
description: Learn more about Contract Management Pro for Legal Service Delivery through a sample workflow and review the benefits it can provide.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Explore Contract Management Pro for Legal Service Delivery

Learn more about Contract Management Pro for Legal Service Delivery through a sample workflow and review the benefits it can provide.

## Contract Management Pro for Legal Service Delivery overview

With the Legal Contract Management Pro for Legal Service Delivery, you can configure and automate the legal contract lifecycle by creating contract document templates, clauses, and clause variations. The legal contract lifecycle enables you to submit, review, finalize, and manage legal contract and amendmentrequests. The integration also supports e-signatures and external storage systems.

## Contract Management Pro for Legal Service Delivery users

|User|Description|
|----|-----------|
|Contract Management Pro for Legal Service Delivery configurator|Contract Management Pro for Legal Service Delivery configurator can configure contract templates, external systems, and configuration rules.|
|Contract Management Pro for Legal Service Delivery administrator|Contract Management Pro for Legal Service Delivery administrator manages contract records, user roles, and system configurations.|
|Contract Management Pro for Legal Service Delivery fulfiller|Contract Management Pro for Legal Service Delivery fulfiller works on legal requests.|
|Legal User|Legal user submits legal and amendment requests and track their progress.|
|Contract user|Contract user initiates and tracks a contract request.|
|Contract fulfiller|Contract fulfiller work on contract request and initiates actions while fulfilling an assigned contract execution.|

## Non-disclosure agreement contract request workflow

![A flowchart illustrating the workflow of non-disclosure-agreement.](../../contract-mgmt-pro/image/mmasset0021153-nda-lsd-horizontal.png "Non-disclosure agreement request workflow")

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

## Third-party contract review request workflow

![A flowchart illustrating the workflow of third-party contract review.](../../contract-mgmt-pro/image/mmasset0021154-tpc-lsd-horizontal.png "Third-party contract review workflow")

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

## Contract Management Pro for Legal Service Delivery benefits

<table id="table_gjx_v3q_dyb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Submit, review, finalize, and manage legal contract requests. The legal department can manage and process these submitted legal requests for contracts from a centralized location.

</td><td>

[Contract Management Pro for Legal Service Delivery](snlc-expl-legal-contracts.md)

</td><td>

-   Legal user and contract user
-   Contract Management Pro for Legal Service Delivery contract fulfiller

</td></tr><tr><td>

Configure word document templates for contract to streamline and reduce the need for rework and maintain uniformity across generated contract documents. Set up dynamic content generation through mappings and conditions for clauses and tables.

</td><td>

[Word Document Templates](../../contract-mgmt-pro/concept/cncore-expl-wdt.md)

</td><td>

Contract configurator

</td></tr><tr><td>

Effectively manage a library of clause variations. Use clause variations to dynamically place content in a contract depending on the specified conditions.

</td><td>

[Clause Management](../../contract-mgmt-pro/concept/cncore-expl-clause-mgmt.md)

</td><td>

Contract configurator

</td></tr><tr><td>

Use Microsoft Word documents to add content controls that act as placeholders for the content. Word templates are easier to review, mark up, and modify.

</td><td>

[Microsoft Word add-in for ServiceNow Contracts](../../contract-mgmt-pro/concept/cncore-expl-snc-addin.md)

</td><td>

Contract configurator

</td></tr><tr><td>

Initiate and manage amendment requests.

</td><td>

[Contract amendments](snlc-amend-req-landing.md)

</td><td>

-   Legal user and contract user
-   Contract Management Pro for Legal Service Delivery fulfiller

</td></tr><tr><td>

Track and manage contract obligations to help ensure compliance and minimize risks.

</td><td>

[Obligation Management](../../contract-mgmt-pro/concept/cncore-obligation-management.md)

</td><td>

Obligation fulfiller or Obligation user

</td></tr><tr><td>

Use Now Assist in Contract Management to analyze contracts for non-standard and missing clauses, and extract information from signed contracts to add in the contract repository.

</td><td>

[Now Assist in Contract Management](../../contract-mgmt-pro/concept/cncore-now-assit-landing.md)

</td><td>

Now Assist contract fulfiller

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using , see:

-   [Configure Contract Management Pro for Legal Service Delivery](snlc-config-sn-legal-contracts.md)
-   -   [Non-disclosure agreement requests](snlc-request-nda-1.md)
-   [Third-party contract review requests](snlc-request-third-party-contract-1.md)
-   [Contract Management Pro for Legal Service Delivery reference](snlc-ref-sn-legal-contracts.md)

-   **[Contract Management Pro for Legal Service Delivery](snlc-expl-legal-contracts.md)**  
Contract Management Pro for Legal Service Delivery enables you to submit, review, finalize, and manage legal contract requests. The legal department can manage and process these submitted legal requests for contracts from a centralized location.

**Parent Topic:**[Contract Management Pro for Legal Service Delivery](snlc-mgmt-pro-landing-page.md)


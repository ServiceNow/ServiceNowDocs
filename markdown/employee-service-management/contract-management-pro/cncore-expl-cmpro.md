---
title: Explore Contract Management Pro
description: Learn more about the Contract Management Pro application through a sample workflow and review the benefits that it can provide.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Contract Management Pro, Employee Service Management]
---

# Explore Contract Management Pro

Learn more about the Contract Management Pro application through a sample workflow and review the benefits that it can provide.

## Contract Management Pro overview

Contract Management Pro is a contract management solution that's easy to use and adopt. You can use it to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.

The components of Contract Management Pro are:

-   [Contracts Core](cncore-expl-ccore.md)
-   [Microsoft Word add-in for ServiceNow Contracts](cncore-expl-snc-addin.md)
-   [Self-served and non-self-served contract requests](cncore-expl-ss-nss-contracts.md)

## Contract Management Pro benefits

|Benefit|Key feature|Role|
|-------|-----------|----|
|Effectively manage a library of clause variations.|[Clause Management](cncore-expl-clause-mgmt.md)|Contract configurator|
|Create contract templates or standard letters that are used to generate contracts or documents based on the values in the submitted request.|[Word Document Templates](cncore-expl-wdt.md)|Contract configurator|
|Add content controls that act as placeholders for the content in Microsoft Word documents on macOS systems and on Windows systems by using an add-in. Content controls can be added manually only on a Windows system.|[Microsoft Word add-in for ServiceNow Contracts](cncore-expl-snc-addin.md)|Contract configurator|
|Initiate self-served or non-self-served contract requests.|[Self-served and non-self-served contract requests](cncore-expl-ss-nss-contracts.md)|Contract user|
|Service a self-served contract request.|[Use a self-served contract request](cncore-request-ss-contract-1.md)|Contract user or Contract fulfiller|
|Revise, approve, and provide a signature for a non-self-served contract request.|[Use non-self-served contract request](cncore-req-nss-contract-1.md)|Contract user or Contract fulfiller|
|Get review and feedback from the internal subject matter experts on contract documents.|[Internal review overview](../task/cncore-expert-review.md)|Contract fulfiller or Contract reviewer|
|Get an insight on the volume of contract requests that are handled by your team.|[Using the Contracts Dashboard](../../../use/dashboards/application-content-packs/cncore-contracts-dashboard.md)|Contract fulfiller|
|Work with actionable widgets to categorize, prioritize, and efficiently work on contract requests.|[Contract Workspace](cncore-contract-workspace.md)|Contract user or Contract fulfiller|
|Track and manage contract obligations to help ensure compliance and minimize risks.|[Obligation Management](cncore-obligation-management.md)|Obligation user or Obligation fulfiller|
|Use Now Assist in Contract Management to analyze contracts for non-standard and missing clauses, and to extract information from signed contracts to add in the contract repository.|[Now Assist in Contract Management](cncore-now-assit-landing.md)|Now Assist contract fulfiller|

## Contract Management Pro workflow

The following sample end-to-end workflow shows how different users can work together to configure the foundation data and submit, review, and finalize contract requests.

A Contract Management Pro configurator takes the following actions to set up the end-to-end workflow:

1.  Creates the contract type and associates it with a contract model.
2.  Creates the clauses and their variations to be used in the document templates.
3.  Creates the document templates that are used to generate the contract document.
4.  Configures the placeholders for signatories.
5.  Completes the template mapping to automatically fill in information that is used in the contract template.
6.  Publishes the document template to make it available to generate contracts while submitting the contract request.
7.  Creates a template selection rule to identify the contract template to be used to generate the contract document for the contract request.
8.  Creates an internal signatory rule to map the signatory to a template by using signatory mappings.
9.  Defines the contract repository where contracts are stored and maps the data that was added to the contract document.
10. Creates a contract repository rule to configure the reminders for expiring contracts.
11. Configures the external storage to store the signed contract documents and their revisions.
12. Configures the electronic signature providers to enable signers to sign the contract documents electronically.

## Self-served contract request workflow

A workflow for a self-served contract request might progress as shown in this process:

1.  The Contract requester initiates a contract request. For more information, see [Initiating a contract request](../task/cncore-initiate-contract.md).
    -   If there are no validation errors, a contract request is created in the Work in progress state.
    -   If there are any signatory validation errors, the contract requester resolves them and resubmits the contract request.
2.  A contract document is generated from a contract template and the metadata, clauses, signatories, and tables are added dynamically according to predefined conditions.
3.  The contract requester edits the requests for any changes and creates a version of the contract document by using the **Regenerate** or **Sync document** option.
4.  The contract requester views the contract document and does one of the following actions:
    1.  If no changes are required, the document is sent for signature.
    2.  If any changes are required, the contract requester submits a change request.
5.  Based on the change request, the contract fulfiller can take the following actions:
    1.  Initiates an internal review process:
        1.  The contract fulfiller submits a review task for an internal review.

            **Note:** The contract fulfiller can create parallel review tasks for the same contract document for different reviewer groups. However, the contract fulfiller can't create a review task for the same document with the same reviewer group if another active task exists.

        2.  A contract reviewer group manager can assign the review task, or a contract reviewer can self-assign it.
        3.  The assigned contract reviewer starts working on the contract document.
        4.  If the information is incomplete, the contract reviewer requests more information from the contract fulfiller.
        5.  If a request for more information was submitted, the contract fulfiller shares the information.
        6.  The contract reviewer reviews the document, accepts or rejects redlines, proposes edits, and adds comments.
        7.  The contract reviewer completes the review and shares the updated contract document if available.
        8.  The contract fulfiller receives the updated document and makes the necessary changes based on the feedback:
            -   For internal storage: If any changes are required, a new document version is created after finalizing the document.
            -   For external storage: Reviewers collaborate on the contract document revision online in real time. After the review is complete, the fulfiller can finalize the contract document that is available online or create an offline version with the changes.
    2.  The contract fulfiller initiates an ad-hoc approval from the stakeholders. If the review reveals any required changes, the changes are made and a new document revision is created.
    3.  After the document is finalized, the fulfiller sends the document to the requester.
6.  The contract requester previews the generated contract and, if no changes are required, sends it to the signatories. If changes are required, the review and revision process continues.
7.  If external storage is configured, contract documents are stored in it. Otherwise, they’re stored in the ServiceNow instance.
8.  If any signatory declines the document, it’s sent back to the requester to be reworked and the revision is sent for signature.
9.  The signed contract is attached to the contract request record.
10. The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the Contracts repository.

## Non-self-served contract request workflow

A workflow for non-self-served contract request might progress as follows:

1.  The Contract requester initiates a contract request from the workspace. For more information, see [Initiating a contract request](../task/cncore-initiate-contract.md).
2.  A contract request is created in the Draft state.
3.  The Contract requester uploads a single contract or multiple contracts and their supporting documents and classifies them.
4.  The contract fulfiller views the contract document attached to the contract request.
5.  If necessary, the contract fulfiller reclassifies the contract and supporting documents.
6.  If an expert review or feedback is required from internal teams, the contract fulfiller initiates an internal review process.
    1.  The contract fulfiller submits a review task for internal review.

        **Note:** Parallel review tasks for the same contract document can be created for different reviewer groups. However, a review task for the same document with the same reviewer group can't be created if another active task exists.

    2.  The contract reviewer is assigned the review task
    3.  If the information is incomplete, the contract reviewer requests more information from the contract fulfiller.
    4.  If a request for more information was submitted, the contract fulfiller shares the information.
    5.  The contract reviewer reviews the document, accepts, rejects, or proposes edits, and adds comments.
    6.  The contract reviewer reviews the contract and provides feedback. If a revised document is available, it’s also shared with the contract fulfiller.
    7.  The contract fulfiller receives an updated document and makes the necessary changes based on the feedback:
        -   For internal storage: If any changes are required, a new document version is created after finalizing the document.
        -   For external storage: Reviewers collaborate on the contract document revision online in real time. After the review is complete, the fulfiller can finalize the contract document that is available online or create an offline version with the changes.
7.  The contract fulfiller uploads the revised contract to the contract request.
8.  The contract fulfiller emails the revised contract document to third-party contacts.
9.  The contract fulfiller views the responses from the third-party contacts in the activity stream of the contract request.

    Multiple iterations of revisions between your company and the third party might be necessary before the contract document is finalized by all parties. The review process may be conducted again with different reviewer groups.

10. The contract fulfiller initiates an ad-hoc approval from the stakeholders. If the review reveals any required changes, the changes are made and a new document revision is created. The contract document can be sent for signature only when it has been approved.
11. If there are multiple contract documents, the contract fulfiller prepares for signatures by specifying the order. If there’s an e-signature, the contract fulfiller adds the required fields and sends the contract document for signature.
12. Signatories review the contract document:
    -   If no change is required, the contract document is signed by all the signatories.
    -   If any changes are required, the signature is declined, and the user who is working on the contract request generates a new document and resends it for signature.
13. The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the contracts repository.


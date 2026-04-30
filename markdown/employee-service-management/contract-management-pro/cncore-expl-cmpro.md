---
title: Exploring Contract Management Pro
description: Learn more about the Contract Management Pro application through a sample workflow and review the benefits that it can provide.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Contract Template, Agreement Template, Contract Draft Template, Predefined Contract, Standard Contract Format, Legal Contract Template, Reusable Contract Template, Master Contract Template, Document templates, word content controls, ms word document templates, clause management, Word document templates, contract metadata extraction]
breadcrumb: [Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Exploring Contract Management Pro

Learn more about the Contract Management Pro application through a sample workflow and review the benefits that it can provide.

## Contract Management Pro overview

Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendmentrequests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.

## Contract Management Pro users

|User|Description|
|----|-----------|
|Contracts Core administrator|Contract administrator manages contract records, user roles, and system configurations.|
|Contracts Core configurator|Contract configurator manages the configurations related to Contract Management Pro. They configure contract templates, external systems, and configuration rules.|
|Contracts Core fulfiller|Contract fulfiller initiates actions while fulfilling an assigned contract execution. This includes tasks such as creating revisions, adding signers, and canceling signer assignments.|
|Contracts Core user|Contract users initiate and track contract and amendmentrequests.|
|Contract reviewer|Contract reviewers review contract documents, track review tasks, and use clause library to add appropriate clauses.|
|Contract report viewer|Contract report viewer views contract reports, analyse contract trends, and support data-driven decision making.|
|Contract report publisher|Contract report publisher publishes reports on Contracts Dashboard.|
|Obligation user|Obligation user submits obligation request.|
|Obligation fulfiller|Obligation fulfiller initiates actions while fulfilling an obligation. This includes tasks like create obligations, approve, reject, or cancel obligation tasks.|
|Obligation administrator|Provides administrative access to Obligation management and underlying data.|

## Self-served contract request workflow

The following image provides an overview of the self-served contract requests.

![A flowchart illustrating a self-served contract request workflow in Contract Management Pro.](../image/mmasset0021155-ss-cmpro-horizontal.png "Self-served request workflow")

1.  The contract requester initiates a contract request.
2.  A contract document is generated from a contract template and the metadata, clauses, signatories, and tables are added dynamically according to predefined conditions.
3.  The contract fulfiller views the contract document and does one of the following actions:
    1.  If no changes are required, gets approval from stakeholders. Sends the contract document for signature.
    2.  If any changes are required, uploads a new revision of document and gets approval from stakeholders before sending it for signature.
4.  If any signatory declines the document, it is sent back to the requester to be reworked and the revision is sent for signature.
5.  After all signatories have approved the document. The signed contract is attached to the contract request record.
6.  The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the Contracts repository.

## Non-self-served contract request workflow

The following image provides an overview of the non-self-served contract requests.

![A flowchart illustrating a non-self-served contract request workflow in Contract Management Pro.](../image/mmasset0021156-nss-cmpro-horizontal.png "Non-self-served request workflow")

A workflow for non-self-served contract request might progress as follows:

1.  The Contract requester initiates a contract request from the workspace.
2.  The Contract requester uploads a single contract or multiple contracts and their supporting documents and classifies them.
3.  The contract fulfiller views the contract document attached to the contract request.
4.  If necessary, the contract fulfiller reclassifies the contract and supporting documents.
5.  The contract fulfiller views the contract document and does one of the following actions:
    1.  If no changes are required, gets approval from stakeholders. Sends the contract document for signature.
    2.  If any changes are required, modifies the contract document, gets internal or ad-hoc approval if required. Uploads new revision of the contract document and sends for signature.
6.  If there are multiple contract documents, the contract fulfiller prepares for signatures by specifying the order. If there's an e-signature, the contract fulfiller adds the required fields and sends the contract document for signature.
7.  Signatories review the contract document.
    -   If no change is required, the contract document is signed by all the signatories.
    -   If any changes are required, the signature is declined, and the user who is working on the contract request generates a new document and resends it for signature.
8.  The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the contracts repository.

## Contract Management Pro benefits

|Feature|Benefit|Users|
|-------|-------|-----|
|[Word Document Templates](cncore-expl-wdt.md)|Configure word document templates for contract to streamline and reduce the need for rework and maintain uniformity across generated contract documents. Set up dynamic content generation through mappings and conditions for clauses and tables.|Contract configurator|
|[Clause Management](cncore-expl-clause-mgmt.md)|Effectively manage a library of clause variations. Use clause variations to dynamically place content in a contract depending on the specified conditions.|Contract configurator|
|[Microsoft Word add-in for ServiceNow Contracts](cncore-expl-snc-addin.md)|Use Microsoft Word documents to add content controls that act as placeholders for the content. Word templates are easier to review, mark up, and modify.|Contract configurator|
|[Contract and amendment requests](cncore-expl-ss-nss-contracts.md)|Initiate self-served or non-self-served contract requests.|Contract user|
|[Contract amendments](../task/cmpro-amend-landing.md)|Initiate and manage amendment requests.|Contract user, Contract fulfiller|
|[Obligation Management](cncore-obligation-management.md)|Track and manage contract obligations to help ensure compliance and minimize risks.|Obligation fulfiller or Obligation user|
|[Configuring external applications for Contract Management Pro](cncore-set-ext-app-config.md)|Integration with external storage and electronic signature providers.|Contract configurator|
|[Contracts Dashboard](../../../use/dashboards/application-content-packs/cncore-contracts-dashboard.md)|Get an insight on the volume of contract requests that are handled by your team.|Contract fulfiller|
|[Contract Workspace](cncore-contract-workspace.md)|Work with actionable widgets to categorize, prioritize, and efficiently work on contract requests.|Contract user or Contract fulfiller|
|[Now Assist in Contract Management](cncore-now-assit-landing.md)|Use Now Assist in Contract Management to analyze contracts for non-standard and missing clauses, and to extract information from signed contracts to add in the contract repository.|Now Assist contract fulfiller|

## What to explore next

To learn more about configuring and using Contract Management Pro, see:

-   [Configuring Contract Management Pro](cncore-config-cmpro.md)
-   [Using Contract Management Pro](cncore-use-cmpro.md)
-   [Now Assist in Contract Management](cncore-now-assit-landing.md)
-   [Managing Contract Management Pro](cncore-manage-cmpro.md)
-   [Contract Management Pro reference](cncore-ref.md)


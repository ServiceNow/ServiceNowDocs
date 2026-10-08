---
title: Exploring Contract Management Pro
description: Learn more about the Contract Management Pro application through a sample workflow and review the benefits that it can provide.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-expl-cmpro.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [Contract Template, Agreement Template, Contract Draft Template, Predefined Contract, Standard Contract Format, Legal Contract Template, Reusable Contract Template, Master Contract Template, Document templates, word content controls, ms word document templates, clause management, Word document templates, contract metadata extraction]
breadcrumb: [Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Exploring Contract Management Pro

Learn more about the Contract Management Pro application through a sample workflow and review the benefits that it can provide.

## Contract Management Pro overview

The ServiceNow® Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract, amendment and renewal requests. Contract requests can be submitted in two ways: linked to a business unit entity such as a purchase requisition or sourcing event, or as standalone requests without a parent record.

## Submitting contract requests

Contract requests can be submitted in two ways:

-   **Standalone requests**

    Contract requests initiated directly without a parent record using a record producer form. Entry points include Employee Center, contract request listing pages, and business unit workspaces.

-   **Parent-linked requests**

    Contract requests tied to a business unit entity using the Initiate Plug and Play modal. Entry points include purchase requisitions and sourcing events.


You can submit a own paper or third-party based contract requests. Regardless of the entry point, contract requests follow the same own paper or third-party paper workflows described in the following sections.

## Contract Management Pro users

<table id="table_rtl_l3k_pfc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contracts Core administrator

</td><td>

Manages contract records, user roles, and system configurations.

</td></tr><tr><td>

Contracts Core configurator

</td><td>

Manages the configurations related to Contract Management Pro. They configure contract templates, external systems, and configuration rules.

</td></tr><tr><td>

Contracts Core fulfiller

</td><td>

-   Initiates actions while fulfilling an assigned contract execution. This includes tasks such as creating revisions, adding signers, and canceling signer assignments.
-   Initiates contract requests.

</td></tr><tr><td>

Contracts Core user

</td><td>

Initiates and tracks contract, amendment and renewal requests.

</td></tr><tr><td>

Contract reviewer

</td><td>

Reviews contract documents, track review tasks, and use clause library to add appropriate clauses.

</td></tr><tr><td>

Contract report viewer

</td><td>

Views contract reports, analyse contract trends, and support data-driven decision making.

</td></tr><tr><td>

Contract report publisher

</td><td>

Publishes reports on Contracts Dashboard.

</td></tr><tr><td>

AI administrator

</td><td>

Installs ServiceNow Otto for Contract Management Pro and activates skills.

</td></tr><tr><td>

AI configurator

</td><td>

Configures the use case mappings for theServiceNow Otto for Contract Management Pro application.

</td></tr><tr><td>

AI contract fulfiller

</td><td>

Uses ServiceNow Otto for Contract Management Pro to analyze contract documents for deviations, extract metadata and obligation from signed contracts, and perform conversational search to query the contract repository and signed contract documents.

</td></tr><tr><td>

Obligation user

</td><td>

Submits obligation request.

</td></tr><tr><td>

Obligation fulfiller

</td><td>

Initiates actions while fulfilling an obligation. This includes tasks like create obligations, approve, reject, or cancel obligation tasks.

</td></tr><tr><td>

Obligation administrator

</td><td>

Provides administrative access to Obligation management and underlying data.

</td></tr></tbody>
</table>## Own paper contract request workflow

Own paper contracts are company-generated contracts that use predefined templates. The following image provides an overview of the own paper contract request workflow.

\[Omitted image "mmasset0021155-ss-cmpro-horizontal.png"\] Alt text: A flowchart illustrating an own paper contract request workflow in Contract Management Pro.

1.  The contract requester initiates a contract request.
2.  A contract document is generated from a contract template and the metadata, clauses, signatories, and tables are added dynamically according to predefined conditions.
3.  The requester or fulfiller can preview the contract document and make edits if needed. Edits create a new revision with updated metadata, clauses, and signatories.
4.  The contract fulfiller or requester does one of the following actions:
    1.  If no changes are required, gets approval from stakeholders and sends the contract document for signature.
    2.  If any changes are required, uploads a new revision of the document and gets approval from stakeholders before sending it for signature.
5.  If any signatory declines the document, it is sent back to the requester to be reworked and the revision is sent for signature.
6.  After all signatories have approved the document. The signed contract is attached to the contract request record.
7.  The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The requester and department members can access the signed contract document from the Contracts repository.

## Third-party paper contract request workflow

Third-party paper contracts are external contracts uploaded for review and signature. The following image provides an overview of the third-party paper contract request workflow.

\[Omitted image "mmasset0021156-nss-cmpro-horizontal.png"\] Alt text: A flowchart illustrating a third-party paper contract request workflow in Contract Management Pro.

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
|[Word Document Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-expl-wdt.md)|Configure word document templates for contract to streamline and reduce the need for rework and maintain uniformity across generated contract documents. Set up dynamic content generation through mappings and conditions for clauses and tables.|Contract configurator|
|[Clause Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-expl-clause-mgmt.md)|Effectively manage a library of clause variations. Use clause variations to dynamically place content in a contract depending on the specified conditions.|Contract configurator|
|[Microsoft Word add-in for ServiceNow Contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-expl-snc-addin.md)|Use Microsoft Word documents to add content controls that act as placeholders for the content. Word templates are easier to review, mark up, and modify.|Contract configurator|
|[Contract, amendment and renewal requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-expl-ss-nss-contracts.md)|Initiate own paper or third-party paper contract requests.|Contract user|
|Standalone contract request submission|Submit contract requests directly without requiring a parent record such as a purchase requisition or sourcing event.|Contract user, Contract fulfiller|
|[Contract amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cmpro-amend-landing.md)|Initiate and manage amendment requests.|Contract user, Contract fulfiller|
|[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cmpro-renewal-landing.md)|Initiate and manage renewal requests.|Contract user, Contract fulfiller|
|[Obligation Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-obligation-management.md)|Track and manage contract obligations to help ensure compliance and minimize risks.|Obligation fulfiller or Obligation user|
|[Configuring external applications for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-set-ext-app-config.md)|Integration with external storage and electronic signature providers.|Contract configurator|
|[Contracts Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-contracts-dashboard.md)|Get an insight on the volume of contract requests that are handled by your team.|Contract fulfiller|
|[Contract Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-contract-workspace.md)|Work with actionable widgets to categorize, prioritize, and efficiently work on contract requests.|Contract user or Contract fulfiller|
|[AI capabilities in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md)|Use ServiceNow Otto for Contract Management Pro to analyze contracts for non-standard and missing clauses, and to extract information from signed contracts to add in the contract repository.|AI contract fulfiller|

## What to explore next

To learn more about configuring and using Contract Management Pro, see:

-   [Configuring Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-config-cmpro.md)
-   [Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-use-cmpro.md)
-   [AI capabilities in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md)
-   [Managing Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-manage-cmpro.md)
-   [Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-ref.md)


---
title: Contract Management Pro release notes
description: The ServiceNow Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendment requests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Contract Management Pro release notes

The ServiceNow® Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendmentrequests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Australia release.

## Contract Management Pro highlights for the Australia release

-   Contract requests now support offline signatures, enabling users to manage contracts signed outside the system.
-   Send contracts for signature using Adobe Sign without having to sign in to the electronic signature portal.
-   Track undelivered electronic signature requests for a contract.
-   Compare two revisions of a contract document that are stored in external storage.
-   Support for processing Microsoft Word documents larger than 10 MB in Contract Management Pro.

See [Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cmpro-landing-page.md) for more information.

**Important:** Contract Management Pro is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Support for offline signatures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-signature-workflow.md#section_offline_workflow)**

    Record contracts that are signed outside Contract Management Pro, without sending signature request emails to the signatories.

    Contract fulfillers and contract users can select **Offline signature** as the signature type on a contract request. The **Initiate offline signature** action moves the contract request to the Awaiting signature state without triggering any signature request notifications. After the signatories sign the contract outside the system, upload the signed document to complete the workflow and create the contract repository record.

-   **[Add signatory initials placeholders to contract templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-addin-add-signatory.md)**

    Add initials placeholders to a contract template to mark the locations where signatories provide their initials. In the Microsoft Word add-in, select the **Signatory initials** tag while configuring participants or signature blocks. The initials tag is supported for Adobe Sign and Docusign.


-   **[Better visibility of undelivered signature requests for a contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cr-state-status.md)**

    When an electronic signature request is not delivered, the contract state is updated to Signature delivery failed and the signatory status to Delivery failed, clearly indicating the state of signature request. Contract fulfillers are also notified through in‑product and email alerts. This capability is supported for both Docusign and Adobe Sign.


## Changed in this release

-   **[Send contracts for signature using Adobe Sign without signing in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-nss-review-request.md)**

    Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract revisions in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-compare-docs.md)**

    Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-addin-add-clauses.md)**

    See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-set-ext-app-config.md)**

    Contract Management Pro now supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.


## Activation information

Install Contract Management Pro by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cmpro-landing-page.md)**

    Use the ServiceNow®Contract Management Pro application to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.

-   **[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-now-assit-landing.md)**

    Use the ServiceNow® Now Assist application in the Contract Management application to analyze a contract for missing and non-standard clauses. It also enables you to review and add the information to the mapped fields in the contract repository, eliminating the need to manually update the contract repository.


-   **[Now Assist in Contract Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/cmpro-na-rn.md)**  
The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Australia release.

**Parent Topic:**[Employee Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/employee-service-management-rn-landing.md)


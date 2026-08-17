---
title: Contract Management Pro release notes
description: The ServiceNow Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendment requests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-06-26"
reading_time_minutes: 5
keywords: [contract management, supporting documents, multi-file upload, document management, signatory roles, electronic signature roles]
---

# Contract Management Pro release notes

The ServiceNow® Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendmentrequests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Australia release.

## Contract Management Pro highlights for the Australia release

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Contract Management Pro. Check your entitlements to determine your access to specific features.
-   View the complete contract family hierarchy — including parent, sibling, and child contract requests — from the Related contract requests tab of the contract request.
-   Upload multiple supporting documents in a single action from your computer, activity stream, or external storage.
-   Assign roles to signatories to define their level of participation in the Docusign e-signature process.
-   Manage contracts signed outside the system using offline signature support for contract requests.
-   Send contracts for signature using Adobe Sign without signing in to the electronic signature portal.
-   Track undelivered electronic signature requests for a contract.

**Note:** Contract Management Pro is available in the ServiceNow store. For details, see the "Activation information" section of these release notes.

## Upgrade information

No upgrade actions are required for this release.

## New in the Australia release

-   **[Signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-signatory-roles.md)**

    Assign a role to each signatory in a contract request to define how each participant interacts with a contract document during the signature workflow. The available roles are Signer, Viewer, Receiver, and Approver. These roles apply to Docusign electronic signature process only. For wet or offline signature types, the **Signatory Role** field is inactive and all signatories are set to the Signer role.

    You can also configure the signatory roles in internal signatory rules to apply them automatically when a contract is generated.

    To enable this feature, set the `sn_cm_core.enable_docusign_signature_roles` system property to `true` and upgrade Docusign to version 4.4.3.

-   **[Support for offline signatures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-signature-workflow.md#section_offline_workflow)**

    Record contracts that are signed outside Contract Management Pro, without sending signature request emails to the signatories.

    Contract fulfillers and contract users can select **Offline signature** as the signature type on a contract request. The **Initiate offline signature** action moves the contract request to the Awaiting signature state without triggering any signature request notifications. After the signatories sign the contract outside the system, upload the signed document to complete the workflow and create the contract repository record.

-   **[Add signatory initials placeholders to contract templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-addin-add-signatory.md)**

    Add initials placeholders to a contract template to mark the locations where signatories provide their initials. In the Microsoft Word add-in, select the **Signatory initials** tag while configuring participants or signature blocks. The initials tag is supported for Adobe Sign and Docusign.

-   **[Better visibility of undelivered signature requests for a contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cr-state-status.md)**

    When an electronic signature request is not delivered, the contract state is updated to Signature delivery failed and the signatory status to Delivery failed, clearly indicating the state of signature request. Contract fulfillers are also notified through in‑product and email alerts. This capability is supported for both Docusign and Adobe Sign.


## UI changes

-   **[Related contract requests tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-linking-parent-child.md)**

    The Related contract requests tab includes a visual indicator that highlights the currently open contract request within the parent, sibling, and child contract requests hierarchy.

-   **[Supporting Documents tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-ss-add-suprt-doc.md)**

    The Supporting Documents tab now supports multiple file selections in a single action from your computer, external storage, and the activity stream.


## Changed in this release

-   **[Contract family hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-linking-parent-child.md)**

    The Related contract requests tab displays the complete contract family hierarchy for the open contract request, including parent, sibling, and child records at all levels. A visual indicator highlights the contract request that is currently open within the hierarchy. Previously, only the immediate parent and direct children were displayed.

-   **[Supporting document upload in additional contract request states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-ss-add-suprt-doc.md)**

    Upload multiple supporting documents in a single action from your computer, activity stream, or external storage from the Supporting Documents tab. You can attach supporting documents in the Awaiting Approval, Awaiting Signature, and Contract Signed states, along with the previously supported Draft, Work in Progress, and Awaiting Review states.

-   **[Signatory status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-signatory-roles.md)**

    The signatory statuses in a contract request have been updated. Pending Signature is now Pending, Signed is now Completed, and Signature Declined is now Declined. The Not started status is unchanged.

-   **[Send contracts for signature using Adobe Sign without signing in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-nss-review-request.md)**

    Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract revisions in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-compare-docs.md)**

    Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-addin-add-clauses.md)**

    See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-set-ext-app-config.md)**

    Contract Management Pro supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.


## Activation information

Contract Management Pro is available in the ServiceNow store. Check your entitlements to determine whether you have access to this application.

## Related ServiceNow applications and features

-   **[Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cmpro-landing-page.md)**

    Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendmentrequests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems.

-   **[ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-now-assit-landing.md)**

    Use the ServiceNow Otto for Contract Management Pro application to analyze a contract for missing and non-standard clauses. It also enables you to review and add the information to the mapped fields in the contract repository, eliminating manual updates to the contract repository.


-   **[ServiceNow Otto for Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/cmpro-na-rn.md)**  
The ServiceNow Otto for Contract Management Pro uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. ServiceNow Otto for Contract Management Pro was enhanced and updated in the Australia release.

**Parent Topic:**[Employee Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/employee-service-management-rn-landing.md)


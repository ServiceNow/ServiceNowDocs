---
title: Contract Management Pro release notes
description: The ServiceNow Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendment requests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 10
---

# Contract Management Pro release notes

The ServiceNow® Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendmentrequests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Zurich release.

## Contract Management Pro highlights for the Zurich release

-   View the complete contract family hierarchy — including parent, sibling, and child contract requests — from the Related contract requests tab of the contract request.
-   Upload multiple supporting documents in a single action from your computer, activity stream, or external storage.
-   Assign roles to signatories to define their level of participation in the Docusign e-signature process.
-   Contract requests now support offline signatures, enabling users to manage contracts signed outside the system.
-   Send contracts for signature using Adobe Sign without having to sign in to the electronic signature portal.
-   Compare two revisions of the contract document and view the redlined compared document.
-   Initiate and manage amendment requests for existing contracts.
-   Generate summaries, FAQs, or retrieve specific information from contract documents, supporting documents, and signed contracts.
-   Link parent contracts during drafting and negotiation phases to inherit parent contract terms.
-   Pause and resume an in-progress signature process when updates to the signatory list are required.

See [Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-cmpro-landing-page.md) for more information.

**Important:** Contract Management Pro is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-signatory-roles.md)**

    Assign a role to each signatory in a contract request to define how each participant interacts with a contract document during the signature workflow. The available roles are Signer, Viewer, Receiver, and Approver. These roles apply to Docusign electronic signature process only. For wet or offline signature types, the **Signatory Role** field is inactive and all signatories are set to the Signer role.

    You can also configure the signatory roles in internal signatory rules to apply them automatically when a contract is generated.

    To enable this feature, set the `sn_cm_core.enable_docusign_signature_roles` system property to `true` and upgrade Docusign to version 4.4.3.

-   **[Support for offline signatures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-signature-workflow.md#section_offline_workflow)**

    Record contracts that are signed outside Contract Management Pro, without sending signature request emails to the signatories.

    Contract fulfillers and contract users can select **Offline signature** as the signature type on a contract request. The **Initiate offline signature** action moves the contract request to the Awaiting signature state without triggering any signature request notifications. After the signatories sign the contract outside the system, upload the signed document to complete the workflow and create the contract repository record.

-   **[Add signatory initials placeholders to contract templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-addin-add-signatory.md)**

    Add initials placeholders to a contract template to mark the locations where signatories provide their initials. In the Microsoft Word add-in, select the **Signatory initials** tag while configuring participants or signature blocks. The initials tag is supported for Adobe Sign and Docusign.


-   **[Better visibility of undelivered signature requests for a contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-cr-state-status.md)**

    When an electronic signature request is not delivered, the contract state is updated to Signature delivery failed and the signatory status to Delivery failed, clearly indicating the state of signature request. Contract fulfillers are also notified through in‑product and email alerts. This capability is supported for both Docusign and Adobe Sign.


-   **[Contract amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-amend-landing.md)**

    Formally change, add, or remove terms in an existing contract through contract amendments without having to replace the entire agreement. The Amendment feature enables you to initiate, track, and finalize amendments to existing contracts and provides an audit trail. The signed contract and its amendment documents are stored in a centralized repository under the parent contract, which enables you to manage all related documents from a single location.

    -   Use the **Request type** field to distinguish between contract and amendment requests.

    -   View the amendment history directly from the contract request.

    -   View amendment details within the contract repository record through related lists:

        -   Contract Requests: View all contract and amendment requests associated with the contract.
        -   Amendment Field Changes: Track modifications over time by accessing a detailed log of all field changes made through amendments.
        -   Contract Documents: Access all documents related to the contract, including those generated or updated as part of amendment processes.

-   **[Compare contract revisions in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-compare-docs.md)**

    Compare a contract document in .docx format with its revised version from your workspace by using the **Compare documents** option.

    Document comparison is not supported for contract documents stored in external storage.

-   **[Contract summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-summarize-contract-cmr.md)**

    Generate a summary of contract documents, supporting documents, and signed contracts in Contract Management Pro. You can also generate FAQs from the document or ask questions in the Now Assist panel to retrieve specific information from the document.


-   **[Link parent contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-link-parent-cmr.md)**

    Establish a hierarchical relationship between the parent and child contract requests during the drafting and negotiation phases. You can choose to have the child contract request automatically inherit the configured fields from the parent request. The contract repository records associated with the parent and child contract requests are automatically linked after the contracts are signed.

-   **[Perpetual contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-work-ss-cntr-request-fulfiller.md)**

    Classify a contract with no end date as a perpetual contract by using the **Perpetual** option.

    Perpetual contracts must be initiated from Sales Customer Relationship Management and Source-to-Pay Operations.

-   **[Help Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/help-center.md)**

    Access help information directly from your workspace through a help icon \[Omitted image "Banner\_HelpIcon.png"\] Alt text: that accesses the Help Center for the landing and list pages of Contract Workspace.​


## UI changes

-   **[Related contract requests tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-linking-parent-child.md)**

    The Related contract requests tab includes a visual indicator that highlights the currently open contract request within the parent, sibling, and child contract requests hierarchy.

-   **[Supporting Documents tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-ss-add-suprt-doc.md)**

    The Supporting Documents tab now supports multiple file selections in a single action from your computer, external storage, and the activity stream.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Contract family hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-linking-parent-child.md)**

    The Related contract requests tab displays the complete contract family hierarchy for the open contract request, including parent, sibling, and child records at all levels. A visual indicator highlights the contract request that is currently open within the hierarchy. Previously, only the immediate parent and direct children were displayed.

-   **[Supporting document upload in additional contract request states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-ss-add-suprt-doc.md)**

    Upload multiple supporting documents in a single action from your computer, activity stream, or external storage from the Supporting Documents tab. You can attach supporting documents in the Awaiting Approval, Awaiting Signature, and Contract Signed states, along with the previously supported Draft, Work in Progress, and Awaiting Review states.

-   **[Signatory status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-signatory-roles.md)**

    The signatory statuses in a contract request have been updated. Pending Signature is now Pending, Signed is now Completed, and Signature Declined is now Declined. The Not started status is unchanged.

-   **[Send contracts for signature using Adobe Sign without signing in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-nss-review-request.md)**

    Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract revisions in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-compare-docs.md)**

    Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-addin-add-clauses.md)**

    See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-set-ext-app-config.md)**

    Contract Management Pro now supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.

-   **[Select contract type while initiating a third-party contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-initiate-non-ss-cnt.md)**

    Specify whether a contract request is for a single contract or multiple contracts. For single contracts, you can select the type of contract document.

-   **[Classify contract requests as a single or multiple contracts type based on selected documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/snlc-submit-request-tpc.md)**

    Automatically classify a contract request as single contract type or multiple contracts type based on single or multiple contracts when creating a third-party contract review request from Employee Portal. The **Type** field in the contract request reflects this selection by displaying either **Single contract** or **Multiple contracts**.

-   **[Use scripts to define additional conditions for a clause variation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-add-clauses-doc-tmplt.md)**

    Define clause conditions on fields and variables of a table that isn't directly linked to the contract template table. The condition determines when the clause variation is used in a contract.

-   **[Configure tables in a contract template to append or add fields from related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-append-data-table.md)**

    Insert additional data from the related table fields into the dynamic tables of a contract using scripts. Display additional data from related table fields by appending it to existing columns or adding it as new columns.

-   **[Contract Management Pro configurations are available on the Contract Request table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-create-ct-word-addin.md)**

    You can now set up the following Contract Management Pro configurations directly on the Contract Request \[sn\_cm\_core\_contract\_request\] table to centralize the configuration on a single table and improve consistency and reusability across business units:

    -   Contract templates
    -   Template rules
    -   Internal signatory rules
    -   Clause and clause variation setup
    -   Contract configuration
    -   External storage and e-signature integrations
    -   Mappings for Now Assist contract metadata extraction and Now Assist contract analysis
    The Contract Request table is automatically selected for a new configuration. You can manually select a different table, if necessary.

-   **[Configure dynamic tables for contract template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-addin-table.md)**

    Set up contract templates on the Contract Request \[sn\_cm\_core\_contract\_request\] table to reuse the template across business units. When you select the Contract Request table, the **Table** tab in the Microsoft Word add-in displays an additional field, called the **Parent request table** field, that you can use to select the source parent request table.

    Additionally, the **Table** field has been renamed **Lookup table**. You can select the table from the data that is populated into the contract document.

    If the template isn't based on the Contract Request table, only the **Lookup table** field is shown.

-   **[Copy fields from parent request to contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-copy-fld-frm-parent.md)**

    Automatically copy the required fields from the originating business unit record to the contract request when it's initiated.

-   **[Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-signature-workflow.md)**

    Wet signature requests are sent one signatory at a time, starting with the first signatory in order, rather than to all signatories at the same time. Signatories can be changed even after the signing process has been initiated. When a signatory signs and returns the document, the fulfiller manages the remaining signatures.

-   **[Modify signatories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-pause-signature.md)**

    Enable contract fulfillers to pause an ongoing signature process, make necessary changes to the list or order of signatories, and then resume the process without restarting the entire workflow by using the **Modify Signatories** and **Resume signature** options. This feature is supported only for the Docusign electronic signature provider.

-   **[Resend signature request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-resend-sign-req.md)**

    Enable contract fulfillers to manually trigger a signature request when needed instead of relying on automated reminders by using the **Resend signature request** option.

-   **[Configuring signatories in Contract template using Microsoft Word add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-config-sign-addin.md)**

    Signature placeholders in contract templates are now mapped to the e-signature tool tags \(such as Docusign\) instead of signer fields to help accommodate changes in the signatories. The values in the signature blocks are filled in by the signatories during the signing process.


## Activation information

Install Contract Management Pro by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-cmpro-landing-page.md)**

    Use the ServiceNow®Contract Management Pro application to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.

-   **[Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-now-assit-landing.md)**

    Use the ServiceNow® Now Assist application in the Contract Management application to analyze a contract for missing and non-standard clauses. It also enables you to review and add the information to the mapped fields in the contract repository, eliminating the need to manually update the contract repository.


-   **[Now Assist in Contract Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/cmpro-na-rn.md)**  
The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Zurich release.

**Parent Topic:**[Employee Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/employee-service-management-rn-landing.md)


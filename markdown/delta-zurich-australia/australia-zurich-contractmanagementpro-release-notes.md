---
title: Combined Contract Management Pro release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Contract Management Pro from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-contractmanagementpro-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined Contract Management Pro release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Contract Management Pro from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Contract Management Pro release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Contract Management Pro to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Contract Management Pro.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Support for offline signatures](https://www.servicenow.com/docs/access?context=cncore-signature-workflow&family=zurich&ft:locale=en-US)**

Record contracts that are signed outside Contract Management Pro, without sending signature request emails to the signatories.

Contract fulfillers and contract users can select **Offline signature** as the signature type on a contract request. The **Initiate offline signature** action moves the contract request to the Awaiting signature state without triggering any signature request notifications. After the signatories sign the contract outside the system, upload the signed document to complete the workflow and create the contract repository record.

-   **[Add signatory initials placeholders to contract templates](https://www.servicenow.com/docs/access?context=cncore-addin-add-signatory&family=zurich&ft:locale=en-US)**

Add initials placeholders to a contract template to mark the locations where signatories provide their initials. In the Microsoft Word add-in, select the **Signatory initials** tag while configuring participants or signature blocks. The initials tag is supported for Adobe Sign and Docusign.


-   **[Better visibility of undelivered signature requests for a contract](https://www.servicenow.com/docs/access?context=cncore-cr-state-status&family=zurich&ft:locale=en-US)**

When an electronic signature request is not delivered, the contract state is updated to Signature delivery failed and the signatory status to Delivery failed, clearly indicating the state of signature request. Contract fulfillers are also notified through in‑product and email alerts. This capability is supported for both Docusign and Adobe Sign.


-   **[Contract amendments](https://www.servicenow.com/docs/access?context=cmpro-amend-landing&family=zurich&ft:locale=en-US)**

Formally change, add, or remove terms in an existing contract through contract amendments without having to replace the entire agreement. The Amendment feature enables you to initiate, track, and finalize amendments to existing contracts and provides an audit trail. The signed contract and its amendment documents are stored in a centralized repository under the parent contract, which enables you to manage all related documents from a single location.

    -   Use the **Request type** field to distinguish between contract and amendment requests.

    -   View the amendment history directly from the contract request.

    -   View amendment details within the contract repository record through related lists:

        -   Contract Requests: View all contract and amendment requests associated with the contract.
        -   Amendment Field Changes: Track modifications over time by accessing a detailed log of all field changes made through amendments.
        -   Contract Documents: Access all documents related to the contract, including those generated or updated as part of amendment processes.

-   **[Compare contract documents](https://www.servicenow.com/docs/access?context=cmpro-compare-docs&family=zurich&ft:locale=en-US)**

Compare a contract document in .docx format with its revised version from your workspace by using the **Compare documents** option.

Document comparison is not supported for contract documents stored in external storage.

-   **[Contract summarization](https://www.servicenow.com/docs/access?context=cmpro-summarize-contract-cmr&family=zurich&ft:locale=en-US)**

Generate a summary of contract documents, supporting documents, and signed contracts in Contract Management Pro. You can also generate FAQs from the document or ask questions in the Now Assist panel to retrieve specific information from the document.


-   **[Link parent contract requests](https://www.servicenow.com/docs/access?context=cmpro-link-parent-cmr&family=zurich&ft:locale=en-US)**

Establish a hierarchical relationship between the parent and child contract requests during the drafting and negotiation phases. You can choose to have the child contract request automatically inherit the configured fields from the parent request. The contract repository records associated with the parent and child contract requests are automatically linked after the contracts are signed.

-   **[Perpetual contracts](https://www.servicenow.com/docs/access?context=cncore-work-ss-cntr-request-fulfiller&family=zurich&ft:locale=en-US)**

Classify a contract with no end date as a perpetual contract by using the **Perpetual** option.

Perpetual contracts must be initiated from Sales Customer Relationship Management and Source-to-Pay Operations.

-   **[Help Center](https://www.servicenow.com/docs/access?context=help-center&family=zurich&ft:locale=en-US)**

Access help information directly from your workspace through a help icon \[Omitted image "Banner\_HelpIcon.png"\] Alt text: that accesses the Help Center for the landing and list pages of Contract Workspace.​


</td></tr><tr><td>

Australia

</td><td>

-   **[Support for offline signatures](https://www.servicenow.com/docs/access?context=cncore-signature-workflow&family=australia&ft:locale=en-US)**

Record contracts that are signed outside Contract Management Pro, without sending signature request emails to the signatories.

Contract fulfillers and contract users can select **Offline signature** as the signature type on a contract request. The **Initiate offline signature** action moves the contract request to the Awaiting signature state without triggering any signature request notifications. After the signatories sign the contract outside the system, upload the signed document to complete the workflow and create the contract repository record.

-   **[Add signatory initials placeholders to contract templates](https://www.servicenow.com/docs/access?context=cncore-addin-add-signatory&family=australia&ft:locale=en-US)**

Add initials placeholders to a contract template to mark the locations where signatories provide their initials. In the Microsoft Word add-in, select the **Signatory initials** tag while configuring participants or signature blocks. The initials tag is supported for Adobe Sign and Docusign.


-   **[Better visibility of undelivered signature requests for a contract](https://www.servicenow.com/docs/access?context=cncore-cr-state-status&family=australia&ft:locale=en-US)**

When an electronic signature request is not delivered, the contract state is updated to Signature delivery failed and the signatory status to Delivery failed, clearly indicating the state of signature request. Contract fulfillers are also notified through in‑product and email alerts. This capability is supported for both Docusign and Adobe Sign.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Contract Management Pro features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Send contracts for signature using Adobe Sign without signing in](https://www.servicenow.com/docs/access?context=cncore-nss-review-request&family=zurich&ft:locale=en-US)**

Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract documents](https://www.servicenow.com/docs/access?context=cmpro-compare-docs&family=zurich&ft:locale=en-US)**

Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://www.servicenow.com/docs/access?context=cncore-addin-add-clauses&family=zurich&ft:locale=en-US)**

See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://www.servicenow.com/docs/access?context=cncore-set-ext-app-config&family=zurich&ft:locale=en-US)**

Contract Management Pro now supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.

-   **[Select contract type while initiating a third-party contract](https://www.servicenow.com/docs/access?context=cncore-initiate-non-ss-cnt&family=zurich&ft:locale=en-US)**

Specify whether a contract request is for a single contract or multiple contracts. For single contracts, you can select the type of contract document.

-   **[Classify contract requests as a single or multiple contracts type based on selected documents](https://www.servicenow.com/docs/access?context=snlc-submit-request-tpc&family=zurich&ft:locale=en-US)**

Automatically classify a contract request as single contract type or multiple contracts type based on single or multiple contracts when creating a third-party contract review request from Employee Portal. The **Type** field in the contract request reflects this selection by displaying either **Single contract** or **Multiple contracts**.

-   **[Use scripts to define additional conditions for a clause variation](https://www.servicenow.com/docs/access?context=cncore-add-clauses-doc-tmplt&family=zurich&ft:locale=en-US)**

Define clause conditions on fields and variables of a table that isn't directly linked to the contract template table. The condition determines when the clause variation is used in a contract.

-   **[Configure tables in a contract template to append or add fields from related tables](https://www.servicenow.com/docs/access?context=cncore-append-data-table&family=zurich&ft:locale=en-US)**

Insert additional data from the related table fields into the dynamic tables of a contract using scripts. Display additional data from related table fields by appending it to existing columns or adding it as new columns.

-   **[Contract Management Pro configurations are available on the Contract Request table](https://www.servicenow.com/docs/access?context=cncore-create-ct-word-addin&family=zurich&ft:locale=en-US)**

You can now set up the following Contract Management Pro configurations directly on the Contract Request \[sn\_cm\_core\_contract\_request\] table to centralize the configuration on a single table and improve consistency and reusability across business units:

    -   Contract templates
    -   Template rules
    -   Internal signatory rules
    -   Clause and clause variation setup
    -   Contract configuration
    -   External storage and e-signature integrations
    -   Mappings for Now Assist contract metadata extraction and Now Assist contract analysis
The Contract Request table is automatically selected for a new configuration. You can manually select a different table, if necessary.

-   **[Configure dynamic tables for contract template](https://www.servicenow.com/docs/access?context=cncore-addin-table&family=zurich&ft:locale=en-US)**

Set up contract templates on the Contract Request \[sn\_cm\_core\_contract\_request\] table to reuse the template across business units. When you select the Contract Request table, the **Table** tab in the Microsoft Word add-in displays an additional field, called the **Parent request table** field, that you can use to select the source parent request table.

Additionally, the **Table** field has been renamed **Lookup table**. You can select the table from the data that is populated into the contract document.

If the template isn't based on the Contract Request table, only the **Lookup table** field is shown.

-   **[Copy fields from parent request to contract request](https://www.servicenow.com/docs/access?context=cncore-copy-fld-frm-parent&family=zurich&ft:locale=en-US)**

Automatically copy the required fields from the originating business unit record to the contract request when it's initiated.

-   **[Signature workflow for a contract request](https://www.servicenow.com/docs/access?context=cncore-signature-workflow&family=zurich&ft:locale=en-US)**

Wet signature requests are sent one signatory at a time, starting with the first signatory in order, rather than to all signatories at the same time. Signatories can be changed even after the signing process has been initiated. When a signatory signs and returns the document, the fulfiller manages the remaining signatures.

-   **[Modify signatories](https://www.servicenow.com/docs/access?context=cncore-pause-signature&family=zurich&ft:locale=en-US)**

Enable contract fulfillers to pause an ongoing signature process, make necessary changes to the list or order of signatories, and then resume the process without restarting the entire workflow by using the **Modify Signatories** and **Resume signature** options. This feature is supported only for the Docusign electronic signature provider.

-   **[Resend signature request](https://www.servicenow.com/docs/access?context=cncore-resend-sign-req&family=zurich&ft:locale=en-US)**

Enable contract fulfillers to manually trigger a signature request when needed instead of relying on automated reminders by using the **Resend signature request** option.

-   **[Configure signatories](https://www.servicenow.com/docs/access?context=cncore-config-sign-addin&family=zurich&ft:locale=en-US)**

Signature placeholders in contract templates are now mapped to the e-signature tool tags \(such as Docusign\) instead of signer fields to help accommodate changes in the signatories. The values in the signature blocks are filled in by the signatories during the signing process.


</td></tr><tr><td>

Australia

</td><td>

-   **[Send contracts for signature using Adobe Sign without signing in](https://www.servicenow.com/docs/access?context=cncore-nss-review-request&family=australia&ft:locale=en-US)**

Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract documents](https://www.servicenow.com/docs/access?context=cmpro-compare-docs&family=australia&ft:locale=en-US)**

Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://www.servicenow.com/docs/access?context=cncore-addin-add-clauses&family=australia&ft:locale=en-US)**

See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://www.servicenow.com/docs/access?context=cncore-set-ext-app-config&family=australia&ft:locale=en-US)**

Contract Management Pro now supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Contract Management Pro features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Contract Management Pro features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Contract Management Pro.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Contract Management Pro by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Contract Management Pro by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Contract Management Pro, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Contract requests now support offline signatures, enabling users to manage contracts signed outside the system.
-   Send contracts for signature using Adobe Sign without having to sign in to the electronic signature portal.
-   Compare two revisions of the contract document and view the redlined compared document.
-   Initiate and manage amendment requests for existing contracts.
-   Generate summaries, FAQs, or retrieve specific information from contract documents, supporting documents, and signed contracts.
-   Link parent contracts during drafting and negotiation phases to inherit parent contract terms.
-   Pause and resume an in-progress signature process when updates to the signatory list are required.

 See [Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Contract requests now support offline signatures, enabling users to manage contracts signed outside the system.
-   Send contracts for signature using Adobe Sign without having to sign in to the electronic signature portal.
-   Track undelivered electronic signature requests for a contract.
-   Compare two revisions of a contract document that are stored in external storage.
-   Support for processing Microsoft Word documents larger than 10 MB in Contract Management Pro.

 See [Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


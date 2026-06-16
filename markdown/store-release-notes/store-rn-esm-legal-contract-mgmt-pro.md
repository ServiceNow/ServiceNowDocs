---
title: Contract Management Pro release notes
description: Version history for the Legal Contract Management Pro application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-contract-mgmt-pro.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Contract Management Pro release notes

Version history for the Legal Contract Management Pro application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.6 - June 2026**
    -   New:
        -   Contract requests now support offline signatures, enabling users to manage contracts signed outside the system.
        -   Adobe Sign and DocuSign flows now support signature initials, enabling template-driven initial blocks alongside full signature blocks in contract documents.
    -   Fixed:
        -   Cancelling a contract immediately after sending for signature no longer incorrectly reverts the contract state to 'Awaiting Signature'.
        -   The Sync document warning no longer appears after a contract document has been successfully synchronised.
        -   The Sync document warning no longer appears repeatedly when the date format differs from the system default.
        -   The Sync document no longer fails when the contract document template is configured on the CMR table.
        -   The Sync document action no longer removes the signature placeholder from a contract document.
        -   Documents attached as contract revisions or supporting documents can now be renamed without error.
        -   The e-signature flow no longer triggers a restricted caller access privilege error.
        -   The contract workspace view now renders correctly following an application upgrade.
        -   The 'Prepare for Signature' action now correctly redirects to DocuSign even when the request's short description is more than 100 characters.
-   **Version 1.7.0 - March 2026**
    -   New:
        -   When an e-signature request fails to deliver, the contract state updates to Signature delivery failed, and the signatory status to Delivery failed. Contract fulfillers are notified via in-product and email alerts. Supported for DocuSign and Adobe Sign
        -   Users can now access the Adobe Sign console via the Prepare for signature button without signing in to Adobe Sign
        -   Contract document comparison now supports externally stored documents
    -   Changed: Support for Microsoft Word documents larger than 10 MB for document operations, including contract revision generation and document comparison etc.
    -   Fixed:
        -   Adding multiple signatories now generates the correct number of signature blocks for internal and external signatories, regardless of name, title, or email mappings
        -   Supporting documents can now be successfully uploaded when a contract request is in the 'Awaiting Review' state
        -   Clause variations are now correctly evaluated when generating template-based contract revisions, even when the Advanced Script option is not selected
        -   The ContractsUtility script include is no longer marked as read-only, allowing custom implementations to extend and override functions as intended
        -   The Uploaded by field on contract documents now correctly displays the uploading user instead of System for requests submitted via the employee portal
        -   The Approving field on contract approval requests now correctly displays the contract document revision name when accessed from the Employee portal
-   **Version 1.6.0 - December 2025**
    -   New:
        -   Initiate and manage amendment requests for existing contracts.
        -   Compare a contract document in .doc or .docx format with its revised version from your workspace by using the “Compare documents” option.
        -   Generate summaries, FAQs, or retrieve specific information from contract documents, supporting documents, and signed contracts.
    -   Changed: PDF documents sent for signature via DocuSign now support file sizes up to 36 MB. Word documents continue to support up to 10 MB.
    -   Fixed:
        -   Security fixes
        -   When a document in a contract template is replaced with a document that has no clauses, all the existing clause mappings are now cleared.
        -   Review task completion notes on activity stream of a contract request now indicate the attachment was uploaded by the reviewer and provide a direct link to access it.
        -   UI improvement: “Changes requested” secondary header is hidden in Contracts Workspace.
        -   Legal name encryption and visibility is corrected to respect role‑based access
        -   The Initiate Contract window now correctly handles user date format preference.
        -   The New button is no longer displayed in the Contract repository tab of a contract request for users without appropriate roles.
        -   Attachments stored in ServiceNow are deleted after successful upload to external storage \(Google Drive/OneDrive\).
        -   When executing contract via DocuSign, one signatory is no longer required to sign for both parties when both signatories share the same full name but different email address.
        -   When both DocuSign and Adobe Sign are installed, the signatory status updates correctly for pause or reorder operations in contract request.
        -   The contract flow no longer fails when signature is delegated by a signatory within DocuSign.
        -   In parent-child contract mapping, system fields can no longer be mapped for inheriting from a parent contract.
-   **Version 2.1.0 - September 2025**
    -   Changed: Legal Contract repository view on the Legal Counsel Center has been improved. The view has been updated to show the additional fields related to contracts, also additional related lists \(e.g. Obligations, Playbook, Executed contracts etc\) been added to show.
    -   Fixed: Sync document functionality was not working with demo data template.
-   **Version 1.5.1 - August 2025**
    -   New:
        -   Signature process:
            -   Added the ability to modify signatories in a contract request when it is in awaiting signature state.
            -   Added the ability to resend the signature request to the pending signer
        -   Backend improvements:
            -   Contract Management Pro configurations are available on the Contract Request table, allowing for centralized configuration on a single table.
            -   The Signature blocks are selected by default when creating a contract template.
            -   New fields like company, perpetual are added to contract request. If contract end date is blank, then contract is perpetual. If end date exists, then contract is not perpetual.
            -   When initiating a third-party contract within business unit workspace, you can specify whether the contract request is for a single contract or multiple contracts.
            -   Classify contract requests as single or multiple contracts when creating a third-party contract review request from Employee Portal based on the number of contract documents attached to the request.
            -   Configure the ContractManagementExt extension point to automatically copy required fields from the originating business unit record to the contract request.
        -   Parent-child contract linking for own paper and single contract third party paper:
            -   Support contract linking during drafting and negotiation phases to establish a hierarchical relationship between parent and child contracts.
            -   Support contract linking and inheritance during drafting and negotiation phases to establish a hierarchical relationship between parent and child contracts and automatically inherit configured fields from the parent contract.
            -   Parent-child hierarchy is visible. The contract repository records associated with the parent and child contract requests are automatically linked after the contracts are signed.
            -   Support the capability to unlink a parent contract request. Audit is managed for linking and unlinking.
    -   Changes:
        -   The Name, Title and Email e-signature tags in the contract template will be populated from the e-signature tool instead of the signer task fields
        -   Reorder of the signer tasks in the contract request can be done using the Reorder modal by drag drop capability instead of editing each signer task.
        -   In the wet signature flow the request for signature will be sent only to the first signer with instructions to the signer to return the signed contract to the fulfiller to coordinate the remaining signatures. Earlier the request for signature was sent to all the signers simultaneously.
    -   Fixed:
        -   In contract approvals record the approving field was populated with the contract request reference instead of the specific contract revision document due to business rules coming from another platform plugin.
        -   Files with the extension .PDF and with files with file names that had 2 periods \(eg: xx.xx.pdf\) were not getting sent for signature in the wet signature flow.
        -   Translations for few labels across the application
-   **Version 1.5.0 - May 2025**
    -   New:
        -   Enhanced electronic signature workflow to enable signatories to do a wet signature in the electronic signature workflow. This capability provides flexibility to complete the signature process when the signatories want to do a wet signature instead of a electronic signature.
        -   Added logout and scope change functionality for Microsoft Word add-in for ServiceNow Contract
    -   Changed: Upload the contract document directly from the Word Add-in instead of selecting it from your system.
    -   Fixed:
        -   Multiple nested folders are created on external storage when the contract type name contains '/'. The issue has been fixed by restricting the character '/' in the contract type name.
        -   In the wet signature process, some contract documents are not attached when sent for signature if the cumulative size of the attachments exceeds 18 MB. This issue has been resolved, and now, the contract documents are sent in multiple emails if the cumulative size of the documents exceeds 18 MB.
        -   Performance issues
        -   UI issues
-   **Version 1.4.1 - February 2025**
    -   New: The Legal request details section has been added to the Details tab of a contract request to display the legal fields of the parent legal request. This enables fulfillers to update legal fields directly from the contract request.
    -   Changed:
        -   In contract requests, the Send for signature process is now improved to display the contract document details before you send it to the signatories.
        -   DocuSign Integration: You need not log in to DocuSign when prepare for signature is initiated for a third-part contract review request.
        -   For self-served contract requests, the Create revision button is not available when the contract type is inactive.
        -   For non-self-served contract requests, the Contract type field displays only the active contract types in the Create revision pop-up window.
        -   While reclassifying a contract document or supporting document, only the active contract types are displayed in the 'Reclassify to' drop-down list.
        -   In the Create revision window, the &amp;lsquo;Inbound email' option in the Storage type field has been replaced by 'Activity stream'. The Activity stream now includes documents attached while requesting changes and received via inbound emails.
        -   In the Contract documents and Supporting documents tabs, the Contract type field in the Preview document window is auto-populated if the contract request has only one contract type.
        -   Legal fulfillers can now view the contract number and contract repository fields in the contract repository record.
        -   When you create a Contract template, only active contract types are displayed in the Contract type field. If a contract type is deactivated while the template is in draft or editing state, you cannot publish the template.
        -   The contract configurator \[sn\_cm\_core.contract\_config\] can now add or update an internal signatory rule.
        -   You can now attach a document while requesting changes to a contract document in a contract request. The attached document is added to the Activity stream of the contract request.
        -   The Activity stream of a contract request now displays the activities of the contract request and the parent legal request.
        -   You can now set conditions for Legal Contract Request fields in the Advanced View of the Legal Counsel Center to filter specific contract requests. Additionally, you can select which Legal Contract Request columns to display in the list view.
        -   Performance improvements.
        -   UI improvements
    -   Fixed:
        -   When Google drive is configured as the external storage, the URL field in the Details tab and the URL column in the Contract documents tab of a contract repository record do not display the link to access the document.
        -   The Ready column on the sn\_cm\_core\_document\_revision table does not filter the values correctly.
        -   There was a lack of consistency in the navigation order of the Lists. This issue has been fixed.
        -   The sync document message appeared even when there were no updates to the metadata. This issue has been fixed.
        -   In a third-party contract review request where wet signature is enabled and documents are stored in extrenal storage, the signed contract documents are not attached to the email sent to the signatories after the signed contract documents are uploaded to the contract request.
        -   The attached document on the createDocument revision was not cleared from the CMR record after the revision was created. This has been resolved.
        -   The "Use this clause" functionality did not work in external storage. This issue has been resolved.
        -   If you deactivate a Contract Configuration associated with an active contract request, an incorrect validation message appears and the contract configuration is saved as inactive.
-   **Version 1.3.1 - November 2024**

    New: The Obligation Management application will be automatically installed with Contract Management Pro. For more information, refer to Obligation Management.

-   **Version 1.2.1 - August 2024**
    -   New:
        -   Support for internal review of contract documents in a contract request.
        -   Support for Wet signatures in contract requests to enable signatories to sign the document using pen and paper.
        -   Map ServiceNow tables to a contract template to populate records dynamically when the contract document is generated.
        -   Support for additional signature blocks in the contract document based on the number of signatories in the contract request.
    -   Changed:
        -   The Signatories tab in the Word add-in has been updated to add and configure signature blocks for signatories.
        -   The Sync signatories button in the Signatories tab has been replaced by the Sync document button in the Contract documents tab.
-   **Version 1.1.1 - May 2024**
    -   New:
        -   Support for non-task tables while configuring contract templates.
        -   Request changes functionality for reviewing and finalizing the contract documents.
        -   Initiate contract request model supports customization of title, information message and setting of Start date as a required field.
    -   Fixed:
        -   Attachment icon is not visible on contextual side panel item in Contract Workspace
        -   Participant fields are disappearing from loading in contract templates
        -   Failure to transfer third-party contract request from.
        -   Draft contract requests are shown as Open requests in dashboard
        -   Users with sn\_cm\_core.contract\_config role are unable to view contract types
        -   Approval users is getting access to only Revision instead of Contract folder
-   **Version 1.0.11 - March 2024**

    New: Plug and play model for easy adoption.

-   **Version 1.0.0 - August 2023**
    -   ServiceNow Contract Management Pro removes the pain of manual processes and complex systems that slows down the business, with an intuitive self-service intake workflow coupled with an optimized workspace for legal staff to track, author, and manage contracts. Template-based contracts such as NDAs can be completely automated without requiring legal involvement. Authoring is made easy with common editing, storage and eSignature tools, ensuring rapid delivery.
    -   Contract Management Pro provides updated capabilities including a centralized and modern interface for easy cross-collaboration. All contract revisions can be viewed and made from one consolidated workspace, and additional parties can be added for review and approval. Higher stakeholder satisfaction is ensured as the system streamlines processes across the contract lifecycle to ensure prompt contract delivery.
    -   Utilize the power of Microsoft Word to efficiently generate new contracts and relevant legal documents. Conveniently store and author reusable contracts templates using Word to deliver prompt services. Ensure contract consistency and compliance by using pre-approved clauses from a library. Lastly, automated email reminders keep the business well-informed and ensures that no contract expiration goes unnoticed.

**Parent Topic:**[ServiceNow Store - Legal Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-esm-legal-service-delivery.md)


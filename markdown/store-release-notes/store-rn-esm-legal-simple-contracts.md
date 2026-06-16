---
title: Legal Simple Contracts release notes
description: Version history for the Legal Simple Contracts on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-simple-contracts.html
release: store
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Legal Simple Contracts release notes

Version history for the Legal Simple Contracts on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.8.0 - February 2025**
    -   Note: Legal Simple Contracts is being prepared for deprecation. It will be hidden and no longer available for activation for new customers but will continue to work and be supported for existing customers. For details, see the Deprecation Process \[KB0867184\] article in the Now Support knowledge base.
    -   Fixed: When a contract document is sent for signature, multiple emails were sent to the signatories. This has been fixed.
-   **Version 5.7.1 - November 2024**
    -   Fixed:
        -   The documents attached while creating a revision and stored in ServiceNow based storage are getting deleted by the Remove Orphaned Attachments' job if they are more than 5 days old. This has been fixed.
        -   The send for signature action ended in an error when you are using Adobe Sign and the Company Name field on the contract has special character. This is now fixed.
-   **Version 5.6.1 - May 2024**

    Fixed: The Deal closure date on Sales Contract Review allowed the date to be in the past.

-   **Version 5.4.2 - March 2024**
    -   New: Support for document templates of type Microsoft Word.
    -   Fixed: For Third-party contract review requests, signatory status is not updated to "Declined" when signature is declined when configured for DocuSign.EndFragment.
-   **Version 5.2.4 - November 2023**

    Fixed: Fixed the issue where the "Cancel Request" option is not displayed for Non-disclosure agreements and third-party contract review requests submitted by a legal user.

-   **Version 5.2.2 - August 2023**
    -   Changed: Added support for inserting signed date tag in HTML contract template
    -   Fixed: Minor issues across self service contracts like NDA, Third party contracts
-   **Version 5.1.2 - May 2023**
    -   New:
        -   Supporting wet signatures along with the already existing electronic signatures in the NDA workflow. This feature helps in effective collaboration between the signatories.
            -   On submitting the request, the contract is sent by email to the signatories
            -   The signatories sign the printed version of the contract manually using ink and send it back to the requestor
            -   The requestor uploads the digital copy of the contract, and on the closure of the request, the final contract is emailed to the stakeholders
        -   Support for a configurable system property \(sn\_lg\_contracts.enable\_executed\_contract\_audit\_certificate\) to generate a certification of completion that contains an audit trail along with timestamp details about each signatory action during electronic signature. This feature is supported for NDAs and third-party contracts
            -   The system property is set to false by default and needs to be enabled on as needed. This is supported for both AdobeSign and DocuSign
            -   The audit trail in the certificate of completion ensures non-repudiation and resolves any objections.
        -   Google Drive supports NDA as well as Third-Party Contract Review for creating, storing revisions, and adding attachments while composing emails
        -   For third-party contract intake forms, the Generate Document from Template option should not be enabled
-   **Version 5.0.3 - February 2023**

    New:

    -   -   Workflow for third-party contract review request
-   Added a new fieldAttributesin the Electronic Signature integration form. It has one attribute calledHost URLto add the default URL of the configured electronic signature provider.
-   Added a new tableContract Type \[sn\_lg\_contracts\_type\] to store contract types.
-   Added a new fieldContract typein theHTML Document Template and PDF Document Template forms to associate the template with a contract type. All active contract types from thesn\_lg\_contracts\_typetable are listed in this field.
-   Added a new Performance Analytics Indicator called Third Party Contract Review for legal requests for third-party contract reviews. The report widgets in the Legal Executive dashboard are updated to include this new PA Indicator.
    -   Changed:
        -   Added Legal Practice Apps core dependency
        -   Preview or Document revision tabs are visible depending on the internal or external storage of attachments respectively
        -   Renamed theContract Draft \[sn\_lg\_contracts\_contract\_draft\] table toDocument Revision.
-   **Version 4.2.2 - November 2022**

    Changed:

    -   Renamed the Simple Contracts module under the Legal Administration module to Simple Contracts Admin.
    -   Updated the legal\_matter\_config role to allow managing contract templates and document templates.
-   **Version 4.1.0 - August 2022**
    -   Fixed:
        -   Fixed the issue where the contract draft was not being generated if the External Signatories variable set was not configured in the record producer.
        -   Fixed the issue where the contract type in the request details was not showing as per the category.
-   **Version 3.2.3**

    Fixed: The placeholder for various signatories in the document template is fixed so that the signatures are enforced only at the designated place.

-   **Version 3.1.2 - February 2022**

    New: Get insight, analyze trends, and drill down into the details of Simple Contracts requests from the new Legal Executive dashboard, which is installed via Performance Analytics Content Pack for Legal Service Delivery app.

-   **Version 2.1.4 - December 2021**
    -   New:
        -   Added new module Template Blocks under Legal Administration &gt; Simple Contracts to create template blocks for legal contracts HTML templates
        -   Added the Document Template Blocks related list on the Document Template form
    -   Changed:
        -   Security-related changes
        -   Renamed external storage and electronic signature workflows
    -   Fixed:
        -   Fixed an issue where the scheduled job was timing out while pulling 500-600 records from CRM
        -   Fixed the error that was being displayed when a user opened the latest document revision record of a completed NDA request.
-   **Version 2.0.6 - September 2021**
    -   New:
        -   Submit a request for a Sales Contract when you have customer questions, to engage legal counsel, or need a review of the terms and conditions given by customers. The commercial legal team can review the sales contract and provide the requested contract support.
        -   Integrate with Microsoft Dynamics CRM to pull the sales accounts and opportunities data into the ServiceNow instance for generating a sales contract.
        -   Integrate with Google Drive and Microsoft OneDrive to save the signed contract documents into these external file storage systems.
-   **Version 1.4.2 - June 2021**
    -   New:
        -   Library of templates for standard contract documents such as Non-disclosure Agreements \(NDA\)
        -   Centralized repository of all signed and finalized contract documents
        -   Send contracts for the electronic signature to external and internal signers


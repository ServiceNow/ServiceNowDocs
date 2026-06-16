---
title: Document Templates release notes
description: Version history for the Document Templates application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-document-templates.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Document Templates release notes

Version history for the Document Templates application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.0.0 - June 2026**
    -   Fixed:
        -   Backend security fixes and other minor defects
        -   PDF document generation defect where date fields are not populated correctly in stamped documents
-   **Version 27.1.1 - March 2026**

    Fixed: Minor Bugs and Defects.

-   **Version 27.1.0 - December 2025**

    New: Backend Security Enhancements

-   **Version 27.0.0 - August 2025**
    -   New:
        -   ​Signing support for PDF templates on Mobile Browser and Now Mobile \(for following signing types : ServiceNow Sign , AdobeSign , DocuSign\)​
        -   Full window signing experience for Document Templates on Employee Centre , Now Mobile, Mobile Browser and Platform \(for following signing types : AdobeSign and Docusign\)​
        -   Signing support for Document Templates directly from HR Agent Workspace via one-click redirection \(for following signing types : AdobeSign and DocuSign\)​
        -   Filling/Reviewing PDF Document Templates directly from HR Agent Workspace \(for following signing types : ServiceNow Sign\)
-   **Version 26.4.2 - June 2025**

    Fixed: Minor bugs.

-   **Version 26.4.1 - May 2025**
    -   4 issues fixed as a part of this release:
        -   Document templates in Edit mode does not delete old attachments
        -   Tick box field is getting cleared while Saving/Submitting the form
        -   Unable to delete header or footer image from HTML document template
        -   \[UIElevation\_Theming\_CoreUI\] - Unable to see the signatures with coral dark theme
-   **Version 26.4.0 - February 2025**

    Fixed: Minor bug fixes and security improvements.

-   **Version 26.3.1 - November 2024**

    Fixed: Minor bug fixes and minor security improvements.

-   **Version 26.2.0 - August 2024**
    -   Fixed following bugs and reported defects:
        -   HTML Document Templates are showing extra spaces after variables of type "Date"
        -   Security issues around Cross-Site Scripting \(XSS\)
        -   Date field display related issues
        -   Document Template is being saved without updating the participants when table name is changed.
        -   User Date format affecting custom date field in document templates.
        -   Save and Submit button on Document task on portal is causing Discrepancies when used one after the other
        -   few minor defect fixes
    -   New: Guided tours introduced for DT
-   **Version 26.1.0 - May 2024**
    -   Added Automatic Signature Date in PDF Templates for ServiceNow signing type.
    -   Fonts used in HTML Templates are now rendered correctly in the HTML Preview page for Document Templates v25.0.2.
-   **Version 26.0.0 - February 2024**
    -   A new signature type 'Digital Signature - Smart Cards' is introduced for PDF Templates
        -   This enables you to create PDF Document Templates with Digital Signature capabilities.
        -   You can digitally sign a PDF document using CAC/PIV cards or Smart Cards.
        -   This feature is available only when the 'Document Template integration with Digital Signatures using Smart Cards' store plugin is installed along with Document Templates.
-   **Version 25.3.1 - January 2024**

    Fixed: Improved tables' security by fixing the ACLs with empty roles.

-   **Version 25.3.0 - November 2023**
    -   New:
        -   Ability to define 'Template level Date format'
        -   Ability to define 'Template Language' for dynamic fields translation
    -   Fixed:
        -   Mandatory validation for PDF checkboxes are not working
        -   ACL Bypass via 'sn\_doc\_preview\_pdf' UI Page
        -   Document content and sign tags are not loaded properly for the HTML doc tasks using Docusign
        -   Participants don't appear in the Word Template mapping fields \(only in an upgraded instance\)
-   **Version 25.0.2 - August 2023**
    -   New:
        -   Manage template versions with start and end dates;
        -   E-signature support extended for PDF and Word templates
        -   Support for internal and external participants for E-signatures
        -   Technical/backend changes to support Word Templates integration
-   **Version 24.1.0 - May 2023**
    -   New:
        -   For HR cases associated with HTML document templates, introduced the ability to cancel the document tasks associated with parent HR case when a parent case gets cancelled.
        -   Admins can de-activate the business rule associated with this capability if they do not want the document tasks to be cancelled when the associated parent HR case gets cancelled.
        -   The Preview Document modal in an HR Case now supports the display of dynamic content instead of variables in the Edit mode.
-   **Version 24.0.0 - February 2023**
    -   New:
        -   Rejection flows in document tasks have been introduced for HTML Document templates. A participant can choose to decline to sign the document once the task is assigned. While declining, the participant can provide the reasons for declining the task. The agent working on the case would be able to see the reasons provided by participant as Additional comments in activity stream. If required, the agent can make changes to the content of the document in the Preview Document modal and save the document. The document tasks can be initiated for participants with the updated document.
        -   Rejection flows in document tasks of HTML Document Templates work with ServiceNow signing and with integrations such as AdobeSign and DocuSign.
        -   Upgraded the mobile list card views and mobile input form screens for Document Templates.
            -   A script action reverts old card views with new card views. If there are customisations done on legacy cards, the script retains the legacy cards and does not replace them with new cards.
            -   A script action inactivates new function instances if customisations are done on legacy function instances or its related records. If no customisations are done, then existing function instances will be inactivated.
-   **Version 22.2.1 - January 2023**

    Fixed: FSM Agent Mobile - Sign &amp; PDF generation not working in both iOS and android with latest document templates.

-   **Version 22.2.0 - November 2022**
    -   New: Variables will be supported in Document Template Configuration
    -   Fixed: Accessibility issues related to 200% zoom
-   **Version 22.1.0 - August 2022**
    -   New:
        -   Enable agents in the Agent Workspace to create document tasks from HTML Doc Templates
        -   Enable participants to sign the document tasks created from HTML Doc Templates in Agent Workspace
        -   Mark the participants in the Document template optional via the Optional field so that if the participant is empty the document task is not created for this participant.
        -   Configure participants in the Document template using advanced scripting.
-   **Version 22.0.1 - May 2022**

    Fixed: Fix for emails related to document tasks were not visible to users having access to Document Task Record.

-   **Version 22.0.0**

    Changed: Technical/backend changes to support e-signature integrations

-   **Version 21.0.0 - February 2022**

    With the ServiceNow® Document Templates application, you can create HTML and PDF document templates to generate standard letters or documents. You can automate and simplify the process of filling, signing, and reviewing a document online.



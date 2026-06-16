---
title: Document Template integration with AdobeSign release notes
description: Version history for the Document Template Integration with AdobeSign on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-document-template-adobesign.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Document Template integration with AdobeSign release notes

Version history for the Document Template Integration with AdobeSign on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - June 2026**

    Fixed: Backend security fixes and other minor defects

-   **Version 1.7.0 - December 2025**

    New: Backend Security Enhancements.

-   **Version 1.6.6 - February 2025**

    Fixed: Minor bug fixes.

-   **Version 1.6.5 - November 2024**

    Fixed: Minor bug fixes and minor security improvements.

-   **Version 1.6.4 - August 2024**

    Fixed: Initiate document task creation failure if the participant email is empty.

-   **Version 1.6.3 - May 2024**

    Minor fix.

-   **Version 1.6.2 - February 2024**

    Minor fixes.

-   **Version 1.6.0 - November 2023**
    -   New: The getPrefilledBody method consumes the Template Date and Template Language parameters.
    -   Fixed:
        -   An internal participant overridden with an email causes the x,y position loss for the participant on PDF templates
        -   Generated pdf name after signing contains 'Unsigned\_'
-   **Version 1.3.1 - August 2023**

    Extended the external signing support for PDF and Word document templates. In earlier releases, this capability was available only for HTML document templates.

-   **Version 1.2.0 - May 2023**

    New:

    -   For HR cases associated with HTML document templates, introduced the ability to cancel the document tasks associated with parent HR case when a parent case gets cancelled.
    -   Admins can de-activate the business rule associated with this capability if they do not want the document tasks to be cancelled when the associated parent HR case gets cancelled.
-   **Version 1.1.0 - February 2023**

    New: A participant can choose to decline to sign the document from AdobeSign application. While declining, the participant can provide the reasons for declining the task. The agent working on the case can view the reasons provided by participant as Additional comments in activity stream. If required, the agent can make changes to the content of the document in the Preview Document modal and save the document. The document tasks can be initiated for participants with the updated document.

-   **Version 1.0.7 - November 2022**

    Minor optimization and refactoring

-   **Version 1.0.5 - August 2022**

    New: Support for optional participants in Document templates

-   **Version 1.0.0 - March 2022**

    With this ServiceNow® application, you can create HTML document templates to generate standard letters or documents, and enable the e-signature capabilities of Adobe Sign with Document Template.


**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)


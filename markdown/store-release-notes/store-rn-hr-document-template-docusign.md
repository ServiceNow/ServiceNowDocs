---
title: Document Template integration with Docusign release notes
description: Version history for the Document Template integration with Docusign on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-document-template-docusign.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Document Template integration with Docusign release notes

Version history for the Document Template integration with Docusign on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.1 - March 2026**

    Fixed: Minor Defects.

-   **Version 1.7.0 - December 2025**

    New: Backend Security Enhancements

-   **Version 1.6.4 - August 2025**

    Minor improvements and bug fixes.

-   **Version 1.6.3 - February 2025**

    Fixed: Minor bug fixes.

-   **Version 1.6.2 - November 2024**

    Fixed: Minor bug fixes and minor security improvements.

-   **Version 1.6.1 - May 2024**

    Minor fix.

-   **Version 1.6.0 - November 2023**
    -   New: The getPrefilledBody method consumes the Template Date and Template Language parameters.
    -   Fixed: Error while generating the signing URL.
-   **Version 1.3.0 - August 2023**

    Extended the DocuSign signing capability to PDF and Word document templates. In the earlier releases, this capability was available only for HTML document templates.

-   **Version 1.2.0 - May 2023**

    New:

    -   For HR cases associated with HTML document templates, introduced the ability to cancel the document tasks associated with parent HR case when parent case gets cancelled.
    -   Admins can de-activate the business rule associated with this capability if they do not want the document tasks to be cancelled when the associated parent HR case gets cancelled.
-   **Version 1.1.0 - February 2023**

    New: A participant can choose to decline to sign the document from DocuSign application. While declining, the participant can provide the reasons for declining the task. The agent working on the case can view the reasons provided by the participant as Additional comments in activity stream. If required, the agent can make changes to the content of the document in the Preview Document modal and save the document. The document tasks can be initiated for participants with the updated document.

-   **Version 1.0.7 - November 2022**

    Minior optimization and refactoring

-   **Version 1.0.6 - August 2022**

    Fixed: Fixed for Optional participants in Document Template.

-   **Version 1.0.4 - May 2022**

    Fixed: Fix for DocuSign flow errors when using automatic document task initiate and document template do not contain any string tokens.

-   **Version 1.0.1 - March 2022**

    With this ServiceNow® application, you can create HTML document templates to generate standard letters or documents, and enable the e-signature capabilities of DocuSign with Document Template.



---
title: Supplier Collaboration Portal release notes
description: Version history for the Supplier Collaboration Portal application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-slm-supplier-collaboration-portal.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Supplier Lifecycle Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Supplier Collaboration Portal release notes

Version history for the Supplier Collaboration Portal application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.0 - June 2026 \(Australia\)**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 8.0.0 - June 2026 \(Zurich\)**

    Fixed: Improved access controls for better security.

-   **Version 5.9.2 - June 2026**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 7.0.0 - March 2026**
    -   New:
        -   Supplier contacts can view and upload documents directly through the Supplier Collaboration Portal, without requiring initiation from a Supplier Manager.
        -   Monitor and enforce time-bound documents from suppliers.
            -   -   Provides escalation pathways if document upload tasks are not completed.
-   Enables admins to configure document lead time, grace period, and reminder frequency.
-   Supplier managers or contacts can fill in the expiry date while uploading documents. Based on this, automated upload document tasks are created \(Supported only in the Australia release\).
        -   Assess supplier performance at scale powered by the Smart Assessment Engine application.
            -   Bulk distribution via segmentation rules: Map assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one-off outreach.
            -   Internal stakeholder completion: Sourcing and procurement teams complete assessments in the Source-to-Pay Workspace, keeping evaluations centralized and auditable.
            -   Supplier self-service completion: Supplier contacts complete their portion through the Supplier Collaboration Portal, reducing follow-up cycles and accelerating response times.
-   **Version 5.6.0 - March 2026 \(Yokohama\)**
    -   New:
        -   Supplier contacts can now view and upload documents directly through the Supplier Collaboration Portal, without requiring initiation from a Supplier Manager.
        -   Monitor and enforce time-bound documents from suppliers.
            -   The workflows enhance supplier document capabilities by:
                -   Providing users with escalation pathways if document upload tasks are not completed.
                -   Enabling admins to configure document lead time, grace period, and reminder frequency.
            -   Ensures seamless management of documents with expiration dates and reduces manual oversight and follow-ups on renewals.
        -   Assess supplier performance at scale powered by the Smart Assessment Engine application.
            -   Bulk distribution via segmentation rules: Associate assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one-off outreach.
            -   Internal stakeholder completion: Sourcing and procurement teams complete assessments in the Source-to-Pay Workspace, keeping evaluations centralized and auditable.
            -   Supplier self-service completion: Supplier contacts complete their assessments through the Supplier Collaboration Portal, reducing follow-up cycles and accelerating response times.
-   **Version 5.0.0 - August 2025**

    Fixed: Minor fixes.

-   **Version 4.1.0 - May 2025**

    Minor fixes.

-   **Version 3.0.1 - February 2025**
    -   New:
        -   Enables effortless access to supplier contact information across multiple suppliers with a single set of login credentials
        -   Centralises case and task tracking from various suppliers, enhancing efficiency within a single platform
    -   Fixed: Minor fixes
-   **Version 3.0.0 - December 2024**
    -   New:
        -   Enables effortless access to supplier contact information across multiple suppliers with a single set of login credentials.
        -   Centralises case and task tracking from various suppliers, enhancing efficiency within a single platform.
-   **Version 2.8.0 - November 2024**

    New: Supplier Contact will be able to provide input for KPI from supplier collaboration portal.

-   **Version 2.7.0 - August 2024**
    -   New:
        -   View information related to suppliers in these new tiles within the My active items widget of the Supplier Collaboration Portal:
            -   Contracts
            -   Supplier Products
            -   Purchase Orders
            -   InvoicesThese new tiles are displayed if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) and Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugins.
-   **Version 2.6.0 - May 2024**

    New: You can now view supplier risk assessment details from the My active items widget in the Supplier Collaboration Portal. In the My active items widget, the Risk Assessments tile shows assessments only if you've installed the Third-party Risk Management \[com.sn\_vdr\_risk\_asmt\] plugin. Select the Risk Assessments tab to open the Assessment Summary page, which displays a list of risk assessments for a supplier \(third-party\) and for an engagement.

-   **Version 2.5.0 - February 2024**

    Minor fixes.

-   **Version 2.4.2 - November 2023**
    -   New:
        -   You can now specify a category while adding a supplier location. The choices are:
            -   Contracting address
            -   Delivery address
            -   Facility \(default\)
            -   Headquarters
            -   Invoice address
            -   Service center
        -   You can now directly remove a supplier contact by selecting the cross icon \(X\) next to the supplier contact name in the My contacts widget.
        -   You can now view details about the case in the Case Details tab for a newly opened request.
        -   The following catalog items have been added:
            -   Enroll a new user: Enables you to submit a request to add a new supplier contact.
            -   Deactivate user account: Enables you to submit a request to remove a supplier contact.
        -   Changed:
            -   The following catalog items have been renamed:
                -   "Add or remove location" renamed to "Update location details".
                -   "Submit an issue" renamed to "Submit or report an issue".
                -   "Something else" renamed to "General inquiry".
                -   "Request elevated access" renamed to "Request an access change request".
-   **Version 2.3.3 - August 2023**
    -   New:
        -   You are no longer required to approve restricted caller access \(RCA\) privileges after installing the Supplier Collaboration Portal. However, you may have to approve RCA privileges if the application prompts you to do so.
        -   A new system property, sn\_supplier\_sp.allow\_all\_apps\_configuration has been added, which allows activity configurations and filters accessible from all application scopes. By default, this system property is set to false. If you set this system property to true, you can create or modify an activity configuration to display relevant activities in My active items widget of the Supplier Collaboration Portal.
-   **Version 2.2.0 - May 2023**

    New: Using Agent Chat, supplier contacts can now start a chat session from the Supplier Collaboration Portal and interact with supplier fulfillers and get immediate responses to their queries or issues.

-   **Version 2.0.0 - February 2023**

    New: The Supplier Collaboration Portal no longer has a dependency on the Supplier Lifecycle Management application \(com.snc.sn\_supplier\_mgmt\), instead the portal now has a dependency on the Supplier Common application \(com.snc.sn\_slm\). This makes the portal a standalone application but with limited functionality. You need to purchase Supplier Lifecycle Management to take advantage of the complete functionality of the Supplier Collaboration Portal.

-   **Version 1.5.2 - December 2022**

    Minor fix.

-   **Version 1.5.0 - November 2022**
    -   New:
        -   Primary contacts can do the following:
            -   Remove secondary contacts and assign their tasks to alternate contacts.
            -   Reassign specific types of tasks to other contacts.
            -   Elevate or restrict access to other contacts.
            -   Update email IDs of the secondary contacts.
            -   View a list of all the tasks, regardless of who the tasks are assigned to.
        -   Secondary contacts can submit the 'Request elevated access' catalog request to gain access to the privileges of the primary contact role.
    -   Changed: Improved the process of inviting contacts. The primary contacts can now specify the access roles for the contacts being invited. The My team widget has been renamed to Contacts.
-   **Version 1.4.1 - September 2022**
    -   Fixed:
        -   Minor fixes and changes
-   **Version 1.4.0 - August 2022**
    -   New:
        -   Provides a seamless portal experience for supplier contacts
        -   Easily communicate and collaborate with the supplier manager
        -   Raise requests and get your questions answered quickly
        -   Perform various supplier tasks, such as updating banking details and supplier profile, using the service catalog
        -   Self-register to the Supplier Collaboration Portal and also invite other contacts to access the portal
-   **Version 1.3.0 - May 2022**
    -   New:
        -   Provides a seamless unified employee portal experience for supplier contacts
        -   Easily communicate and collaborate with the supplier manager
        -   Perform various supplier tasks, such as updating banking details and supplier profile, using the service catalog
        -   Self-register to the Supplier Collaboration Portal and also invite other contacts to access the portal


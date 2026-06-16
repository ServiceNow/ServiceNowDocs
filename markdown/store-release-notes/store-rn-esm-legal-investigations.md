---
title: Legal Investigations release notes
description: Version history for the Legal Investigations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-investigations.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Legal Investigations release notes

Version history for the Legal Investigations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.11.0 - June 2026**

    Changed: Security enhancements

-   **Version 3.10.0 - March 2026**

    Fixed: 'Ethics' requests can now be submitted when the 'Provide the approximate date and time of the incident' field contains a current date with a past time.

-   **Version 3.7.0 - December 2025**

    Changed: Security enhancements.

-   **Version 3.6.0 - September 2025**

    Changed: Added additional ACLs on sn\_lg\_investigate\_m2m\_allegation\_party table.

-   **Version 3.5.1 - August 2025**

    Fixed: Added required RCA and cross scope within legal applications.

-   **Version 3.5.0 - May 2025**

    Changed: Improved Legal Investigations icon for improved space utilization in the intake form.

-   **Version 3.4.0 - November 2024**

    Fixed: The Ethics Complaints catalog item now only appears under the Ethics Requests category. Previously, it appeared in both Ethics Compliants and Legal Requests categories. This is now fixed.

-   **Version 3.3.1 - August 2024**

    Fixed: The quick link for submitting Ethics Complaints in Employee Center portal is now available.

-   **Version 3.2.10 - November 2023**
    -   Fixed:
        -   Ethics Complaints catalog removed from Legal Requests and Ethics Requests
        -   Adding or Removing involved parties and allegations is available
-   **Version 3.2.2 - August 2023**

    New: Changes for the Next Experience Legal Counsel Center.

-   **Version 3.1.0 - May 2023**

    Fixed: Minor fixes, which include client scripts and RCA, are added.

-   **Version 3.0.1 - February 2023**
    -   New:
        -   Complete data copy mapping is possible for the legal fulfillers to transfer legal ethics matter to HR employee relations and vice versa
            -   Anonymous Reporting Center Captcha works without depending on HR Security plugin
            -   The requester is added in the watchlist
            -   Transfer all documents from HR to Legal when external storage is enabled
            -   Users with non-legal roles can view the Ethics Complaint quick links
            -   In Universal Request create legal ticket, ethics matter template can be selected
            -   Apply default template from the legal side when an HR case is getting transferred to legal ethics matter.
            -   The description column is created in matter task to maintain consistency and support smooth transfer between HR Employee Relations tables and Legal Ethics tables
-   **Version 2.0.2 - November 2022**
    -   New:
        -   Update of Ethics complaints via Universal Requests:
            -   Added a new base system record producer for submitting universal requests for legal ethics complaints.
            -   Added the Quick Links option in the Employee Center portal for submitting a Universal Request to report an ethics complaint.
            -   Added a system property, default assignment group, to set the default assignment group for ethics complaints submitted through Quick Links in Employee Center.
            -   Added Ethics Complaints list item in Legal Counsel Center to show a list of all ethics complaint matters created through a universal request.
            -   Enabled creation of ethics complaint legal matters from an HR Ethics case while it is transferred through a Universal Request. All attachments from the HR case are also copied to the shared artifact of the legal matter. This transfer is possible if Employee Relations is the service in the HR case and Ethics Complaints is selected in the service for the Legal department.
            -   Enabled creation of a HR Ethics case from an ethics complaint legal matter while it is transferred through a Universal Request. All attachments from the legal matter are also copied to the HR case as attachments. This transfer is possible if Employee Relations is selected in the service for the HR department.
        -   Added the Properties module under the Legal Investigations Admin module in the Application Navigator.
        -   Added the base system Ethics matter template that is applied as default while creating a legal matter from Universal Request.
        -   Added the Document and Attachments tab in the Standard Ticket page, of which only one is visible based on whether the external storage is enabled:
            -   If external storage is enabled for ethics complaints, the Document tab is available for the requesters to see all documents in the shared artifact of their submitted ethics complaint matter.
            -   If external storage is enabled for ethics complaints, the Attachments tab is available for the requesters to see all documents in the shared artifact of their submitted ethics complaint matter.
    -   Changed:
        -   Renamed the Ethics Complaints module under the Legal Administration module to Legal Investigations Admin.
        -   Changes to Ethics complaints via Universal Requests:
            -   If the ticket type while transferring is selected as Ethics Complaints, then a legal matter is created and made as the primary ticket of the universal request. Attachments from the universal request are copied to a shared artifact in the legal matter.
            -   Renamed the Enable legal request creation from universal request option in the Intake Form's Options field to Enable Legal Ticketing in Universal Request.
            -   Renamed the Create Legal Request button on the Universal Request form to Create Legal Ticket.
            -   Mapped Ethics Complaints service configuration in Universal Request to the Ethics \[sn\_lg\_matter\_ethics\] table.
-   **Version 1.0.0 - August 2022**

    ServiceNow Legal Investigations is a Legal Practice app included with Legal Service Delivery that enables Legal departments to accept anonymous or named complaints from a simple intake process. Guided matter templates help the legal team organize and conduct detailed legal investigations including interviews, gathering evidence, and preparing final reports along with recommended actions.



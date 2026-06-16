---
title: Public Sector Digital Services Core release notes
description: Version history for the Public Sector Digital Services Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-public-sector-digital-services-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Public Sector Industry release notes, ServiceNow Store release notes]
---

# Public Sector Digital Services Core release notes

Version history for the Public Sector Digital Services Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.1 - June 2026**
    -   Security Enhancements
    -   Defect Fixes
-   **Version 13.0.10 - May 2026**

    Incremental Release with Enhancements and Java 21 Support

-   **Version 13.0.9 - April 2026**

    Defect fixes for localisation, functional and accessibility issues.

-   **Version 13.0.0 - March 2026**
    -   Updated Psds Core to facilitate Investigative Case Management application.
    -   Bug fixes to ensure better overall quality and adaptability
-   **Version 12.21.2 - February 2026**
    -   New:
        -   Added dynamic, configurable filtering across GSP portal lists. All filters are multi-select; date fields support ranges.
        -   sn\_gsm\_government\_service\_case: Business, Business contact, State, Priority; Opened \(range\), Updated \(range\)
        -   sn\_customerservice\_task: Priority, State, Subject, Visible to Customer
        -   sn\_gsm\_service\_request\_case, sn\_gsm\_information\_request\_case, sn\_gsm\_license\_permit\_case: Constituent, Business, Business contact, State; Reported date \(range\)
        -   sn\_gsm\_social\_benefits\_case: Product, Constituent, Business, Business contact, Stage, State, Assigned to; Reported date \(range\)
        -   customer\_account: Name, Primary Contact, City, Zip/Postal code
        -   customer\_contact: Name, Business
        -   sn\_install\_base\_item: Contact
    -   Changed:
        -   /gsp homepage updated to new design; now uses Configurable Portal Widgets \(Banner, Mega Menu, Header/Footer, Data List, FAQ/Quick Links\).
        -   Enabled configurable widgets on pages: gov\_case\_list, gsp\_businesses, gsp\_business\_details, gsp\_contacts, gsp\_contact\_details, gsp\_receieved\_items, gsp\_receieved\_item\_details, gsp\_services\_detail. Lists use Data List search and filters.
-   **Version 12.2.4 - August 2025**
    -   New:
        -   Added Coral Theme Compatibility
        -   Added activities to support the Grants Management Playbook Application
            -   Result Letters
            -   Merit Reviewers
            -   Internal Program Team
            -   Funding Proposals
-   **Version 12.1.6 - August 2025**
    -   New
        -   Added Coral Theme Compatibility
        -   Added activities to support the Grants Management Playbook Application
            -   Result Letters
            -   Merit Reviewers
            -   Internal Program Team
            -   Funding Proposals
-   **Version 12.1.1 - May 2025**
    -   New:
        -   Added features to support the new Grants Management Playbook.
        -   Added support for the newly added Service Applicant Program Management plugin, which is a comprehensive application that aids in the setup and configuration of applicant programs.
-   **Version 11.1.5 - May 2025**

    Fixed: Resolved an issue where pre-eligibility questions loaded incorrectly when decision tables were copied for implementation.

-   **Version 12.0.4 - February 2025**
    -   Changed: Migrated the legacy 'Account/Business Registration' workflow to be a low code solution.
    -   Fixed: Improved security to better prevent inadvertent access to constituent/business contact data.
-   **Version 11.1.4 - January 2025**
    -   Changed: Migrated the legacy 'Account/Business Registration' workflow to be a low code solution.
    -   Fixed: Improved security to better prevent inadvertent access to constituent/business contact data.
-   **Version 11.1.2 - November 2024**
    -   Changed:
        -   Migrated account/business registration workflow to low code solution
        -   Updated plugin dependencies
        -   Added new property page
-   **Version 11.0.2 - August 2024**

    Changed: Ensure PSDS core is fully compatible with Java Development Kit \(JDK\) 17.

-   **Version 10.0.5 - June 2024**
    -   Fixed:
        -   Resolved accessibility issues
        -   Updated API call to glide plugin manager when checking if a plugin exists
-   **Version 10.0.2 - May 2024**

    New: Extended the PSDS data model via the new Service Applicant Information plugin to store financial datasets needed for the Social Benefits and other playbooks.

-   **Version 9.0.1 - February 2024**

    Changed: Promoted the Fee Waiver and Fee Waiver Justification attributes from the Information Request entity to the Government Base Case entity.

-   **Version 8.0.2 - November 2023**
    -   Changed:
        -   Uptake of CSM Service definition changes for case tasks
        -   Agent workspace now supports auto-reflow to transform page layouts into a stacked view automatically when agents zoom their screen up to 400%. Auto-reflow can be turned off with a system property for instances, experiences, and pages.
        -   The Performance Analytics dashboard has been migrated to Next Experience
-   **Version 7.0.3 - August 2023**

    New:

    -   Use the Business Location service portal in Public Sector Digital Services to request specific services and submit cases against agency locations, sold products, or install base items at a service organization.
    -   Use service definitions to connect services and case types, and extend service definitions to case tasks. Agents can create case tasks by selecting from a list of install base items or public services, and then by selecting from a list of available task types.
-   **Version 6.0.0 - May 2023**
    -   Changed:
        -   Business data model - New and updated fields in the Business data model, such as Legal entity name, Trademark, Tax ID, and more, are reflected in the CSM Configurable Workspace and in profile attributes, such as Veteran Status, set in the Government Service Portal.
        -   Constituent data model - New and updated constituent fields in the Constituent data model are reflected in the CSM Configurable Workspace and in the Constituent profile attributes set in the Government Service Portal. The Constituent profile is an extension of the Consumer profile.
        -   Agency data model - Changes to related lists, such as Items received for Install base and Related parties are reflected in the CSM Configurable Workspace.
-   **Version 5.0.2 - February 2023**
    -   New:
        -   Enable government workers to add related parties to Services Received and Items Received, and enable authorized related parties to view items and services received and any cases created for them.
        -   Enable government workers to create new business record from interactions.
        -   Enable administrators to use Guided Setup to configure Public Sector Digital Services Core.
-   **Version 3.0.0 - August 2022**
    -   New:
        -   Government case types updates to support business services
        -   Self-service for businesses across registration, case tracking and customer information
        -   Agent workspace updates to support 360 degree view of business and agencies
        -   Roles for government agents and contributors servicing businesses
-   **Version 2.1.0 - May 2022**
    -   New: VA topic blocks to:
        -   Create Government cases for new services being requested or on an existing service
        -   Enable additional members to a case
-   **Version 1.3.0 - March 2022**

    Public Sector Digital Services is the digital platform modernizing government service delivery. Using a purpose-built foundation of data models, workflows and experiences tailored to governments and the people they serve, agencies are empowered to easily build new applications for any services they offer.



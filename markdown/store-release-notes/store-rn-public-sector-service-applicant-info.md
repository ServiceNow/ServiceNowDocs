---
title: Service Applicant Information release notes
description: Version history for the Service Applicant Information application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-public-sector-service-applicant-info.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Public Sector Industry release notes, ServiceNow Store release notes]
---

# Service Applicant Information release notes

Version history for the Service Applicant Information application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.1 - June 2026**

    Defect fixes

-   **Version 3.2.0 - May 2026**

    Incremental release with enhancements and Java 21 support

-   **Version 3.0.5 - April 2026**

    Defect fixes for localisation, functional and accessibility issues.

-   **Version 3.0.1 - March 2026**

    Minor fixes.

-   **Version 2.21.1 - February 2026**
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
-   **Version 1.2.5 - September 2025**

    Fixed: Confirm Application activity was skipped when a new Social Benefits case was created

-   **Version 2.2.2 - August 2025**
    -   New:
        -   Added additional capabilities for the generic activity UI used for various playbook activities in the grants management playbook
        -   Coral theme compatibility
    -   Fixed: Upload and Verify Document Activity UI CSS Fixes
-   **Version 1.2.4 - May 2025**

    New: Added fields in the applicant data model to support capturing additional information.

-   **Version 2.0.3 - February 2025**

    Fixed: Improved security to better prevent inadvertent access to constituent/business contact data.

-   **Version 1.2.3 - January 2025**

    Fixed: Improved security to better prevent inadvertent access to constituent/business contact data.

-   **Version 1.2.2 - November 2024**
    -   Changed:
        -   Migrated account/business registration workflow to low code solution
        -   Updated plugin dependencies
        -   Added new property page
-   **Version 1.1.0 - August 2024**

    Fixed: Ensure Government Admin roles can now view the full Service Applicant Information module as well as the appropriate product model menu options.

-   **Version 1.0.4 - June 2024**
    -   Fixed:
        -   Resolved accessibility issues
        -   Updated API call to glide plugin manager when checking if a plugin exists
-   **Version 1.0.2 - May 2024**

    This new plugin will enable customers to capture additional information entered during the case creation/application process. It includes a data model and corresponding custom UIs to facilitate storing new applicant information as well as their associated financial information.



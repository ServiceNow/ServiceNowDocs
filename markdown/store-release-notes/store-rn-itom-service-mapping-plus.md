---
title: Service Mapping Plus release notes
description: Version history for the Service Mapping Plus application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-mapping-plus.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Mapping Plus release notes

Version history for the Service Mapping Plus application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.21.0 - June 2026**

    Fixed: UI enhancements in the multi-source mapping flow.

-   **Version 1.20.0 - May 2026**

    NewSupport for IIS server candidate creation and CMDB-based mapping.FixedEnhanced and fixed the alignment, UI and performance issues related to multi-source service mapping.

-   **Version 1.19.0 - April 2026**
    -   Fixed: Multi-Source Mapping:
        -   1. Ensure all matching results are aligned with the top recommendation list on the Find and Select Service Instance step.
        -   2. When unifying two tag-based unmapped services, and one service get's mapped along the process- searching for related services will result in suggesting the  service as mapped.
        -   3. The loading delay observed when clicking 'Review and Create' in the sidebar has been resolved.
-   **Version 1.18.3 - March 2026**

    New: Introducing Multi-Source Service Mapping – gain a single, trusted view of your services by eliminating fragmented maps and blind spots across discovery and service mapping methods. Unify top-down, tag-based, and ML-powered services into composite service maps. Using a unified service view enables your teams to troubleshoot faster, understand dependencies at a glance, and make better service-aware decisions.

-   **Version 1.17.2 - January 2026**

    Now view the unified tag-based map from within the CMDB workspace.

-   **Version 1.17.0 - December 2025**

    New: Now view the unified tag-based map from within the CMDB workspace

-   **Version 1.16.3 - August 2025**
    -   New:
        -   A tag-based mapping workspace that helps you visualize and manage tag-based services more efficiently.
        -   Additional properties added to improve and improve the information included in application service candidates.
    -   Changed:
        -   Improved filtering of non-operational or retired servers.
        -   Improved filtering of noise from application service candidates and Service Fingerprints.
-   **Version 1.15.2 - May 2025**

    Changed: A limit of 200 service candidates generated per tag-based service family.

-   **Version 1.15.0 - February 2025**

    New: Added Service Fingerprint as a source in the Name Suggestion - In the application Service Suggestions tab for ML powered Candidates, the application service candidates will now have Service Fingerprint as one of the sources in the Name Suggestion.

-   **Version 1.14.1 - November 2024**
    -   New: Service fingerprint - new tab on ML candidates page that shows application service ML candidates grouped by service fingerprint of smart content.
    -   Fixed: Several PRB fixes
-   **Version 1.13.0 - August 2024**
    -   New: Filters for avoiding redundant recomputations on discovered and tag-based services
    -   Changed:
        -   Added columns "install status" and "class" to 'Unmapped servers without candidate' list in Service mapping plus navigation page.
        -   Added a filter to show most recent discovery in the last 90 days
-   **Version 1.12.3 - May 2024**

    Changed: Disabled Application service candidates - smart EP naming job

-   **Version 1.11.1 - February 2024**
    -   New: Preview Map for ML Powered Candidates loads Unified Map
    -   Changed:
        -   Support for Page Layout 3.0
        -   UX improvements
-   **Version 1.10.3 - December 2023**

    Fixed: Fixed regression in Readiness page job stuck messages.

-   **Version 1.10.0 - November 2023**

    New ACL and ACL role added for table sa\_ml\_application\_service\_candidate\_to\_server.

-   **Version 1.9.0 - August 2023**
    -   New:
        -   Domain separation support was added for this application.
            -   In domain-separated instances only leaf domains can use the app features.
    -   Fixed:
        -   Absent connections will not be shown in the candidate preview map.
        -   Includes valid operational status and install status in the candidate similar to TD behavior.
-   **Version 1.8.0 - May 2023**
    -   What's New: Automated Service Suggestions:
        -   Update existing application services based on service suggestions that are generated using Machine Learning. 
        -   Two new sources for candidate name suggestions \(loadbalancer name &amp; process name\)
        -   Candidate name suggestion and candidate name suggestion source fields are populated according to the priority list.
    -   Service Mapping Homepage:
        -   Search for a server on the homepage
        -   Click the Populate Data button on the homepage to refresh all the tiles and widgets with the latest data on the homepage.
        -   Visualize the count of mapped application services, ML-powered candidates, Mapped servers, and Unmapped servers and get the records in the form of a list by clicking the respective tiles on the homepage.
        -   Widgets that display the data of application services based on their operational status, creation method, and business criticality and show the respective list on clicking the widgets Changed
        -   Access the ML-powered candidates from the homepage.
        -   Access the Readiness Dashboard by clicking the checklist icon on the side navigation on the new homepage
    -   Fixed: Automated Service Suggestions:
        -   Disable service suggestions with IPV6 IP addresses.
        -   Disable service suggestions with invalid host status.
-   **Version 1.6.0 - November 2022**
    -   New: Automated Service Suggestions - Create application services based on service suggestions that are generated using Machine Learning.
    -   Changed: The retry logic should skip retry on the 'Failed due to missing artifacts' update state. Added automation to clean the existing solution and restart AFP and P2P jobs from scratch.
    -   Fixed:
        -   ML Dashboard
            -   AFP estimation time is calculated incorrectly for a small number of processes.
            -   P2P estimation time is calculated incorrectly for a small number of processes.
            -   P2P return value isn't consistent for a run load of zero process TP upgrade.
            -   The link for "View the Process to Process Connection table" doesn't open in a new window.
            -   When drilling down from an empty state to the connection suggestion table, irrelevant records are displayed.
            -   Filter on service issues does not handle the use case properly.
            -   Filter on service issues does not reveal the problem in each suggestion.
-   **Version 1.0.2 - February 2022**

    Service Mapping Plus offers extended features for Service Mapping. Particularly, an updated version of mapping based on Machine Learning \(Predictive Intelligence\) is available.



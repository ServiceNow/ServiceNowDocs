---
title: Pre-Visit Management release notes
description: Version history for the Pre-Visit Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-previsit-mgmt.html
release: store
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Pre-Visit Management release notes

Version history for the Pre-Visit Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.1.2 - February 2025**

    Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the Deprecation Process \[KB0867184\] article in the Now Support Knowledge Base.

-   **Version 8.0.1 - January 2025**
    -   Fixed:
        -   Adjusted access to the sn\_previsit\_procedure\_request\_list table as follows:
            -   Removed read/write access from sn\_previsit.sm\_agent role.
            -   Added read/write access to sn\_previsit.patient\_service\_agent and sn\_previsit.agent\_connector roles.
-   **Version 9.1.1 - December 2024**
    -   Fixed:
        -   Adjusted access to the sn\_previsit\_procedure\_request\_list table as follows:
            -   Removed read/write access from sn\_previsit.sm\_agent role.
            -   Added read/write access to sn\_previsit.patient\_service\_agent and sn\_previsit.agent\_connector roles.
-   **Version 8.0.0 - August 2024**

    New: Added minor improvements to true up to the Xanadu release.

-   **Version 7.0.0 - May 2024**

    Removed: Deprecated the old dashboards from the application.

-   **Version 6.0.0 - February 2024**

    New: Added minor enhancements to true up to the Washington DC release.

-   **Version 4.0.0 - November 2023**

    Changed: Dashboards have been updated with improved data visualizations and navigation.

-   **Version 3.0.0 - August 2023**

    Minor fixes to true up to Vancouver release.

-   **Version 1.4.0 - May 2023**

    Changed: Existing sn\_customerservice.customer\_data\_viewer role is now contained directly under sn\_previsit.agent\_connector. No change to role functionality.

-   **Version 1.3.1 - February 2023**
    -   Fixed:
        -   Issue where procedure request's patient 360 demographics populates incorrectly
        -   Issue where changing a case state to Closed Complete or Closed Incomplete still allows for operations in the playbook to occur.
    -   Removed: The 'Open list' button in playbook activities has been removed
-   **Version 1.2.0 - August 2022**
    -   New:
        -   Agent connectors and contributors for procedure request cases: Administer who can act as an agent connector or contributor for procedure request cases by assigning the following roles
            -   sn\_previsit.agent\_connector
            -   sn\_previsit.contributor
        -   Procedure request case contributors: Create procedure request cases for your patients with contributor profile from a service portal.
        -   Domain separation support in Pre-Visit Management: Use domain separation at the basic support level in Pre-Visit Management.
-   **Version 1.1.0 - May 2022**

    Changed: Playbook experience now handles consent management changes

-   **Version 1.0.2 - February 2022**

    Fixed: Minor bugs



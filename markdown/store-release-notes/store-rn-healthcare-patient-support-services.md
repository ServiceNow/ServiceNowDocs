---
title: Patient Support Services release notes
description: Version history for the Patient Support Services application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-patient-support-services.html
release: store
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Patient Support Services release notes

Version history for the Patient Support Services application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.0.2 - February 2025**

    Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the Deprecation Process \[KB0867184\] article in the Now Support Knowledge Base.

-   **Version 7.0.1 - February 2025**
    -   Updates made to give sn\_hcls\_patient for appropriate role access
    -   CSM query rules and Scripted ACLs added to the following tables:
        -   sn\_patientservice\_training\_task
-   **Version 8.0.0 - August 2024**

    New: Three new Automated Testing Frameworks tests were added.

-   **Version 7.0.0 - May 2024**

    New: Improved the Onbourd Medical Device record producer to be conformant with PID uptake.

-   **Version 6.0.0 - February 2024**

    New: Added minor enhancements to true up to the Washington DC release.

-   **Version 4.0.0 - November 2023**

    Changed: Dashboards have been updated with improved data visualizations and navigation.

-   **Version 1.5.3 - September 2023 \(Utah\)**

    Fixed: Issue causing slow ACL and response time.

-   **Version 1.3.3 - September 2023 \(Tokyo\)**

    Fixed: Issue causing slow ACL and response time.

-   **Version 3.0.0 - August 2023**

    Minor fixes to true up to Vancouver release.

-   **Version 1.5.0 - May 2023**

    Changed: Existing role sn\_customerservice.customer\_data\_viewer is now contained directly under sn\_patientservice.agent\_connector. No change to role functionality.

-   **Version 1.4.1 - February 2023**
    -   New: Error document has been added to appointment booking
    -   Fixed:
        -   Issue with enrollment case patient 360 demographics populating incorrectly
        -   Issue with filtering enrollment case patient 360
-   **Version 1.3.0 - August 2022**
    -   New:
        -   Agent connectors and contributors for enrollment cases: Administer who can act as an agent connector or contributor for enrollment cases by assigning the following roles
            -   sn\_patientservice.agent\_connector
            -   sn\_patientservice.contributor
        -   Enrollment case contributors: Create enrollment cases for your patients with contributor profile from a service portal.
        -   Domain separation support in  Patient Support Services Use domain separation at the basic support level in Patient Support Services.
    -   Removed: The sample Enrollment Request Form \[enrollment\_request\_form\] page was removed.
-   **Version 1.2.0 - May 2022**
    -   Changed:
        -   Playbook experience now allows creating a prescription based on configured dosage specifications for a program
        -   Playbook experience now handles consent management changes
-   **Version 1.1.0 - February 2022**

    Minor fixes.

-   **Version 1.0.1 - October 2021**

    Patient Support Services helps life sciences organizations overcome the hurdles faced when patients start therapy by removing financial barriers and streamlining onboarding so that therapy starts faster.


**Parent Topic:**[ServiceNow Store - Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-healthcare-highlights.md)


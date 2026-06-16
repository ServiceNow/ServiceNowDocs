---
title: Contact Tracing release notes
description: Version history for the Safe Workplace Contact Tracing application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-contact-tracing.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Contact Tracing release notes

Version history for the Safe Workplace Contact Tracing application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

**Note:** To automatically install all the Safe Workplace applications at once, download the ServiceNow® Safe Workplace suite application.

## Version history

-   **Version 1.30.2 - June 2026**

    Fixed: Remediated non-Glide ACLs

-   **Version 1.30.0 - August 2025**

    Changed: Minor ACL updates.

-   **Version 1.29.5 - November 2024**

    Security fixes.

-   **Version 1.29.4 - August 2024**
    -   Removed:
        -   The Zebra integration has been deprecated. Customers who have downloaded the 1.29.2 or any older version will continue to have the Zebra integration, and can continue to use it. Customers who have downloaded 1.29.4 or newer version of the app will NOT have the Zebra integration.
        -   The Devvio integration portal has been deprecated. Customers who have downloaded the 1.29.2 or any older version will continue to have the Devvio integration, and can continue to use it. Customers who have downloaded 1.29.4 or newer version of the app will NOT have the Devvio integration.
-   **Version 1.29.2 - May 2024**

    Security fixes.

-   **Version 1.29.1 - January 2024**

    Security fixes.

-   **Version 1.29.0 - November 2022**

    Fixed:

    -   Next Experience theming alignment
    -   Accessibility improvements
-   **Version 1.28.1 - August 2022**

    Fixed:

    -   Added a new role sn\_imt\_tracing.cisco\_admin. To continue using the cisco integration within the application, existing customers should assign this new role to relevannt users and re-login to their instance from within Cisco.
    -   Contact tracing demo data to be retained upon upgrade.
    -   Quality improvement.
-   **Version 1.26.0 - March 2022**

    Fixed: Minor bug

-   **Version 1.24.0 - January 2022**

    New: Localization for 22 languages other than English. Translations are available for features released up until the December 16, 2021 release.

-   **Version 1.23.1 - December 2021**

    Changed: Updates to the translation engine

-   **Version 1.22.0 - October 2021**

    Fixed: Minor bug

-   **Version 1.21.0 - September 2021**

    New: Localization for features from the August 19 release

-   **Version 1.20.0 - August 2021**

    Fixed: Minor bug

-   **Version 1.19.0 - July 2021**

    Changed: Updates to the translation engine

-   **Version 1.18.0 - June 2021**

    Fixed: Minor bug with data flows on upgrade

-   **Version 1.17.0 - April 2021**

    New: Localization for features from the March 25 release

-   **Version 1.16.0 - March 2021**
    -   New:
        -   View vaccination status on cards and the list of exposed contacts
        -   Ability to filter cards by vaccination status
    -   Fixed: Minor bug fix for the Kinexon wearables integration
-   **Version 1.15.1 - March 2021**

    New: Localization for features from the February 18 release

-   **Version 1.14.0 - February 2021**
    -   New:
        -   Support for Contact Tracing Exposure Surveys by SMS
        -   Localization for features from the February 4 release
    -   Fixed: Security fix
-   **Version 1.13.0 - February 2021**

    New:

    -   Contact Tracing visualizations were updated to include a third level hierarchy
    -   Localization for features from the January 21 release
-   **Version 1.12.0 - January 2021**

    New: Support for domain separation

-   **Version 1.11.0 - December 2020**

    New: Localization for features from the December 3 release

-   **Version 1.10.0 - December 2020**
    -   New: Localization for features from the November 19 release
    -   Fixed: The Handheld Devices menu option is now shown under the Handheld/Wearables section instead of Devvio
-   **Version 1.9.0 - November 2020**

    New:

    -   Devvio \(wearables data API\) integration
    -   Localization for features from the November 5 release
-   **Version 1.8.0 - November 2020**
    -   New:
        -   Health verifications are limited to once per day
        -   When a case task's Outcome is updated, the case's Exposed Contacts is also updated
        -   New catalog item icon for daily contact logs
        -   Localization for features from the October 15 release
    -   Fixed: Minor bug fixes
-   **Version 1.7.0 - October 2020**
    -   New:
        -   Default tasks are created when a new case is created
        -   Ability to add user notes on daily contact logs for interactions with non-coworkers, such as contractors
        -   Localization for features from the October 1 release
    -   Fixed:
        -   Case managers can now view attachments on cases
        -   Other minor bug fixes
-   **Version 1.6.2 - October 2020**
    -   New:
        -   Ability to set up a new tracing system for your own contact tracing data source. For users on previous versions of the Contact Tracing application, v1.6.2 includes an upgrade fix script.
        -   Employers can email potentially exposed individuals to request they get tested.
        -   Integration with Zebra MotionWorks.
    -   Changed:
        -   Updated the legend for Contact Tracing visualizations.
        -   Adjusted the case management 'Impacted from XX' fields to a single field, 'Tracing System.' No changes were made to manually-added fields.
        -   Daily contact logs now account for multiple potentially exposed contacts.
    -   Fixed: Minor bug fixes.
-   **Version 1.4.0 - September 2020**
    -   New:
        -   Update to data purging
        -   Daily Log - Timezone consideration
        -   Localization for the September 3 release features
    -   Fixed:
        -   Privacy Consent's 'Change Preference' link
        -   Flow Designer
        -   Badge Reader logic
-   **Version 1.3.0 - September 2020**
    -   New:
        -   Added the ability to use raw Wi-Fi data through an integration with Cisco DNA Spaces
        -   Created an outreach notification for exposed contacts
        -   Changed Contact Tracing visualizations with color coding for potentially exposed individuals
        -   Localization for features from the August 20 release
    -   Fixed: The color for the primary affected individual is correctly updated depending on the person's health status
-   **Version 1.2.0 - August 2020**

    New:

    -   Field Service application integration with Zoom
    -   Added a MIST BLE - API to get the BLE enabled sites
    -   Added a navigation menu for wearables
    -   Added support for Cisco DNA Spaces for Wi-Fi access log data
    -   Localization for features from the August 6 release
-   **Version 1.1.0 - August 2020**

    New:

    -   Changes on related cases
    -   Design changes for privacy consent
    -   Juniper MIST BLE integration
    -   Guided Setup updates
    -   Localization for features from the July 23 release
-   **Version 1.0.5 - July 2020**

    New:

    -   Wi-Fi data source \(import + Mist integration\)​
    -   Visitor data source​: Use data from the ServiceNow Employee Health Screening visitor screening feature as a data source for contact tracing
    -   Automated case creation​
    -   Ability to update Employee Health and Safety Requirement​ with status from case management​
-   **Version 1.0.4 - July 2020**

    New:

    -   Case Management - Confidential flag
    -   Contact Tracing
        -   Data retention management
        -   Privacy consent
        -   Localization for features from the June 18 release
-   **Version 1.0.1 - June 2020**

    The ServiceNow Contact Tracing application provides the capability to identify employees that may have been exposed to an individual classified as positive for a condition \(e.g. COVID-19\) by correlating information from work shifts, workspace locations, badge scans, and employee daily contact logs. The Contact Tracing application includes the capability to manage the response process related to these events.


## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)


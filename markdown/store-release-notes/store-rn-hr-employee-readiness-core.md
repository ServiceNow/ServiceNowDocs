---
title: Employee Readiness Core release notes
description: Version history for the Safe Workplace Employee Readiness Core on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-employee-readiness-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Employee Readiness Core release notes

Version history for the Safe Workplace Employee Readiness Core on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

**Note:** To automatically install all the Safe Workplace applications at once, download the ServiceNow® Safe Workplace suite application.

## Version history

-   **Version 1.43.0 - June 2026**
    -   Changed:
        -   Fixed ACL-role mismatches by validating role existence and ACL references
        -   Updated internal tooling alignment
        -   Remediated non-Glide ACLs
    -   Fixed: Resolved a security vulnerability where an arbitrary GlideRecord read was possible via SafeWorkplaceAudienceAjax in Employee Readiness
-   **Version 1.42.0 - December 2025**

    Fixed: Updated Read only fields to use new platform security features.

-   **Version 1.41.0 - August 2025**

    Changed: Minor ACL updates

-   **Version 1.40.3 - February 2025**
    -   New: Exposures on H&amp;S Profile for specific roles e.g. requestor
    -   Fixed: The display value of the user's name was incorrect when a new contractor record was created in the Health and Safety User table
-   **Version 1.40.2 - November 2024**

    Security fixes.

-   **Version 1.40.1 - May 2024**

    Security fixes.

-   **Version 1.40.0 - February 2024**

    Removed: The Testing Status dashboard and Vaccine Status dashboard have been deprecated. Customers who have downloaded the 1.39.0 or any older version will continue to have the dashboards and can continue to use them. Customers who have downloaded the 1.39.1 or newer version of the app will NOT have the dashboards.

-   **Version 1.39.1 - January 2024**

    Security fixes.

-   **Version 1.39.0 - November 2022**

    Fixed: Accessibility and quality improvements

-   **Version 1.38.2 - August 2022**
    -   Changed:
        -   Improved approval portal design to align to WCAG 2.0/WCAG 2.1 guidelines. This includes:
            -   Keyboard accessibility
            -   ARIA labels
            -   Screen readers
            -   Better icons
            -   Enabling 200% zoom
    -   Fixed:
        -   Provided access to health and safety admin to approve test results in approval portal.
        -   Added terminology to indicate booster dose in approval portal and differentiate it from normal dose.
        -   Performance and quality improvements.
-   **Version 1.37.0 - May 2022**
    -   New: Localization for features in the May 5 release.
    -   Changed:
        -   Added health\_and\_safety\_approver role for the Approval Portal.
        -   Managers have the ability to access the Approval Portal.
    -   Fixed:
        -   Added report\_view ACL to sn\_imt\_core\_test\_result\_history.
        -   Added sys\_domain field to sn\_imt\_core\_test\_result\_history and sn\_imt\_core\_vaccine\_history tables.
        -   Performance improvements to requirement activation process.
        -   Added scheduled job 'Remove inactive health and safety users' to periodically delete inactive Health and Safety Users.
        -   Syslog errors occured during installation due to the Caller Access setting on sn\_imt\_core\_safe\_workplace\_audience\_cached\_user table.
        -   Allow HTML encodings in the User Privacy Consent form.
        -   Improve tab navigation and fixed screen reader bug.
        -   Fixed high contrast color issue on My Safe Workplace page.
        -   Improved rendering of approve/deny buttons in the Approval Portal and fixed the JavaScript code that prevented the widget in the form editor from being saved.
        -   Rejecting a user's test result didn't set the user's Health Test Requirement to Not Cleared.
        -   Two or more Emergency Outreaches couldn't use the same User Privacy Notice and Consent record.
        -   Requirements now have a User field to specify which user should be associated with a given table. For example, the COVID-19 Vaccine Requirement uses the User field on Vaccination Profile.
        -   Approval Portal row height was misaligned due to text alignment in a button animation.
        -   Minor bugs fixed.
-   **Version 1.36.1 - March 2022**
    -   New: Localization for features from the February 17 release
    -   Fixed:
        -   Requirements using an audience with the "All the criteria \(AND\)" criteria weren’t being honored by requirement flow
        -   Improved the Approval Portal's search performance
        -   Improved the performance when creating Health and Safety Users and their associated Employee Health and Safety Requirements
        -   Requirement audiences weren't working when the audience contained multiple groups
        -   Other minor bugs
-   **Version 1.34.0 - February 2022**
    -   New:
        -   Updated the logic to arrive at Requirement Status for a Health and Safety user
        -   Added a new requirement status "Not Required"
        -   Ability to identify applicable user set for a requirement and create requirement records
        -   Updated the "recalculate audience" scheduled job to address status of "Not Required"
        -   New scheduled job to reset the requirement status to align with new logic of "Not required" status
        -   Localization for features from the January 27 release
    -   Fixed:
        -   JavaScript was not handled on SWA Approval portal when Vaccination Status or Health and Safety Testing apps were not installed
        -   Recalculate audience job flows did not run when there were no users added or deleted from an audience
        -   Employee Health and Safety Requirement records were not created for users who already submitted Health Test Results
        -   Other minor bugs
-   **Version 1.33.0 - January 2022**
    -   New:
        -   Vaccine Status Dashboard
        -   Testing Status Dashboard
        -   Localization for 22 languages other than English. Translations are available for features released up until the December 16, 2021 release.
    -   Fixed: Minor bugs
-   **Version 1.31.1 - January 2022**

    Fixed: Performance and functionality bugs

-   **Version 1.30.0 - December 2021**
    -   New:
        -   Added fields and functionality to Test Result, Vaccine and Exemption records in the approval modal
        -   Show vaccination names in list view on the approval portal
        -   Open modals on a record that does not have an image attachment
        -   Localization for features from the November 18 release
    -   Changed: Updates to the translation engine
    -   Fixed: Security and minor bug fixes
-   **Version 1.28.0 - November 2021**
    -   New: Localization for features from the November 4 release
    -   Fixed: Ability to view PDF files in modals on the Approval Portal
-   **Version 1.27.0 - November 2021**
    -   New:
        -   Manager Approval
        -   Localization for features from the October 14 release
    -   Fixed: Minor bugs
-   **Version 1.26.0 - October 2021**
    -   New:
        -   Approval Portal
        -   Localization for features from the September 16 release
    -   Fixed: Minor bugs
-   **Version 1.25.0 - September 2021**
    -   New:
        -   Country-specific vaccination responses and retention policy
        -   Vaccine exemptions added to profiles
    -   Fixed: Several minor bugs
-   **Version 1.24.0 - September 2021**

    Fixed: Minor bugs

-   **Version 1.23.0 - August 2021**

    Fixed: Minor bugs

-   **Version 1.22.0 - August 2021**

    New: Localization for features from the July 22 release

-   **Version 1.21.1 - July 2021**
    -   New: Added Employee Health and Safety Status support for travel requests and reservations
    -   Fixed: Minor bugs
-   **Version 1.20.0 - July 2021**

    Fixed: Security bugs

-   **Version 1.18.0 - June 2021**

    Fixed: Minor bug for flow changes on upgrade

-   **Version 1.17.0 - April 2021**

    New: Localization for features from the March 25 release

-   **Version 1.16.0 - March 2021**

    New: Support for syncing the WSD and WSM Visitor tables

-   **Version 1.15.1 - March 2021**
    -   New: Localization for features from the February 18 release
    -   Fixed
        -   Requirement flow in Emergency Self Report not executed for repeated states
        -   Other minor bug fixes
-   **Version 1.14.0 - February 2021**

    Fixed: For the Contact Tracing application, notes appear correctly when the case is closed or when the note is logged on the case closure date

-   **Version 1.13.0 - February 2021**
    -   New: Localization for features from the January 21 release
    -   Fixed: Security bug
-   **Version 1.12.1 - January 2021**

    New:

    -   Support for Level 2 domain separation
    -   Localization for features from the December 17 release
    -   WCAG improvements
-   **Version 1.11.1 - December 2020**
    -   New:
        -   Support for a common structure to request consent for various privacy policies
        -   Support for the new Vaccination Status application
        -   Localization for features from the December 3 release
    -   Fixed: Minor bug fixes
-   **Version 1.10.0 - December 2020**
    -   New:
        -   Ability to track and report on employee QR code scans for entry
        -   Localization for features from the November 19 release
    -   Changed: The My Day menu item and page title were renamed to My Safe Workplace
-   **Version 1.9.2 - November 2020**

    New:

    -   Use the new My Safe Workplace page to view all of your information and resources for returning to the workplace. Manage your requirement status for workplace entry, update your health status, track workspace reservations, and create requests for PPE or testing. Modules include:
        -   My status
        -   Things I can do
            -   Screen a visitor for entry
            -   Set up a visit to our company
            -   Request permission to travel
            -   Set up a COVID-19 diagnostic test
            -   Report a COVID-19 diagnostic test result
            -   Request PPE items
            -   Reserve a shift and space for a day
            -   Schedule your arrival today
        -   My open requests
        -   My workplace reservations
        -   My health status
        -   My team status
    -   Localization for features from the November 5 release
-   **Version 1.8.0 - November 2020**
    -   New:
        -   Employers can set up an employee privacy consent requirement to help facilitate contact tracing
        -   New catalog item icons
        -   Localization for features from the October 15 release
    -   Fixed: Minor bug fixes
-   **Version 1.7.0 - October 2020**
    -   New:
        -   Set future dates for visitor scheduling
        -   On the Health Verification confirmation page, new links are available for employees to easily resolve outstanding requirements
        -   Managers can view the Health and Safety status of their direct reports
        -   Localization for features from the October 1 release
    -   Changed: Updated the Uber link in ServiceNow's guided setup
    -   Fixed: Minor bug fixes
-   **Version 1.6.0 - October 2020**

    New:

    -   Users can upload a spreadsheet or CSV file to create a Safe Workplace audience
    -   Localization for features from the September 16 release
-   **Version 1.5.1 - September 2020**
    -   New: Updates to usage metering
    -   Fixed: Various priority fixes
-   **Version 1.4.0 - September 2020**

    Fixed:

    -   Security fix
    -   Activating requirements no longer trigger conflicts upon upgrade
-   **Version 1.3.0 - August 2020**

    New:

    -   Additional information on the Health and Safety Status page
    -   Support for the ServiceNow Safe Workplace Dashboard's automation of building and campus creation through guided setup
    -   Localization for features from the August 6 release
-   **Version 1.2.1 - August 2020**

    New:

    -   Added Guided Setup content for setting up the Uber for Business feature
    -   Updated Guided Setup for Contact Tracing in Employee Readiness Core
    -   Updated the Exposed Contacts Requirement \(one of the possible health and safety requirements\)
    -   Localization for features from the July 23 release
-   **Version 1.1.0 - July 2020**

    New:

    -   Generic logging API
    -   Webhook to call third-party systems for health verification
    -   Localization for features from the July 9 release
    -   Compatible with ServiceNow instances on the Paris release
-   **Version 1.0.6 - July 2020**
    -   New:
        -   Manage visitor requirements
        -   Localization for features from the June 18 release
    -   Changed: 'View employee status' was updated to 'View employee and visitor status'
-   **Version 1.0.5 - June 2020**

    New: Support for Employee Health Screening and Emergency Self Report

-   **Version 1.0.4 - June 2020**

    Fixed: In Orlando Patch 3 and later instances, reference fields are now rendered at the correct width

-   **Version 1.0.3 - May 2020**

    The Employee Readiness Core plugin provides shared functionality and data structures for Employee Readiness apps, such as Employee Readiness Surveys and Employee Health Screening.


## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)


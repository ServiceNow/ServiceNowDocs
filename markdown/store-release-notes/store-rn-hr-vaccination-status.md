---
title: Vaccination Status release notes
description: Version history for the Safe Workplace Vaccination Status on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-vaccination-status.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Vaccination Status release notes

Version history for the Safe Workplace Vaccination Status on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

**Note:** To automatically install all the Safe Workplace applications at once, download the ServiceNow® Safe Workplace suite application.

## Version history

-   **Version 1.25.1 - June 2026**

    Fixed: Remediated non-Glide ACLs

-   **Version 1.25.0 - December 2025**

    Fixed: Updated Readonly fields to use new platform security features.

-   **Version 1.24.0 - August 2025**

    Changed: Minor ACL updates

-   **Version 1.23.4 - May 2024**

    Security fixes.

-   **Version 1.23.2 - January 2024**

    Security fixes.

-   **Version 1.23.1 - November 2022**

    Fixed:

    -   Improvement in Next Experience theming alignment
    -   One minor bug related to restricted caller access \(RCA\)
-   **Version 1.23.0 - August 2022**
    -   Changed: Security-related updates.
    -   Fixed:
        -   Security bug.
        -   Added a new attribute 'vaccine reviewed on' to show the vaccine review information in users' timezone.
        -   Performance and quality improvements.
-   **Version 1.22.0 - May 2022**
    -   New: Localization for features in the May 5 release.
    -   Changed:
        -   Streamline submission of vaccination responses.
        -   Added health\_and\_safety\_approver role for Approval Portal.
    -   Fixed:
        -   Added report\_view ACL to sn\_imt\_vaccine\_attachment\_validation.
        -   Vaccination doses can now be reported in any order.
        -   sys\_domain fields added to sn\_imt\_vaccine\_vaccine\_code and sn\_imt\_vaccine\_vaccine\_code\_system tables.
        -   Vaccine booster reminders were not sent at their specified frequency.
        -   Added new Consider review outcome for setting the covid19\_vaccine\_completed field system property. This property will override the 'Reset Covid 19 Vaccine Complete to false if Vaccine Review Outcome is Rejected' and enforce vaccine response approval when calculating a user's 'Covid-19 vaccine completed' status.
        -   Booster shots required a 14 day wait time similar to other vaccine doses.
        -   Users without the sn\_imt\_core.privacy\_consent\_user role could submit responses with the Report Vaccination record producer.
-   **Version 1.21.0 - March 2022**
    -   New:
        -   Localization for features from the February 17 release
        -   Ability to enter vaccine booster information in a more flexible way
        -   Ability to enter vaccine and booster information at the same time
    -   Fixed:
        -   "Covid-19 vaccine completed" was getting checked when booster due date passed, but the employee hadn't responded with a booster dose
        -   Azure Form Recognizer integration threw errors and does not complete validation flow in Rome or Quebec
        -   The "Set covid19\_vaccine\_completed" business rule was crashing when employee only had booster dose vaccine responses
        -   Duplicate activity log entries were created when a vaccine response's Vaccine Review Outcome was changed
-   **Version 1.20.0 - February 2022**
    -   New:
        -   Azure Form Recognizer: Service interaction
        -   Admin set-up: Ability to copy the training model to the customer subscription
    -   Fixed: Minor bug
-   **Version 1.19.1 - January 2022**
    -   New:
        -   Deletion of decoded QR data per the specified data retention period
        -   Localization for 22 languages other than English. Translations are available for features released up until the December 16, 2021 release.
    -   Fixed: Minor bug
-   **Version 1.18.0 - January 2022**

    Fixed: Minor bug fixes

-   **Version 1.17.1 - December 2021**
    -   New:
        -   Automated validation of submitted vaccine responses \(integration with The Commons Project - SMART Health Card QR Code: Service Interaction\)
        -   Ability to have two different manufacturers when submitting two vaccine doses
    -   Changed: Updates to the translation engine
-   **Version 1.16.0 - November 2021**
    -   New: Localization for features from the November 4 release
    -   Fixed: Ability to view PDF files in modals on the Approval Portal
-   **Version 1.15.0 - November 2021**
    -   New:
        -   Manager Approvals
        -   Activity log on the changes to a vaccination responses
        -   Ability to append approver notes to vaccine responses
        -   Localization for features from the October 14 release
    -   Fixed: Minor bugs
-   **Version 1.14.0 - October 2021**
    -   New:
        -   Approval Portal
        -   Exemption request support for mobile
        -   Localization for features from the September 16 release
    -   Fixed: Minor bugs
-   **Version 1.13.0 - September 2021**
    -   New:
        -   Support for vaccine exemptions
        -   Ability to deny proof of vaccine
        -   New 'My Vaccinations' menu item
        -   Localization for features from the September 2 release
    -   Fixed: Minor bugs related to vaccine response, exemption, and booster shots
-   **Version 1.12.0 - September 2021**
    -   New:
        -   Localization for features from the August 19 release
        -   Additional fields added to Vaccination Profiles and Dose Records
    -   Fixed: Minor bug
-   **Version 1.11.0 - August 2021**
    -   New:
        -   Support for booster vaccination doses
        -   Localization for features from the August 5 release
    -   Fixed: Minor bug
-   **Version 1.10.1 - August 2021**
    -   New: Localization for features from the July 22 release
    -   Fixed: Minor bugs
-   **Version 1.9.0 - July 2021**
    -   New:
        -   Improved reporting capabilities
        -   Updated the threshold for full vaccination to be 14 days after the final dose
        -   Localization for features from the July 1 release
    -   Fixed: Minor bugs
-   **Version 1.8.0 - July 2021**
    -   Changed: Updates to the translation engine
    -   Fixed: Minor bugs
-   **Version 1.7.0 - June 2021**

    Fixed: Data retention bug

-   **Version 1.6.0 - April 2021**

    New: Localization for features from the April 15 release

-   **Version 1.5.0 - April 2021**
    -   New:
        -   Populate vaccination data for use in the Safe Workplace Dashboard
        -   Localization for features from the March 25 release
    -   Fixed: Minor bug
-   **Version 1.4.0 - March 2021**
    -   New: A new role was added to view Vaccination Status Profile records to support Vaccination Status data in the Contact Tracing application
    -   Fixed: Scheduled job for data retention
-   **Version 1.3.2 - February 2021**

    New:

    -   Ability to provide second dose reminders \('Due' and 'Past Due'\)
    -   Localization for features from the February 4 release
-   **Version 1.2.0 - February 2021**

    New: Ability to request an employee's submission of vaccination status via SMS

-   **Version 1.1.0 - January 2021**

    New: Localization for features from the December 17 release

-   **Version 1.0.0 - December 2020**

    The ServiceNow® Vaccination Status application gives HR departments the ability to track the status of employee vaccinations in the workplace. Organizations can collect vaccination data for workforce planning, as needed based on business requirements, and report on the readiness of the workplace. Employees are empowered to submit documentation of completed vaccinations to meet their employer’s health and safety requirement for a safe return to the workplace, while administrators can track the status of employee vaccination in the workplace. Status updates can be made manually by the employee.


## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.


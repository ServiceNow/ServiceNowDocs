---
title: Emergency Self Report release notes
description: Version history for the Emergency Self Report on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-bcm-emerg-self-report.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Emergency Self Report release notes

Version history for the Emergency Self Report on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.21.2 - June 2026**

    Fixed: Remediated non-Glide ACLs

-   **Version 1.21.0 - August 2025**

    Changed: Minor ACL updates

-   **Version 1.20.5 - May 2024**

    Security fixes.

-   **Version 1.20.4 - January 2024**

    Security fixes.

-   **Version 1.20.3 - November 2022**

    Fixed: Accessibility improvements

-   **Version 1.20.1 - August 2022**
    -   Fixed:
        -   Introduced a security restriction to ensure managers cannot submit health status for any user other than direct reports.
        -   Restricted addition of an emergency self report when no user is populated in the user field and an error message is shown.
        -   Quality improvement
-   **Version 1.19.0 - January 2022**

    New: Localization for 22 languages other than English. Translations are available for features released up until the December 16, 2021 release.

-   **Version 1.18.1 - December 2021**

    Changed: Updates to the translation engine

-   **Version 1.17.0 - August 2021**

    Fixed: Minor bug

-   **Version 1.16.0 - July 2021**

    New: Localization for features from the July 1 release

-   **Version 1.15.0 - July 2021**
    -   Changed: Updates to the translation engine
    -   Fixed: Minor bugs
-   **Version 1.14.0 - April 2021**

    Fixed: Minor bug

-   **Version 1.13.0 - April 2021**
    -   New: Localization for features from the March 25 release
    -   Fixed: Minor bug
-   **Version 1.12.0 - March 2021**

    Fixed: Users now have appropriate read/write access to Crisis Task worknotes

-   **Version 1.11.1 - March 2021**

    New: Localization for features from the February 18 release

-   **Version 1.10.0 - February 2021**

    Fixed: Security fix

-   **Version 1.9.0 - February 2021**
    -   New: Localization for features from the January 21 release
    -   Fixed: Minor bug fixes
-   **Version 1.8.0 - January 2021**
    -   New:
        -   Crisis task admins can now create crisis tasks in bulk, by uploading a CSV or XLS/X file containing users
        -   Added ability to use alternate table criteria to define a Safe Workplace audience
        -   WCAG improvements
-   **Version 1.7.0 - December 2020**
    -   New: Localization for features from the December 3 release
    -   Fixed: Minor bug fixes
-   **Version 1.6.1 - December 2020**

    New: Historical data is available for self-reported health status data

-   **Version 1.5.0 - November 2020**
    -   New:
        -   In the new My Safe Workplace page, there is a new 'Update your health status' option in the 'Things you can request' module
        -   Localization for features from the November 5 release
-   **Version 1.4.0 - November 2020**
    -   New: Localization for features from the October 15 release
    -   Fixed: Customers can use new system properties to control the behavior of the system when a user updates their health status to something that should re-open the task
-   **Version 1.3.0 - October 2020**

    New: Localization for features from the October 1 release

-   **Version 1.2.0 - October 2020**

    Fixed: The Knowledge Base category has been modified so that only crisis task user roles can read

-   **Version 1.1.0 - July 2020**

    New: Compatible with ServiceNow instances on the Paris release

-   **Version 1.0.12 - June 2020**
    -   New: Updated localization for:
        -   Japanese
        -   French
        -   German
        -   Spanish
        -   Italian
        -   Brazilian Portuguese
        -   Korean
        -   Simplified Chinese
-   **Version 1.0.11 - May 2020**
    -   New: The Crisis Task form has a new related list to display tasks that are assigned to the user.
    -   Fixed: The Emergency Self Report dashboard now updates user statuses correctly if a new task is created for a user who had an inactive task.
-   **Version 1.0.9 - April 2020**
    -   Fixed:
        -   After activating the 1.0.4 version of the Emergency Self Report Store application, related lists \(that appear as tabs\) are no longer missing in Agent Workspace
        -   The 'Update health' widget status no longer returns a message with a non-translatable field type
        -   Fixed various hard-coded and concatenated strings in the Self Report widget and Overview dashboard
-   **Version 1.0.8 - April 2020**
    -   New: The Emergency Self Report UI is now available in the following languages.
        -   Brazil/Portuguese
        -   French
        -   German
        -   Italian
        -   Japanese
        -   Korean
        -   Simplified Chinese
        -   Spanish
    -   Fixed:
        -   Performance improvements were made to reduce the load time of records in list view.
        -   The empty Health Alert List widget was removed.
-   **Version 1.0.4 - April 2020**
    -   New:
        -   A new Service Portal dashboard allows the global task force or HR team to monitor the situation
        -   Users with the HR emergency response role can submit tasks for any employee in the company
        -   Users can now view self-reported HR tasks
        -   A new module \(**Emergency Self Response** &gt; **HR tasks**\) allows the HR emergency response team to open a list of all HR tasks.
        -   General performance improvements
    -   Fixed:
        -   Users with the sn\_imt\_quarantine.crisis\_task\_user role can now submit their health status as expected
        -   A record is created properly if a user selects ‘Reporting to Work’ or ‘Decline to Say’
        -   Minor bug fixes
-   **Version 1.0.3 - March 2020**

    During a crisis, the ServiceNow Emergency Self Report application enables employees to notify their employer of their health status. An application helps the employee safely return to work. It is part of a group of apps built on the ServiceNow AI Platform® to assist companies in their emergency response efforts.


## Notice regarding use by employers

All decisions in connection with the implementation of this application are at the sole decision of the Employer utilizing this application. Employers agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Employers remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Employers’ specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to employees of government agencies in their individual capacities. Use of this application is being offered free of charge for a limited or extended time period and with no expectation of payment from the government agency to ServiceNow for use during that time period, nor does usage create an actual or implied future obligation on behalf of the government. ServiceNow hereby expressly waives any future claims for payment from the agency in connection with usage of the application. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)


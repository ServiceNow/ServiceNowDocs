---
title: Emergency Outreach release notes
description: Version history for the Emergency Outreach on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-bcm-emerg-outreach.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Emergency Outreach release notes

Version history for the Emergency Outreach on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.34.2 - June 2026**

    Fixed: Remediated non-Glide ACLs

-   **Version 1.34.0 - August 2025**

    Changed: Minor ACL updates

-   **Version 1.33.0 - February 2024**

    Removed: The Emergency Outreach dashboard has been deprecated. Customers who have downloaded the 1.32.0 or any older version will continue to have the dashboard and can continue to use it. Customers who have downloaded the 1.32.1 or newer version of the app will NOT have the dashboard.

-   **Version 1.32.1 - January 2024**

    Security fixes.

-   **Version 1.32.0 - November 2022**

    Fixed:

    -   Added an information message to highlight when the emergency outreach does not have audience selected
    -   Quality improvements
-   **Version 1.31.1 - August 2022**
    -   Changed:
        -   Removed dependency from sn\_imt\_core's ArrayUtil; customers can now use emergency ourtrach application without employee readiness core.
        -   Changed message banner from information to error message when blocking a record creation.
    -   Fixed:
        -   Added a new reference attribute "Emergency Outreach" where customers can optionally set the column to explicitly make clear which outreach should be updated when an SMS response is made to ensure the correct acknowledgement record can be updated when there are multiple outreaches for a particular user.
        -   Fixed notifications to ensure any new users that are added or that qualify after the first sent outreach receive notifications.
        -   Fixed translation related issue to ensure the error messages are translated.
        -   Quality improvements
-   **Version 1.30.0 - May 2022**
    -   New: Localization for features in the May 5 release
    -   Fixed: Outreaches are sent at an incorrect time when the user that schedules them has a time zone different than the system time zone
-   **Version 1.29.0 - March 2022**

    Fixed: General performance improvements, particularly with dispatching large amounts of notifications

-   **Version 1.28.0 - February 2022**

    Fixed: Added read role to the sn\_imt\_checkin.notification\_logging property

-   **Version 1.27.0 - January 2022**

    New: Localization for 22 languages other than English. Translations are available for features released up until the December 16, 2021 release.

-   **Version 1.26.0 - January 2022**

    Fixed: Mobile push notifications for outreach acknowledgements

-   **Version 1.25.1 - December 2021**

    Changed: Updates to the translation engine

-   **Version 1.23.0 - September 2021**

    Fixed: Minor bug

-   **Version 1.22.0 - August 2021**

    Fixed: Minor bug

-   **Version 1.21.0 - August 2021**

    New: Localization for features from the July 22 release

-   **Version 1.20.0 - July 2021**

    Fixed: Outreach scheduling bug

-   **Version 1.19.0 - July 2021**

    Fixed: Security bug

-   **Version 1.18.0 - June 2021**

    Fixed: Notification bugs

-   **Version 1.17.0 - April 2021**
    -   New: Localization for features from the April 15 release
    -   Fixed: Minor bug related to timing of scheduled notifications and the Health Verification log
-   **Version 1.16.0 - April 2021**

    Fixed: Issue where the exposed contact notification failed to send from a Contact Tracing case

-   **Version 1.15.2 - March 2021**
    -   New: Localization for features from the February 18 release
    -   Fixed:
        -   Outreach recipient receives multiple notifications if they are removed from the audience and then readded
        -   Changing the response mode on new outreach produces script error
        -   Other minor bug fixes
-   **Version 1.14.0 - February 2021**
    -   New:
        -   Support for SMS Exposure Surveys
        -   Localization for features from the February 4 release
    -   Fixed: Security fix
-   **Version 1.13.1 - February 2021**

    Fixed:

    -   Daylight Savings Time scheduling issues
    -   Other minor bug fixes
-   **Version 1.12.0 - January 2021**

    New:

    -   Added ability to use alternate table criteria to define a Safe Workplace audience
    -   Localization for features from the December 17 release
-   **Version 1.11.0 - December 2020**
    -   New:
        -   New common structure for employers to request consent to various privacy policies
        -   Changes to update users on the status of Emergency Outreach instance generation
        -   Localization for features from the December 3 release
    -   Fixed: Minor bug fixes
-   **Version 1.10.1 - December 2020**

    New:

    -   Easily configure SMS as an outreach channel
    -   Localization for features from the November 19 release
-   **Version 1.9.0 - November 2020**
    -   New: Localization for features from the November 5 release
    -   Fixed: Issue with user timezones when sending an Outreach
-   **Version 1.8.0 - November 2020**
    -   New: Localization for features from the October 15 release
    -   Fixed:
        -   Localization fixes to email templates and response options
        -   Outreaches no longer display a premature confirmation message
        -   Other minor bug fixes
-   **Version 1.7.2 - October 2020**
    -   New: Localization for features from the October 1 release
    -   Fixed:
        -   Scheduled outreach recipients no longer receive notifications after they are removed from the Safe Workplace audience
        -   Minor bug fixes
-   **Version 1.6.0 - October 2020**
    -   New: Localization for features from the September 16 release
    -   Fixed:
        -   Scheduled outreaches are now triggered in local time
        -   The Employee Workplace Readiness Survey assessable record is no longer missing a category
-   **Version 1.5.0 - September 2020**
    -   New:
        -   Exclude specific days of week on Daily Outreach
        -   Localization for the September 3 release features
    -   Fixed: Widget name spelled incorrectly in Emergency Outreach Dashboard
-   **Version 1.4.1 - September 2020**
    -   New:
        -   Created an Outreach notification for exposed contacts in the Contract Tracing application
        -   Added additional security for Outreach readiness surveys
        -   Localization for features from the August 20 release
    -   Fixed: Mobile Exposure Notices are no longer blank
-   **Version 1.3.0 - August 2020**

    New:

    -   Ability to schedule a single Outreach for a specific time
    -   Added survey due dates
    -   New Daily Health Verification feature
    -   Ability to schedule monthly Outreaches
    -   Localization for features from the August 6 release
-   **Version 1.2.1 - August 2020**

    New:

    -   Readiness flows, including out-of-box examples
    -   Ability to relate survey instances to specific Outreaches
    -   Create new survey instances and cancel old ones on new Outreaches
    -   Design changes for Contact Tracing privacy consent
    -   Localization for features from the July 23 release
-   **Version 1.1.2 - July 2020**

    New:

    -   Add User Collection Option \('Audience'\) to Outreach notifications
    -   Scheduled outreach with timezone support
    -   Localization for features from the July 9 release
    -   Compatible with ServiceNow instances on the Paris release
-   **Version 1.0.12 - July 2020**

    New: Localization for features from the June 18 release

-   **Version 1.0.11 - June 2020**
    -   New:
        -   Localization for Emergency Outreach v1.0.9
        -   Support for Outreach scheduling
    -   Fixed:
        -   Survey instances related list
        -   When assigning outreaches to departments/groups/locations, child groups, locations, etc. were being used but not the parent
        -   There is now only one **Save** button in the Outreach form when a user is in the advanced UI form
-   **Version 1.0.9 - June 2020**
    -   New:
        -   Updated localization for:
            -   Japanese
            -   French
            -   German
            -   Spanish
            -   Italian
            -   Brazilian Portuguese
            -   Korean
            -   Simplified Chinese
        -   Added the ability to schedule Emergency Outreach communications
    -   Fixed: ACL issues
-   **Version 1.0.8 - May 2020**
    -   New: Admins can configure scripted notification channels to send surveys to users on other platforms, such as Slack.
    -   Fixed: The **Response Value** field is now visible in list view.
-   **Version 1.0.7 - April 2020**

    New

    -   Editable Templates for Alternate Questions and Content – Enables users to more easily locate and edit the Outreach email notification template, and enables support for additional email notification templates for other types of Outreach communications.
    -   Dynamic Response Handling – Eliminates the need to hardcode response options and create additional custom Inbound Actions. Users can now create the response options in a table, where they can be used by one or multiple notification templates.
-   **Version 1.0.6 - April 2020**

    New: The Emergency Outreach UI is now available in the following languages.

    -   Brazil/Portuguese
    -   French
    -   German
    -   Italian
    -   Japanese
    -   Korean
    -   Simplified Chinese
    -   Spanish
-   **Version 1.0.4 - April 2020**
    -   New
        -   Added domain separation support
        -   General improvements and changes
    -   Fixed
        -   Minor UI improvements and adjustments, including some label changes
        -   On the Outreach Acknowledgements table, a **New** button now appears as expected
-   **Version 1.0.3 - March 2020**

    Enables employers to quickly notify employees of important information in the event of an emergency, such as COVID-19. Also provides a simple response interface for employees to self-report their health status to ensure employee safety and anticipate staffing gaps. Graphical dashboards make it easy for employers to monitor status.


## Notice regarding use by employers

All decisions in connection with the implementation of this application are at the sole decision of the Employer utilizing this application. Employers agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Employers remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Employers’ specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to employees of government agencies in their individual capacities. Use of this application is being offered free of charge for a limited or extended time period and with no expectation of payment from the government agency to ServiceNow for use during that time period, nor does usage create an actual or implied future obligation on behalf of the government. ServiceNow hereby expressly waives any future claims for payment from the agency in connection with usage of the application. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.


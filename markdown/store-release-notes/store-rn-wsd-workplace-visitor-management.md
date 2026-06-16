---
title: Workplace Visitor Management release notes
description: Version history for the Workplace Service Delivery Workplace Visitor Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-visitor-management.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Visitor Management release notes

Version history for the Workplace Service Delivery Workplace Visitor Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.9 - June 2026**
    -   Fixed:
        -   All-day visitor registration schedule collapses to 1-hour window when location is changed to a different timezone
        -   The "View invite details" button was displayed in the host check-in email
        -   Fixed translation issues
        -   Fixed issues introduced by plugin upgrades
    -   Removed: Removed duplicate Host and Receptionist page records.
-   **Version 1.19.19 - June 2026**

    Fixed: Added phone number validation during kiosk self-registration.

-   **Version 2.0.1 - May 2026**
    -   Fixed:
        -   Fixed an issue related to Visitor Portal access.
        -   Added required dependencies to enable OTP access.
-   **Version 2.0.0 - April 2026**
    -   This release introduces breaking changes. Please review the impact on your current configuration and user experience before upgrading.
        -   New:
            -   Added a Receptionist page to manage the full visitor flow from a single place.
            -   Introduced a Host page for employees to view, update, or cancel visits.
            -   Launched a secure Visitor portal to complete pre-visit steps and access visit details.
            -   Enabled dynamic, condition-based visitor check-in flows.
            -   Introduced the Workplace Concierge AI agent to automate visit creation and management from email, calendar invites, and Now Assist.
        -   Changed:
            -   Migrated the product to use Workplace locations instead of CMN locations.
            -   Replaced the record producer in the 'Register a guest' page with the new requirements configuration.
            -   Centralized the check-in configuration flow into the Visit Requirements model, enabling dynamic, condition-based configurations.
            -   Replaced the record producer in the kiosk self-registration with the new requirements configuration.
            -   Updated kiosk self-registration to display forms instead of one question per page.
        -   Fixed:
            -   Removed an issue affecting the phone number self check-in option.
            -   Enabled support for phone numbers formatted with dashes during kiosk check-in and check-out.
            -   Fixed an issue where visitor QR codes did not display correctly on Windows devices.
            -   Resolved several badge printing issues.
-   **Version 1.19.15 - April 2026**
    -   Fixed:
        -   Removed an issue affecting the phone number self check-in option.
        -   Enabled support for phone numbers formatted with dashes during kiosk check-in and check-out.
        -   Fixed an issue where visitor QR codes did not display correctly on Windows devices.
        -   Resolved several badge printing issues.
-   **Version 1.19.10 - February 2026**

    Fixed: Prevent duplicate invitation emails from being sent after an upgrade.

-   **Version 1.19.0 - December 2025**
    -   New:
        -   Added support to bulk upload visitors when creating a visit.
        -   Added support for recurring and multi-day visits.
        -   Added the ability for receptionists to capture visitor photos.
        -   Added an order field to control the sequence of check-in and check-out options on the kiosk.
        -   Introduced new invitation table to support multi-day and recurring visit logic.
    -   Changed:
        -   Updated email notification logic to support multi-day and recurring visit patterns.
        -   Merged the invitation and policy emails into a single notification.
    -   Important: All email notification customizations need to be updated.
    -   Fixed:
        -   Fixed an issue where selecting a prior visitor did not retain their VIP status.
        -   Fixed timezone-related issues.
        -   Fixed an issue that caused future visits to be anonymized.
-   **Version 1.18.3 - September 2025**
    -   Fixed:
        -   Timezone related issues.
        -   Issue where certain email formats prevented guest check-in using email on kiosk.
-   **Version 1.18.1 - August 2025**
    -   New:
        -   Added ability to capture signatures directly from policy approval emails.
        -   Enabled collection and storage of visitor consent when capturing photos during check-in.
        -   'All Day' registration values for visitor check-in are now configurable.
-   **Version 1.17.0 - May 2025**
    -   New:
        -   Ability to check in using QR codes \(on kiosk\)
        -   QR code included in the visitor invitation email
        -   Option to capture visitor photos \(on kiosk\)
        -   Support for signing signature policies \(on kiosk\)
        -   New configurable badge templates for printing
    -   Fixed: When uploading visitors via csv import, the passcode now appears in the invitation email.
-   **Version 1.16.1 - February 2025**
    -   Fixed:
        -   The Visitor Staff role now has read-only access to dashboards.
        -   The Co-host field is now populated when visitor registration is done through Virtual Agent.
-   **Version 1.16.0 - November 2024**

    Fixed translation issues.

-   **Version 1.15.2 - August 2024**
    -   New:
        -   Self registration, self check-in and check-out by guests through the new Visitor Kiosk experience.
        -   Ability to notify hosts of guests arrival through Virtual Agent.
    -   Fixed:
        -   Registering a visitor using Virtual Agent resulted in an error. This has been fixed.
        -   The confirmation page was not showed when registering a new guest. This has been fixed.
        -   The title field in the policy definitions did not support translation. This has been fixed.
        -   Security fixes
-   **Version 1.14.0 - May 2024**

    Fixed: Visitor registrations created for certain locations in Latin America were off due to incorrectly applying daylight saving time. This has been fixed now.

-   **Version 1.13.0 - February 2024**
    -   Changed: The Visitor Reception Dashboard can now be accessed from the Workplace Central workspace. Customers who have installed 1.11.0 or earlier versions of the app can still access the old version of the dashboard. Customers installing the app for the first time from 1.13.0 version onwards can access the dashboard in Workplace Central only.
    -   Fixed:
        -   When printing badge labels an additional blank screen is printed
        -   Security fixes
-   **Version 1.11.0 - November 2023**

    Changed: The Visitor Reception Dashboard can now be accessed from the Workplace Central. Download the Workplace Central plugin and open the Workplace Dashboards tab to view the dashboard.

-   **Version 1.10.0 - August 2023**

    New: Introduce additional archiving configuration.

-   **Version 1.9.1 - February 2023**

    Changed: The default email templates have been updated to match the next experience content and style guidelines. The new templates will be installed along with the old ones in case the old ones already exist on the instance.

-   **Version 1.8.7 - November 2022**
    -   Fixed:
        -   Earlier, whenever the arrival time was set to 11:01 pm, the end date was set to the next day. This has been fixed now.
        -   Earlier, it was not possible to add additional roles to the Visitor reception module available in the platform view. This has been fixed now.
-   **Version 1.8.6 - August 2022**
    -   Changed: Added 'Title' field to the 'Register a guest' record producer to support translations accordingly.
    -   Fixed
        -   Earlier, the default notification value while registering a visitor was false. This has been fixed now.
        -   Earlier, the visitor policy acceptance was not updating the related policy confirmation record. This has been fixed now
-   **Version 1.8.4 - July 2022**

    Fixed: All visitor registrations were updated whenever an employee updated a reservation that contained visitors.

-   **Version 1.8.2 - May 2022**

    New: Register guests and invite them while making a reservation. The visitor registrations will be related to the reservation. If the visitor is revisiting, their details are displayed in the list of known visitors.

-   **Version 1.7.4 - February 2022**
    -   Fixed
        -   Correct notifications are sent to employees regarding visitor policies while registering visitors.
        -   The response from a visitor regarding accepting or rejecting mandatory visitor policy is now updated correctly in case of a reply.
-   **Version 1.7.2 - December 2021**
    -   Fixed
        -   It was not possible to cancel a visitor registration on NowMobile.
        -   Visitor records were not deleted from the audit table when the data got anonymized.
-   **Version 1.6.8 - October 2021**
    -   New: Additional support has been added to support all the 22 languages that are currently available across the ServiceNow AI Platform.
    -   Fixed
        -   The visitor registrations were not visible in the My Request section in the Now Mobile.
        -   The **Cancel** button on the summary page was not displayed correctly.
-   **Version 1.6.5 - September 2021**
    -   Fixed
        -   Earlier, submitting a visitor registration on Now Mobile did not display the details.
        -   Earlier, when creating a new visitor registration and selecting 'all day' resulted in an error.
        -   Earlier, visitor policy notifications were not displayed when required while registering a new visitor.
-   **Version 1.6.1 - June 2021**
    -   Fixed
        -   Earlier, the name of the host was not printed on the badge. This has been fixed now.
        -   Earlier, the host was notified correctly when a visitor did not reply to the policy notification. This has been fixed now.
-   **Version 1.5.1 - May 2021**
    -   New: Synchronize registered visitors between Workplace Visitor Management and Safe Workplace application's Employee Health and Safety Status. The synchronization is bi-directional between both applications.
    -   Fixed:
        -   Earlier, visitor details were duplicated when registering multiple visitors in a single registration. This has been fixed now.
        -   Earlier, the Visitor details option was not displayed after an upgrade from Orlando to Quebec. This has been fixed now.
        -   The accessibility has been improved when opening an existing visitor registration.
-   **Version 1.4.1 - March 2021**
    -   Changed
        -   The state of the current day's \(today\) visitor registrations is automatically updated end of the day.
        -   Visitor registrations will now open in the ticket page when you search using the Virtual Agent chat option.
-   **Version 1.3.1 - January 2021**
    -   New:
        -   Define and assign policies on workplace locations. The policy will be sent to the visitor to accept/reject before arriving at the workplace location.
        -   Notify visitors via an email message to accept or reject the policies.
        -   Reception or security staff can view if a visitor has accepted the policy before visiting the location.
-   **Version 1.2.2 - December 2020**
    -   New: You can now search for visitors from your submitted requests. This feature is available from Paris and onwards.
    -   Fixed: Earlier, visitor registrations could not be created when the time was set to 12-hour time format. This has been fixed now.
-   **Version 1.1.2 - November 2020**
    -   New:
        -   Virtual agent chat support to register a visitor, know your registered visitor's details, and cancel a visitor registration.
        -   Anonymize a visitor and delete their data.
    -   Changed:
        -   From Workplace Safety Management \(sn\_wsd\_core\) version 2.1, all updates, and new features are available only on the Workplace Service Portal. The workplace services provided by ServiceNow® are removed from the Service Portal from Workplace Safety Management \(sn\_wsd\_core\) version 2.1.
        -   The Visitor Reception Dashboard is now accessible only from the Workplace Safety Management application.
        -   The mobile web interface has been improved in the Now Mobile app.
        -   The Workplace Services Catalog can also be accessed from the Now Mobile app homepage.
-   **Version 1.0.6 - October 2020**
    -   The new Workplace Visitor Management application enables employees to easily register guests arriving at the workplace. The workplace teams and receptionists can easily check in visitors to provide them a seamless experience. The application allows you to monitor a visitor's status at any point.

## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)


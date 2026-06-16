---
title: Mobile Publishing release notes
description: Version history for the Mobile Publishing on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-mobile-publishing.html
release: store
topic_type: reference
last_updated: "2025-12-04"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Mobile release notes, ServiceNow Store release notes]
---

# Mobile Publishing release notes

Version history for the Mobile Publishing on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 24.0.0 - December 2025**
    -   New:
        -   Publishing Guide with contextual, OS-specific setup steps for deep links, push notifications, app store listings, MAM, and more.
        -   Mobile\_admin role can now access Mobile Publishing.
        -   Background Location Tracking toggle in the UI to assist with Apple/Google review requirements.
        -   Specify custom package names / bundle IDs for public app distribution apps.
        -   See what native client version you will receive before submitting a request.
        -   “Update Available” banner for new versions of Mobile Publishing.
        -   Login modal on session timeout to prevent data loss.
-   **Version 23.2.0 - November 2024**
    -   New: Android Deep Link Enablement for Multiple Instances.
    -   Fixed: Branding asset input now supports validation for transparent images.
-   **Version 23.1.0 - May 2024**
    -   New:
        -   Pre-populate the instance URL for each branded app, so that users no longer need to enter instance details during login.
        -   Update for iOS Intune applications for ServiceNow mobile app versions 17.5 and later.Microsoft now requires additional registration and consent from Microsoft Entra ID administrators. To help with these procedures, additional messaging is included in the ServiceNow AI Platform detailing the new process.
    -   Changed:
        -   iOS Bundle IDs and Android Package IDs are now listed in the request form.
        -   The mobile application management \(MAM\) section has moved from the App basic info page \(on the first page of the form\) to the App details page \(on the second page of the form\).
-   **Version 23.0.0 - February 2024**
    -   New:
        -   New look and feel with more information such as FAQs embedded into the UI
        -   For customers on Washington family version:
            -   Use Mobile Publishing on sub-production instances
            -   Build custom app types in early availability; reach out to your ServiceNow representative for conditional approval
-   **Version 3.3.1 - November 2023**

    Fixed: Security patch to address a vulnerable third party library.

-   **Version 3.3.0 - May 2023**

    Fixed:

    -   Updating an existing app now pulls theme colors defined on the instance
    -   Universal linking file was not able to be downloaded
    -   New lines characters and carriage returns are now prevented in app name
-   **Version 3.2.0 - February 2023**
    -   New:
        -   Added support for configuring themes in Mobile Publishing builds. These themes use a new table that was introduced in Utah with the Next Experience.
        -   Removed the capability to build Mobile Onboarding apps from the Mobile Publishing form. ServiceNow has deprecated the Mobile Onboarding app and will remove it from app stores in March 2023.
-   **Version 3.1.1 - September 2022**
    -   Changed:
        -   Module name changed from "Request Branded App" to "Manage Mobile Publishing Apps"
        -   Changed Mobile Publishing landing page wording to reflect new product name "Publishing" instead of "Branding"
        -   Documentation links to point to Tokyo family release
    -   Fixed:
        -   Artifact download timeouts
        -   Translations
        -   Performance Improvements
        -   Approve/Cancel buttons disabled when not a valid step
        -   Universal links file appears once build is complete, not before
        -   Allowing unique file names upon download
        -   Show file download in progress
        -   Stop form resetting after selecting distribution type
-   **Version 3.1.0 - November 2021**
    -   New:
        -   Ability to create branded Android applications that allows public distribution via the Google Play Console.
        -   Ability to request updates to existing branded applications without needing to fill out the branding request form again.
        -   Added downloading progress bar, for build or push certificate file downloads.
    -   Changed:
        -   The mobile app version is visible for each build request.
        -   Added support for special characters and unicode to be included in app name.
    -   Removed: "Android Legacy Launcher Icon" input for Android builds, are no longer supported for Android 7.
-   **Version 3.0.0 - October 2021**
    -   New:
        -   Ability to create branded iOS applications that will allow public distribution via the Apple App Store Connect portal.
        -   Minor UI improvement to organize the display of current and previous app branding requests.
-   **Version 2.3.1 - September 2021**

    Fixed: Issue that caused Android apps to crash when special characters were included in the Firebase API Key

-   **Version 2.3.0 - August 2021**

    Fixed: Minor fixes

-   **Version 2.0.17 - January 2021**
    -   Fixed:
        -   Properly populate universal links host and write client theme values to table
        -   Persist DEP ID and Org Name, zero out platform after submission
        -   Set the app table's report view ACL to True
-   **Version 2.0.16 - November 2020**

    Removed: Removed the description field from the Request custom branding form.

-   **Version 2.0.15 - October 2020**

    Changed: Updated user-facing text for more clarity and added the ability for customer admins of New York instances to add analytics to their requests

-   **Version 2.0.14 - September 2020**

    New: Added support for iOS Universal Links - Users can connect to content deep inside the custom branded mobile apps with universal links.

-   **Version 2.0.12 - August 2020**

    New: Added support for iOS Universal Links - Users can connect to content deep inside the custom branded mobile apps with universal links.

-   **Version 2.0.10 - July 2020**
    -   New:
        -   With Mobile Publishing you can order a secure, branded version of any ServiceNow mobile app through your instance. With branding, you can make the following customizations to your mobile apps:
            -   App icon
            -   App name
            -   App description
            -   App splash screen
            -   In app theme colors
            -   Add MAM \(Mobile App Management\) support


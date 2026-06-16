---
title: Notify Zoom Connector release notes
description: Version history for the ITSM Notify Zoom Connector on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-notify-zoom.html
release: store
topic_type: reference
last_updated: "2026-01-20"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Notify Zoom Connector release notes

Version history for the ITSM Notify Zoom Connector on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.9.1 - January 2026**

    New: Added support to capture the meeting transcript and summary provided by Zoom in ServiceNow.

-   **Version 1.9.0 - August 2025**

    New: Added support to capture the meeting transcript and summary provided by Zoom in ServiceNow.

-   **Version 1.7.0 - May 2025**

    New: The "deny-unless" authentication ACL allows only authenticated users to access the tables related to collaboration services. This ACL significantly improves the security of the data and prevents unauthorized access.

-   **Version 1.6.2 - February 2025**

    Fixed: Incorrect messages displayed for unauthenticated user actions.

-   **Version 1.6.1 - July 2024**

    Fixed: Support added for adding users from different domains as participants on conference calls.

-   **Version 1.6.0 - February 2024**
    -   Fixed: Duplicate entries created in Notify participant table.
    -   Removed: Support for Verification Token with this release aligning with Zoom's plan to sunset verification token as of February 3, 2024. Secret Token must be mandatory for authentication. For more details, refer KB1212919.
-   **Version 1.5.0 - August 2023**
    -   New: Support for Notify UIB plugin.
    -   Fixed: Webhook validation token was a mandatory field when you upgrade to Notify Zoom Connector v1.4. This field is now optional.
-   **Version 1.4.0 - May 2023**
    -   Added:
        -   This release is in line with our plan to transition from Verification/Validation to Secret Token as specified in KB1266167. With this release, you can use the Secret Token as a replacement to Verification/Validation token. You can adopt the new Secret Token based verification by populating the "Webhook secret token" on the configuration form \(Notify &gt; Zoom &gt; Configuration\) on the ServiceNow instance and leave the "Webhook validation token" without populating any value on the same page.
        -   You can find the Secret Token on Zoom by navigating through Marketplace &gt; \(your Zoom Integration app\) &gt; Features &gt; Secret Token.
        -   Once you populate the Secret Token, ensure you click on "Validate" on the webhook event subscriptions in Marketplace &gt; \(your Integration app\) &gt; Features &gt; General Features. This will validate that your instance is capable of receiving webhook events from Zoom. For more details refer Validate your webhook endpoint.
        -   As per Zoom's announcement, Zoom will sunset the verification token in October 2023, and you must use the Secret Token post October 2023. However, in this release, ServiceNow is not mandating the use of Secret Token, and you may continue to use the verification token until October 2023. However, if you are creating new webhooks, or modify the existing webhook endpoints, or event subscriptions then a validation of the endpoint is necessary for which the Secret Token is required.
        -   For more information, refer KB1266167 Transition into using Secret Token.
-   **Version 1.3.4 - March 2023**
    -   ServiceNow supports Zoom's transition from current verification token to secret token. For more details visit, https://marketplace.zoom.us/docs/api-reference/webhook-reference/\#verify-webhook-events.
    -   ServiceNow is planning to support the transition in a phased approach. As per the current updates from Zoom, the Verification token will be sunset on October 2023 for all users, and they must use the secret token post October 2023. Also, Zoom has a requirement for Web hook endpoint validation starting October 2022. For more details, visit https://marketplace.zoom.us/docs/api-reference/webhook-reference/\#validate-your-webhook-endpoint.
    -   This requirement is mandatory for all new Web hooks created after October 2022, however, if you are using a Web hook endpoint created before October 2022, the validation isn't required unless the end point is modified or a new event subscription is created.
    -   In this release, we are addressing the need for Web hook endpoint verification between ServiceNow and Zoom for seamless conference calls. The Secret Token is introduced in this release to support the same. The secret token will not be used for verifying the Web hook events, instead will only be used to support Zoom's Web hook endpoint verification.
    -   We have prepared a tentative plan for this transition and the same can be found on KB1266167.
-   **Version 1.3.3 - February 2023**
    -   Fixed:
        -   Restarting a meeting shows incorrect conference code.
        -   Localization fixes.
-   **Version 1.3.2 - November 2022**

    Changed: Build process improvements.

-   **Version 1.3.1 - September 2022**
    -   New: Localization support added.
    -   Fixed:
        -   Validation token clears on upgrade.
        -   Zoom Configuration is not preserved when you clone an instance.
        -   Duplicate entries created for a conference participant when an invited user joins anonymously without logging in.
-   **Version 1.3.2 - March 2022**
    -   New:
        -   Added support to use the 'Email' field in Zoom events related to participant's presence in the meeting.
        -   Changed the attribute names to accommodate changes in the callback structure for Zoom events.
    -   Changed: Modified the minimum version requirement for Zoom Spoke app to 2.0.2.
    -   Fixed: One fix related to cache flush.
-   **Version 1.2.2 - September 2021**

    Changed: Modified the minimum version requirement for Zoom Spoke app to 2.0.0.

-   **Version 1.2.1 - June 2021**
    -   Fixed:
        -   Participants can re-join to an active conference call using the "Join Call" feature. This feature is available on the task and the Major Incident Workbench.
        -   The host can add the participants if they leave an active conference call using the "Add Participant" feature.
-   **Version 1.2.0 - March 2021**
    -   Changed: Key Management Framework \(KMF\) plugin isn't active by default for Orlando and Paris. The change here ensures that the app loads KMF related files only when KMF is active.
    -   Minor fixes.
-   **Version 1.1.5 - December 2020**

    Fixed: Unable to process the email ID with more than 40 characters.

-   **Version 1.1.3 - June 2020**
    -   Fixed:
        -   Meeting Agenda is now set from conference description and Topic is set from source record display value. Previously both were set from the conference description.
        -   Zoom recording links are now getting captured. In the last release, changes at the Zoom Video Communications side had resulted in broken links.
-   **Version 1.1.2 - April 2020**
    -   New:
        -   Zoom meeting recording links are captured in Notify Recordings table.
        -   Zoom meetings can be centrally configured to not have passwords.
        -   Zoom configuration page optionally enables you to select a Workflow which is triggered when Zoom conference is created or modified.
        -   A Workflow is also shipped as demo data which can be selected for above configuration. The Workflow sends SMS with Zoom meeting link to participants if a Notify Telephony connector is configured.
    -   Fixed: Fixed issues with error messages presented by this connector, where they were presented multiple times or were misleading.
-   **Version 1.0.3 - September 2019**
    -   Start and end a Zoom meeting directly from any task record such as incident, change request, etc. including the Major Incident Workbench.
    -   Manage a Zoom meeting by adding or removing participants.
    -   Track and report on the meeting details, such as meeting duration, and attendees, for further analysis.

**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


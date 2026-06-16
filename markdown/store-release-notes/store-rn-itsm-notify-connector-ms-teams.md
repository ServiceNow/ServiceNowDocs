---
title: Notify Connector for Microsoft Teams release notes
description: Version history for the IT Service Management Notify Connector for Microsoft Teams application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-notify-connector-ms-teams.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Notify Connector for Microsoft Teams release notes

Version history for the IT Service Management Notify Connector for Microsoft Teams application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.10.3 - May 2026**

    Fixed: The Events API flow no longer sends duplicate call notifications.

-   **Version 2.10.2 - April 2026**

    Fixed: Errors in Transcript Flow via Events API.

-   **Version 2.10.1 - March 2026**

    Fixed: Change notifications for Transcripts will only be enabled when it is explicitly opted.

-   **Version 2.10.0 - December 2025**
    -   New:
        -   Support for Events API.
        -   Support for Transcripts Extraction from Microsoft Teams.
        -   Granular Admin role.
    -   Fixed: Broken flow with v1 Beta API.
-   **Version 2.9.0 - August 2025**
    -   Changed: The initiator of the meeting will now be the co-organizer. This change will enable features like break out rooms in a Microsoft Teams meeting. This behaviour will apply to existing users and can be changed in the configuration page.
    -   Fixed:
        -   Issues with callback handling giving exception for MSP instances.
        -   Callback error handling for scenarios with certain malformed data payload types.
-   **Version 2.8.0 - May 2025**

    Added: The "deny-unless" authentication ACL allows only authenticated users to access the tables related to collaboration services. This ACL significantly improves the security of the data and prevents unauthorized access.

-   **Version 2.7.8 - February 2025**
    -   Fixed/Changed:
        -   API improvements for Start Group Call
        -   Handled duplicate email for Microsoft Azure users.
        -   Added Suffix - Pre Published to OOB Application Registry for easier recognition of the flavour of setup.
-   **Version 2.7.6 - November 2024**
    -   Fixed:
        -   Participants will now be invited in batches of 50 to prevent errors in certain scenarios.
        -   Add error handling and messaging for the invalid UPN field.
-   **Version 2.7.5 - September 2024**

    Fixed: Removed the JTI validation requirement from the base system OIDC record as it causes errors.

-   **Version 2.7.4 - July 2024**
    -   Fixed:
        -   Deep links to conference calls chat threads.
        -   Application name 'ServiceNow for Microsoft 365' changed to 'ServiceNow for Teams' on installing plugin.
        -   Multiple alert messages for invalid user on start conference call modal.
        -   Incorrect alert message when Join call fails for user with invalid/no email.
-   **Version 2.7.3 - March 2024**
    -   New:
        -   Implemented Clone Preservers and exclusion features for configuration records.
        -   Updated NotifyTeamsDatabase Script Include to Support Non-SNC environments and increase customization options.
    -   Fixed:
        -   Issues with MSP Support.
        -   "undefined" BOT Name in the calling popup.
        -   Issue with Join call for users with an empty email field.
-   **Version 2.7.2 - December 2023**
    -   Fixed:
        -   Issues related to Domain Separation support.
        -   In a call where the call recording or the transcription is enabled, the call doesn't end when the participants leave the call.
-   **Version 2.7.1 - October 2023**

    Fixed: Calls were intermittently dropped upon initiation.

-   **Version 2.7.0 - August 2023**
    -   New: Support for Notify UIB plugin.
    -   Fixed: The bot calls the participant multiple times even if the meeting invite is declined.
-   **Version 2.6.3 - May 2023**
    -   Fixed:
        -   Added the support to restrict addition of the meeting chat links in Notify Recording table for conference calls using sn\_notify\_msteams.suppress\_chat\_link\_in\_notify\_recording system property.
        -   Fixed an issue with Join call feature for Major Incident Management workbench.
    -   Changed: Notify number table will no longer be used to store the dial-in "toll" or "toll-free" numbers for Microsoft Teams conference calls.
-   **Version 2.6.2 - February 2023**
    -   Fixed:
        -   Fixed an issue which resulted in multiple duplicate numbers getting added in the Notify Number table.
        -   In some cases Webhook validation was failing, resulting in stale meeting information on the Workbench to be displayed like particpant and meeting status.
        -   In some sceanrios some of the invitees where not recieving notifications.
-   **Version 2.6.0 - November 2022**

    Fixes.

-   **Version 2.5.0 - August 2022**

    Changed: Minor fixes.

-   **Version 2.4.2 - May 2022**

    Minor fixes.

-   **Version 2.4.0 - February 2022**
    -   New:
        -   Added support for:
            -   Joining the confernce call through conference phone numbers \(dial-in info / access code\) to expedite Microsoft Teams meeting for Major Incident Management \(MIM\)
            -   Additional administrative controls for who can bypass the lobby
    -   Fixes
-   **Version 2.2.5 - November 2021**

    Fixes for stabilisation

-   **Version 2.2.3 - September 2021**
    -   New:
        -   Added support for guest users added to the Tenant for look-up via e-mail
        -   Added support for UPN \(Microsoft's User Principle Name\) to be specified in field other than sys\_user.email to lookup azure users.
        -   Uptake of new API recommended by Microsoft, for creating online Meeting, with support for Application Access policy.
    -   Fixed: Microsoft Teams Meeting Extensibility experience, which now relies on newer API for creating Online Meeting.
-   **Version 2.1.2 - June 2021**

    New: Added support for Azure Multi-Tenant app. The users can use the BOT shipped by ServiceNow for the Microsoft Teams meeting.

-   **Version 2.0.1 - February 2021**
    -   New: For calls requiring higher-touch resolution, an agent can promote a Chat to a Microsoft Teams Call, directly from Agent Workspace. Requires - Agent Chat \(Plugin\).
    -   Minor fixes
-   **Version 1.0.4 - December 2020**

    Minor fixes

-   **Version 1.0.4 - December 2020**

    Minor fixes

-   **Version 1.0.2 - November 2020**

    Notify connector for Microsoft Teams provides support for conference calls on the ServiceNow AI Platform for rapid communication with internal team members, customers, and contractors.


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


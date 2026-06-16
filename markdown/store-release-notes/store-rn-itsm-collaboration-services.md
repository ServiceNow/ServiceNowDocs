---
title: Collaboration Services release notes
description: Version history for the IT Service Management Collaboration Services application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-collaboration-services.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Collaboration Services release notes

Version history for the IT Service Management Collaboration Services application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.13.3 - June 2026**
    -   Fixed:
        -   A user with a comma in the name will get "and" instead of the comma.
        -   ACLs.
        -   Filtering of MS Teams chats not working in SOW.
        -   External is coming against some users while importing the team's chat.
        -   Internal fixes.
-   **Version 3.13.0 - March 2026**
    -   Changed:
        -   Removed Choose your preferred chat client option from start teams chat model, from this release the redirection will always go to new web/desktop client deeplink
        -   Optimised auto-import to reduce the number of IHub transactions during Auto-Import flow.
-   **Version 3.12.2 - December 2025**
    -   Fixed:
        -   Handling refresh token revocation failure is improved for better resilience during authentication changes.
        -   IHub Exceptions in Auto Import now allow for graceful retries before exiting, enhancing import stability.
        -   Fixed an error in the Teams Chat portal widget.
        -   The "Start chat" action now redirects to the new desktop client by default.
        -   A new granular admin role, sn\_tcm\_collab\_hook.admin, has been introduced for collaboration hooks.
        -   Insufficient privilege error affecting the Slack integration.
-   **Version 3.11.6 - August 2025**
    -   New:
        -   Microsoft Teams Auto-import will be turned off by default for new installations.
        -   When you start a Microsoft Teams chat, you will be automatically redirected to the new Teams client, which will be the default option.
-   **Version 3.11.1 - May 2025**
    -   New: The "deny-unless" authentication ACL that only authenticated users can access tables related to collaboration services. This significantly improves the security of the data and prevents unauthorized access.
    -   Fixed:
        -   Stabilized the auto-import process, reducing the occurrence of errors and ensuring that attachments are consistently imported without interruptions.
        -   Download process for pasting the images is stabilized, ensuring that images are consistently and accurately downloaded without any interruptions.
        -   The dynamic translation feature is improved to provide more accurate and contextually appropriate translations for imported messages.
-   **Version 3.10.9 - March 2025**

    Fixed: Internal build related artifact.

-   **Version 3.10.7 - February 2025**
    -   Fixed:
        -   Issues with emoji in auto import.
        -   Error handling in MS Teams Auto-Import functionality.
        -   Picker Search is failing while searching for users.
        -   Error when opening reassigned chat.
-   **Version 3.10.6 - November 2024**
    -   Fixed:
        -   Chat title was empty in title with newlines.
        -   Unable to start chat with unverified users.
        -   Issues with Automatic Import.
        -   Other fixes.
-   **Version 3.10.5 - August 2024**

    Minor fixes.

-   **Version 3.10.3 - May 2024**

    Minor fixes.

-   **Version 3.9.1 - February 2024**

    Minor fixes.

-   **Version 3.9.0 - November 2023**
    -   Fixed:
    -   -   Component accessibility related issues with the Microsoft Teams chat components.
-   Fixed issue related to auto import failing on final poll of messages.
-   Fixed issue related to Start Microsoft Teams Chat.
-   Other minor bug fixes.
-   **Version 3.8.4 - August 2023**
    -   Fixed:
        -   Chats are not imported correctly from Microsoft Teams on the incident in Service Portal.
        -   Importing messages from Microsoft Teams.
        -   Importing the messages from Slack channel's tab in user profile.
-   **Version 3.8.2 - May 2023**
    -   New: Added search based on User ID when starting a Microsoft Teams chat on Agent Workspace.
    -   Fixed:
        -   Fixed issue with starting Microsoft Teams chat when trying to add any recommended user with empty email.
        -   Other minor bug fixes.
-   **Version 3.8.0 - February 2023**
    -   New:
        -   Implemented the auto import of chat messages from Zoom to ServiceNow.
        -   Implemented the support for the re-assignment flows, which is when the assignee of the ticket is changed, the new user gets added to the Zoom Team chat automatically.
        -   Support for nested replies in auto import for Zoom Team chat.
        -   Handled the auto close/closure conditions of the ticket and importing the messages from Zoom for one last time.
-   **Version 3.7.3 - January 2023**
    -   New: Zoom Team Chat
    -   Fixed: A minor issue in the True-up is fixed.
-   **Version 3.7.0 - November 2022**

    Added support for Zoom Team Chat.

-   **Version 3.6.1 - August 2022**
    -   New:
        -   Added framework support for:
            -   Added ability to display Microsoft Teams chat history associated with a ticket on Employee Center.
            -   Added ability for a third-party service provider to initiate a chat from ServiceNow with an employee in a different Microsoft Teams tenant.
    -   Changed: Minor fixes.
-   **Version 3.5.1 - May 2022**

    New: Added framework support for fetching user presence in Teams for Request Based Chat.

-   **Version 3.4.1 - February 2022**
    -   New: Added support to customize User Principal Name \(UPN\) field as defined in Microsoft Azure portal instead of using sys\_user.email field for a user.
    -   Fixes.
-   **Version 3.2.5 - November 2021**

    Fixes

-   **Version 3.2.3 - September 2021**
    -   New:
        -   Added support for Microsoft Teams changes
        -   Request Based Chat
            -   Request based chats can now be imported automatically, saving agents time on each ticket.
            -   Added **Start Chat** action to Catalog tasks.
    -   Fixes
-   **Version 3.1.7 - June 2021**
    -   New: Added support for Azure Multi-Tenant app. The users can use the Azure apps shipped by ServiceNow instead of creating their own apps for integration.
    -   Minor fixes
-   **Version 3.0.4 - February 2021**

    Added Slack and MS Teams notification and Chat Collaboration on Major Incidents and Incident Communication Plans.

-   **Version 2.0.10 - December 2020**

    Minor fixes

-   **Version 2.0.5 - November 2020**
    -   New: Added support for Microsoft Teams for task-based collaboration
    -   Changed: Renamed 'Collaboration Services for Task Management' as 'Collaboration Services'
    -   Removed: Removed dependencies on Task Communications Management and Major Incident Management
-   **Version 1.0.3 - July 2019**

    Fixed: Group contacts in an existing ICP record were not added to a Slack channel if ICT was added at a later point in time \(PRB1343447\)

-   **Version 1.0.2 - May 2019**

    Initial release of Collaboration Services for Task Communications Management.


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)


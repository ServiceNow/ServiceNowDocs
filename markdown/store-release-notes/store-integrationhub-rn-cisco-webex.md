---
title: Cisco Webex Meetings spoke release notes
description: Version history for the Integration Hub Cisco Webex Meetings spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-cisco-webex.html
release: store
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Cisco Webex Meetings spoke release notes

Version history for the Integration Hub Cisco Webex Meetings spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.3 - August 2024**

    Fixed: Defect related to creating OAuth application from the new Webex Developer Portal.

-   **Version 2.3.2 - May 2024**

    Fixed: Remove user\_modify scope from Connection Template.

-   **Version 2.3.1 - September 2023**
    -   Removed: Deprecated 4 actions due to EOL announcements from Cisco Webex:
        -   Get Users
        -   Get User Activity
        -   Remove User
        -   Look up Events Stream
    -   Cisco Webex announced the deprecation of their SOAP APIs and published new REST APIs. You can find replacement actions for the deprecated actions here in Cisco Webex Teams Spoke.
-   **Version 2.2.2 - December 2022**

    New: Localization framework.

-   **Version 2.1.1 - June 2022**

    Fixed: Patch release of Cisco Webex Meetings Spoke. This version fixes an install error observed at logs - "webexAccGr" is not defined.

-   **Version 1.0.3 - March 2020**
    -   New: Features for managing user's Cisco Webex Meetings subscriptions and actions
    -   Fixed:
        -   The Webex Meetings OneForm experience didn't have the necessary scope for reclamation
        -   The Webex Meeting's account table connection column wasn't editable
-   **Version 1.0.2 - January 2020**

    Provides actions to manage Cisco Webex Meetings software subscriptions.



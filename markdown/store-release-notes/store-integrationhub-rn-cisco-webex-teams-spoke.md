---
title: Cisco Webex Teams spoke release notes
description: Version history for the Cisco Webex Teams Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-cisco-webex-teams-spoke.html
release: store
topic_type: reference
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Cisco Webex Teams spoke release notes

Version history for the Cisco Webex Teams Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.6 - December 2025**

    A bug has been fixed in the "Look up Events Stream" of the Cisco Webex Update User Activity subflow. Previously, the date/time value was not being updated between executions, resulting in the repeated processing of the same time frame and subsequent timeouts. This issue has been resolved by ensuring that the date/time parameter now updates correctly between executions.

-   **Version 2.3.5 - November 2024**

    Fixed: Action - Look up People Stream.

-   **Version 2.3.4 - May 2024**

    Fixed: Issue related to Look up Licenses action error response.

-   **Version 2.3.3 - March 2024**

    Fixed: OAuth API script in the OOB Application Registry.

-   **Version 2.3.2 - January 2024**

    Fix related to fetching OAuth Token.

-   **Version 2.3.1 - September 2023**
    -   New:
        -   Delete Person
        -   Look up Meetings Stream \(look\_up\_meetings\_stream\)
    -   Removed: Deprecated Look up Meetings \(list\_meetings\).
-   **Version 2.2.4 - August 2023**

    Fixed: The Look up People Stream and Look up User Stream actions are fixed to handle the Webex API pagination limit.

-   **Version 2.2.3 - January 2023**
    -   New: Location changes.
    -   Fixed: Look Up Meetings action.
-   **Version 2.2.1 - October 2022**

    Fixed: Patch release of Cisco WebEx Teams Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 2.2.0 - June 2022**

    New: Minor release for the Cisco WebEx Teams Spoke. This version includes a new action, Look up Meetings.

-   **Version 2.1.0 - October 2021**
    -   New: New actions for Meeting management.
    -   Fixed: Fixes within Create Meeting, Create Webhook and Get Webhook actions, and agent not getting updated within outlook invite.
-   **Version 2.0.2 - August 2021**
    -   New: In this release, these actions are added:
        -   Event Management
            -   Look up Events stream
        -   People Management
            -   Update Person
            -   Look up Person Details
            -   Look up People Stream
        -   Organization Management
            -   Look up Organizations
        -   License Management
            -   Look up Licenses
            -   Look up Roles
-   **Version 1.0.2 - July 2021**

    New: Patch release of the Cisco Webex Teams spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields.

-   **Version 1.0.1 - September 2020**

    New: Provides actions to automate the management of Spaces, Messages, and Memberships in Cisco Webex Teams.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)


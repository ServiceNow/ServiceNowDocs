---
title: Smartsheet spoke release notes
description: Version history for the Smartsheet spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-smartsheet.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Smartsheet spoke release notes

Version history for the Smartsheet spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.7.0 - June 2026**
    -   Fixes:
        -   Security fix on non-glide ACLs
        -   Pagination for Look up Webhooks Stream action
        -   Added description hint on the "Sheet count" for Look up User ID action
        -   Deprecated the old "Create Folder" action and created 2 new actions of "Create Folder in Workspace" and "Create Folder in Folder" via the new Smartsheet APIs
        -   Deprecated the old "Look up Folders Stream" and replaced with the new action of the same label using the new Smartsheet API
        -   Refined Create Share Sheet, Update Share Sheet, and Look up Sheet Shares Stream actions
-   **Version 2.6.1 - January 2026**
    -   Fixed: Setting the values of the rows with values coming from system properties
    -   Fixed: Mismatch in data types in create and update row input fields
-   **Version 2.6.0 - November 2025**

    Security patch: Improved sample webhook registry security.

-   **Version 2.5.0 - September 2025**

    Added required ACLs and Roles as per the AI Security Directive guidelines.

-   **Version 2.4.1 - August 2025**
    -   Fixed: AI Agents: Tools - Output response includes anchor tags that are not rendered as clickable link
    -   Added: Expose Connection url on the connection template for Gov customers
-   **Version 2.4.0 - May 2025**

    Minor release with new AI agents.

-   **Version 2.3.1 - February 2025**

    Fixed: "glide.rest.max\_content\_length" to be shipped as global level property instead of plugin.

-   **Version 2.3.0 - November 2024**

    Evaluated and modified Sandbox Access for Client-Callable Script Includes as false.

-   **Version 2.2.1 - August 2024**

    Look up User Activity Stream action issue is fixed.

-   **Version 2.2.0 - May 2024**

    Added Last Login output variable in the Look up Users Stream action.

-   **Version 2.1.4 - November 2023**

    Fixed: Reclamation functionality from vendor making changes for deactivating users.

-   **Version 2.1.3 - May 2023**

    Added "report view" ACLs to the table columns with sensitive info.

-   **Version 2.1.2 - March 2023**
    -   Added actions beyond user management and subscription management
    -   Bug fixes
-   **Version 2.1.1 - January 2023**
    -   Added actions beyond user management and subscription management
    -   Bug fixes
-   **Version 2.0.0 - February 2021**
    -   Smartsheet spoke provides actions to see and understand Smartsheet software subscriptions.
    -   This release adds new features for managing user's Smartsheet subscriptions and actions.
-   **Version 1.0.1 - January 2021**
    -   Smartsheet spoke provides actions to see and understand Smartsheet software subscriptions.
    -   This release adds new features for managing user's Smartsheet subscriptions and actions.


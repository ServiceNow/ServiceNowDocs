---
title: Microsoft AD v2 spoke release notes
description: Version history for the Microsoft AD v2 Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ms-ad-v2.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft AD v2 spoke release notes

Version history for the Microsoft AD v2 Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.5.3 - May 2026**

    Fixed: Action: Look up User Password Expiration Details - Various date format support

-   **Version 2.5.2 - April 2026**

    Fixed: Action - Is User In Group

-   **Version 2.5.1 - October 2025**
    -   New: Delete Object Action - Created a new equivalent action with additional recursive property.
    -   Changed: Delete Object Action - Deprecated the old action
    -   Fixed:
        -   Look up Computer Action - memberof property.
        -   Look up User Action - with users whose OU contains comma \(,\) &amp; info property.
-   **Version 2.5.0 - September 2025**

    Fixed - Required ACL\(s\) and Role\(s\) for agents.

-   **Version 2.4.1 - August 2025**

    Fixed - AI Agents - Renaming and Output transformation strategy

-   **Version 2.4.0 - March 2025**

    Minor release with new AI agents.

-   **Version 2.3.0 - February 2025**
    -   Added two conversational Spoke Actions.
    -   Fixed: Generate a Random Password Action and avoid a false alarm warning message when the AD is in a different domain than that of the MID Server, or when the MID Server does not have ADWS installed.
-   **Version 2.2.1 - December 2024**

    Fixed: Add User to Group action.

-   **Version 2.2.0 - November 2024**

    Enabled "Look up User" Spoke Action to be Now Assist conversational capable.

-   **Version 2.1.1 - December 2023**
    -   Fixed:
        -   'Create User' action now creates appropriate User logon name and assigns it
        -   'Look up Objects by Filter' action now returns consistent results whether search results a single or multiple objects
-   **Version 2.1.0 - December 2022**
    -   New:
        -   Computer Management - Disable Computer, Does Computer Exists, Enable Computer, Is Computer Disabled
        -   Group Management - Add Computer to Groups, Add Computers to Group, Add Users to Group, Create Group, Delete Group, Does Group Exists, Look up Group, Remove Computer from Groups, Remove Computers from Group, Remove Users from Group
        -   Object Management - Update Object Expiration
    -   Changed: Update action name for metadata actions fromLook up User Additional Fields \(Metadata\) to Get User Additional Fields \(Metadata\).
-   **Version 2.0.1 - November 2022**
    -   This is a new major release \(2.0.0\).
    -   New:
        -   Authentication template for spoke connection from Connections dashboard
        -   New User Management actions: Look up User, Update User
        -   New Computer Management actions: Create Computer, Delete Computer, Look up Computer, Update Computer
        -   New Object Management actions: Create Object, Delete Object, Look up Object by Filter, Update Object OU
        -   Added a newer version for the 15 deprecated actions with modern error handling and complex object outputs.
    -   Changed:
        -   Name of the spoke from "Microsoft AD v2 Spoke" to "Microsoft Active Directory v2 Spoke"
        -   Add User to Group -&gt; Add User to Groups for bulk actions
        -   Remove User from Group -&gt; Remove User from Groups for bulk actions
    -   Removed: Deprecated 15 actions
-   **Version 1.2.0 - July 2022**

    New: This is a minor release for MS AD V2 with a new Create User action.

-   **Version 1.1.2 - November 2021**

    Fixed: Patch release for MS AD V2 with fixes.

-   **Version 1.1.1 - October 2021**

    Fixed: This version fixes an issue at action 'Look up User Password Expiration Details' for user whose password is set to never expire.

-   **Version 1.1.0 - September 2021**

    New: This version adds a new action 'Look up User Password Expiration Details' and other fixes.

-   **Version 1.0.0 - April 2021**

    New: Microsoft AD v2 spoke provides actions to automate Microsoft Active Directory tasks for User Management &amp; Authentication and Group Membership.



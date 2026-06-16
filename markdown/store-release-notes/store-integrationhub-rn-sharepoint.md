---
title: Microsoft SharePoint Online spoke release notes
description: Version history for the Integration Hub Microsoft SharePoint Online Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-sharepoint.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft SharePoint Online spoke release notes

Version history for the Integration Hub Microsoft SharePoint Online Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.11.0 - June 2026**

    Fixed: Streamline ACLs.

-   **Version 2.10.0 - September 2025**

    Fixed - Required ACL\(s\) or Role\(s\) for agents, Copy Attachment to folder action, handling default value for actions where true/false inputs are present.

-   **Version 2.9.1 - July 2025**

    Fixed: AI Agents - Naming, Output Transformation.

-   **Version 2.9.0 - May 2025**

    Minor release with new AI agents.

-   **Version 2.8.1 - March 2025**

    Minor release with new AI agents.

-   **Version 2.7.1 - December 2024**

    Fixed: ScriptInclude errors.

-   **Version 2.7.0 - September 2024**
    -   New:
        -   Subflows:
            -   Delete Modern Site \(without O365 Group\) \(delete\_modern\_site\_without\_o365\_group\)
            -   Submit Modern Site \(with O365 Group\) for Deletion \(submit\_modern\_site\_with\_o365\_group\_for\_deletion\)
        -   Actions:
            -   Create Modern Site \(create\_modern\_site\)
            -   Create Subsite \(create\_subsite\)
            -   Delete Subsite \(delete\_subsite\)
            -   Delete Modern Site \(delete\_modern\_site\)
            -   Delete Modern Site with O365 Group \(delete\_modern\_site\_with\_o365\_group\)
            -   Look Up Sites Stream \(look\_up\_sites\_stream\)
            -   Look Up Modern Site Group Information \(look\_up\_modern\_site\_group\_information\)
            -   Look Up Modern Site Information \(look\_up\_modern\_site\_information\)
    -   Fixed: Action: Add User To Group - Added Site Location input as well.
    -   Removed:
        -   Deprecated actions:
            -   Create Site \(create\_site\)
            -   Delete Site \(delete\_site\)
            -   Look Up Sites \(lookup\_sites\)
-   **Version 2.6.1 - August 2024**
    -   New - Action: Look up M365 Members by Site Group
    -   Fixed - Action: Copy attachment to Folder - For encoding issues
-   **Version 2.5.0 - May 2024**

    New: Added action - Look up Search Query Results Stream.

-   **Version 2.4.6 - March 2024**

    Fixed: Issues related to OAuth scripts - Check active flag on the connection.

-   **Version 2.4.5 - February 2024**

    Fixed: Invalid URI issue when filenames have multilingual names.

-   **Version 2.4.4 - January 2024**

    Changed: Look up Files, Look up File - Added additional output fields.

-   **Version 2.4.3 - October 2023**
    -   Fixed:
        -   Not able to get authentication token
        -   User permission actions not working for non root site collection
        -   Share Folder with Group action has no access level options
-   **Version 2.4.1 - April 2023**
    -   Fixed:
        -   Error handling for Look up Permissions action
        -   Script include to handle JSON parsing better
-   **Version 2.4.0 - February 2023**
    -   Changed: Spoke name
    -   Fixed: JSON parsing and retry policies for many actions
-   **Version 2.3.0 - September 2022**

    New: Added action - Look up Role Assignments

-   **Version 2.2.0 - August 2022**
    -   New:
        -   Added 2 new actions
            -   Site Management - Look up Site Permissions
            -   File Management - Look up File Permissions
-   **Version 2.1.2 - February 2022**

    New: Patch version of Microsoft SharePoint Spoke. This version includes missing dependencies from earlier version.

-   **Version 2.1.1 - December 2021**

    Fixed: Patch release of Microsoft SharePoint Spoke for IntegrationHub. This includes fixes for issues with tenant flows, an error within the Lookup Drive action, and security bugs.

-   **Version 2.0.2 - June 2021**

    Minor version of the SharePoint Spoke for IntegrationHub. This version includes a change to the Look up Files action.

-   **Version 2.0.1 - January 2021**

    Patch version release for the SharePoint spoke.

-   **Version 1.1.2 - August 2020**

    New: This version enables the spoke to work on both online and on-prem versions of SharePoint.

-   **Version 1.0.4 - August 2019**

    Licensing patch for the Microsoft SharePoint Online spoke on Integration Hub

-   **Version 1.0.3 - April 2019**

    Branding patch for the Microsoft SharePoint Online spoke

-   **Version 1.0.2 - March 2019**

    Provides flows and actions to automate collaboration, document management, and user access rights in Microsoft SharePoint.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)


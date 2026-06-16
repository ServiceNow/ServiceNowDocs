---
title: Microsoft OneDrive spoke release notes
description: Version history for the Integration Hub Microsoft OneDrive Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-onedrive-spoke.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft OneDrive spoke release notes

Version history for the Integration Hub Microsoft OneDrive Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.9.0 - June 2026**

    Fixed: Streamline ACLs

-   **Version 2.8.2 - May 2026**
    -   Fixed:
        -   Actions: Look up File or Folder Item Info by ID and Look up File or Folder Item Info by Path added newer output fields
        -   Support for file names ending in -
-   **Version 2.8.1 - November 2025**

    Fixed - Security defect related to read-only

-   **Version 2.7.0 - October 2025**

    Fixed: Security issue.

-   **Version 2.6.2 - September 2025**

    Fixed - Required ACL\(s\) / Role\(s\) for agents, Granular admin access checks in various actions.

-   **Version 2.5.1 - August 2025**

    Fixed - AI Agents: Renaming and Output transformation strategy

-   **Version 2.5.0 - March 2025**

    Minor release with new AI agents.

-   **Version 2.4.0 - November 2024**
    -   New:
        -   Added Retry Policy - Microsoft OneDrive HTTP Retry Policy to the default connection &amp; credential alias OneDrive \(sn\_onedrive\_spoke.OneDrive\), that Honor "Retry-After" Header.
        -   Updated all actions except 3 to have the retry policy enabled.
-   **Version 2.3.2 - February 2024**

    Fixed the labels.

-   **Version 2.3.0 - November 2022**

    Minor release of Microsoft OneDrive Spoke for Integration Hub. This version include changes to expose attributes to output.

-   **Version 2.2.1 - September 2022**

    Patch version of Microsoft OneDrive Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 2.2.0 - August 2022**

    New: The minor release of Microsoft OneDrive Spoke for IntegrationHub. This version adds actions to Create Upload Session, Delete Upload Session, Upload Large File, and includes fixes to handle error codes for 4xx &amp; 5xx API responses.

-   **Version 2.1.1 - December 2021**

    Changed: Patch release of Microsoft OneDrive Spoke for IntegrationHub. This version includes security-related changes.

-   **Version 2.1.0 - June 2021**

    Added the Look up Subscription Metadata helper action to generate dynamic choices of subscription list for other actions. It is for only available for internal use and is not available to use in a flow.

-   **Version 1.6.0 - April 2021**
    -   Fixed:
        -   JSON response body is now updated with drag-n-droppable data pills so that end user can create workflow in Flow Designer 10x easier
        -   Added permission management to control file or folder access
        -   Enable link sharing capability for a file or folder with collaborators
        -   Manage webhook subscription for inbound integration from Onedrive to ServiceNow
-   **Version 1.5.2 - September 2020**

    Minor release of Microsoft OneDrive spoke for IntegrationHub.

-   **Version 1.0.1 - August 2019**

    Licensing patch for the Microsoft OneDrive Spoke on Integration Hub.

-   **Version 1.0.0 - June 2019**

    Initial release of Microsoft OneDrive Spoke for Integration Hub.



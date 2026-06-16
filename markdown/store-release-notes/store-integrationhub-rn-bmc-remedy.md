---
title: BMC Remedy spoke release notes
description: Version history for the Integration Hub BMC Remedy spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-bmc-remedy.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# BMC Remedy spoke release notes

Version history for the Integration Hub BMC Remedy spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.0 - June 2026**

    Fixed: Streamline ACLs

-   **Version 1.4.1 - October 2024**
    1.  Enabled Java 11 support.
    2.  Fixed: The Incident's Additional comments with multiple lines is being truncated in the Update Record action and any other actions that use dynamic templates.
-   **Version 1.3.0 - May 2023**

    Added Authentication Template for one-click setup of this spoke.

-   **Version 1.2.2 - September 2022**

    Patch version of BMC Remedy Spoke for IntegrationHub. This version includes a fix to improve the installation performance of the spoke and an update to the Icon displayed in the workflow and installed spokes pane.

-   **Version 1.2.1 - July 2022**

    Fixed: Patch version of BMC Remedy Spoke for IntegrationHub. This version includes fixes for missing choices at Create Change and Create Incident actions.

-   **Version 1.2.0 - October 2021**

    Fixed: Security bug

-   **Version 1.1.3 - July 2021**

    Patch release of the BMC Remedy spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields, and adds compatibility to Rome.

-   **Version 1.1.2 - February 2021**

    Patch release of the BMC Remedy spoke for IntegrationHub.

-   **Version 1.1.1 - December 2020**

    Patch release of the BMC Remedy spoke for IntegrationHub.

-   **Version 1.1.0 - November 2020**

    Patch release of the BMC Remedy spoke for Integration Hub.

-   **Version 1.0.1 - May 2020**
    -   The BMC Remedy spoke provides a list of actions that wraps around the primary Remedy REST APIs. It provides the foundation to synchronize ServiceNow and Remedy bi-directionally, such as ticket cutting scenario.

        -   Sync incidents, changes, problems, and theoretically any records through Get, Create, and Update Record Actions.
        -   Bi-directionally create and update incidents between ServiceNow and Remedy.
    -   Enterprises can have multiple ITSM systems to handle different incidents, changes, problems, and so on, for different departments. Sometimes, this can be set up to differentiate regionally or strategically. Irrespective of the reasons, the BMC Remedy spoke synchronizes ServiceNow and BMC Remedy easily and conveniently so that the end-users can view and modify ITSM related actions only at one place, instead of swivel chair from different places.


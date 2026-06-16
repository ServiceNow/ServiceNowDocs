---
title: Okta Spoke release notes
description: Version history for the Integration Hub Okta Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-okta.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Okta Spoke release notes

Version history for the Integration Hub Okta Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.8.0 - June 2026**
    -   Security fix on non-glide ACLs
    -   Fixed: API responses pagination for OOB Flow action "Is User in Group"
-   **Version 4.7.1 - November 2025**
    -   Fixed: Passing empty values in Update user Profile action
    -   Fixed: SAM SSO Integration with Okta might pull less SSO Subscriptions in the next run if the first "Download Group Memberships" job failed partially
-   **Version 4.7.0 - September 2025**

    Added required ACLs/Roles as per the AI Security Directive guidelines.

-   **Version 4.6.0 - August 2025**
    -   Added: 9 conversational actions and subflows
    -   Fixed: Security patch updates
-   **Version 4.3.0 - May 2025**

    Minor release with new AI agents.

-   **Version 4.2.7 - October 2024**

    Fixed: Sample flows and subflows that are configured to run as a system.

-   **Version 4.2.6 - March 2023**

    Fixed: Download groups job with unknown field error.

-   **Version 4.2.4 - December 2022**

    Patch release of Okta Spoke for IntegrationHub. This version includes fixes for localization and SaaS Okta integration. The Okta Spoke now supports pre-Utah family releases.

-   **Version 4.2.1 - October 2022**

    Fixed: Patch release of Okta Spoke for Integration Hub. This version adds fixes to improve the installation performance, a documentation issue to auto-populate Authorization URL, Token URL, Token Revocation URL, and changes to module titles "Okta groups".

-   **Version 4.2.0 - May 2022**

    New: Minor release of Okta Spoke. This version add a new action - Look up App Launcher Applications Stream.

-   **Version 4.1.5 - March 2022**

    Removed: In the 4.1.5 release, references to sys\_hub\_action\_status\_metadata are removed that are available in the platform from Rome and not in Quebec.

-   **Version 4.1.4 - December 2021**

    Changed: Patch release of Okta Spoke for IntegrationHub. The version includes security-related changes.

-   **Version 4.1.3 - November 2021**

    Fixed: Patch release of Okta Spoke for IntegrationHub. This version includes fixes for getting the Okta Logs Data Stream Action to return debugContext information

-   **Version 4.1.2 - August 2021**

    Changed: Patch release of the Okta spoke for Software Asset Management. This version includes a fix to support multiple connections to Okta when using SaaS License Management.

-   **Version 4.1.1 - May 2021**
    -   Changed:
        -   Added event hook lifecycle management actions to handle inbound integration from Okta to ServiceNow
        -   New sample inbound subflow from Okta to ServiceNow
        -   New sample remote table to view real-time Okta info without going logging into Okta
        -   New authentication template to configure connection and credential easier
-   **Version 4.1.0 - April 2021**

    Patch release of the Okta spoke for IntegrationHub. This version includes a fix for the password sent incorrectly to Okta.

-   **Version 4.0.4 - March 2021**

    Patch release of the Okta spoke for IntegrationHub. This version includes a fix for the password sent incorrectly to Okta.

-   **Version 4.0.3 - February 2021**

    As part of this release, new a datastream action, Look up User Groups is released and a fix is provided for the Group Memberships delta pull logic.

-   **Version 4.0.2 - January 2021**
    -   New: Added support for toggling between multiple connections on one Connection Credential record
    -   Fixed: Fixed the OAuth token expiration issue
-   **Version 4.0.1 - November 2020**

    Patch release of Okta spoke for IntegrationHub

-   **Version 2.0.0 - October 2020**

    Licensing patch for the Okta spoke on IntegrationHub

-   **Version 1.1.1 - November 2019**

    Licensing patch with the added "Get Groups" Action for the Okta spoke on IntegrationHub

-   **Version 1.0.2 - August 2019**

    Licensing patch for the Okta spoke on Integration Hub

-   **Version 1.0.0 - March 2019**
    -   Provides the necessary actions to easily automate Okta User, Group, and Password Management
    -   Automates User, Group, and Password Management in Okta
    -   Increases productivity and response time of IT support for employee onboarding/offboarding and password reset incidents


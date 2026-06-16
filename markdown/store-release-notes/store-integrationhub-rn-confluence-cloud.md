---
title: Confluence Cloud Spoke release notes
description: Version history for the Confluence Cloud Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-confluence-cloud.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Confluence Cloud Spoke release notes

Version history for the Confluence Cloud Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.1 - June 2026**

    Fixed: Streamline ACLs

-   **Version 2.0.1 - May 2026**
    -   New:
        -   Actions: Report Personal Data. You are now required by Atlassian to report user personal data usage if you store such details using existing actions of the spoke in your apps. Refer to User privacy guide by Atlassian for more details.
        -   Authentication Template for Confluence Cloud. A new authentication template has been introduced for Confluence Cloud customers using 3-Legged OAuth \(3LO\). Refer to the product documentation for more details on how to set up.
    -   Changed: Based on guidance for Building Secure and Scalable Integrations: Our Guidance for Third-Party Apps by Atlassian, the way to set up and authenticate the Confluence Cloud connection has been changed for Confluence Cloud customers.
    -   Removed: Authentication Template for Confluence Cloud. The previous authentication template for Confluence Cloud has been retired. Refer to the product documentation for more details on how to set up.
-   **Version 1.2.6 - January 2026**

    Fixed: Confluence subscription date format issue.

-   **Version 1.2.4 - December 2025**

    Fixed: Confluence subscription license Reclamation Issue

-   **Version 1.2.3 - March 2025**

    In this version, confluence actions are fixed to support site-specific API calls for multi-site use cases.

-   **Version 1.2.2 - December 2024**

    Fixed: Existing actions fail if connection alias is overriden.

-   **Version 1.2.0 - November 2024**

    Added: Look up Pages Stream.

-   **Version 1.1.1 - August 2024**

    Additional APIs/actions added to support AI Search in Confluence.

-   **Version 1.0.5 - September 2022**

    Fixed: Patch release of Confluence Cloud Spoke for Integration Hub. This version fixes an issue with Group Membership that doesn't allow fetching details from a different connection alias.

-   **Version 1.0.4 - October 2021**

    Fixed: Fix to handle latest API change from Confluence Cloud

-   **Version 1.0.3 - August 2021**

    Changed the API base URL as part of the changes incorporated by confluence team

-   **Version 1.0.2 - May 2021**

    Minor release of the Conflluence Cloud spoke.

-   **Version 1.0.0 - March 2021**
    -   New:
        -   Software Subscriptions actions:
            -   Download Subscriptions
            -   Calculate User Activity
            -   Reclaim Subscriptions

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)


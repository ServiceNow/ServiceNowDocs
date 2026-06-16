---
title: ServiceNow Voice for ITSM release notes
description: Version history for the ServiceNow Voice for ITSM integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-servicenow-voice-itsm.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Voice, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# ServiceNow Voice for ITSM release notes

Version history for the ServiceNow Voice for ITSM integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.1.1 - December 2025**

    Changed: Granular roles for configuration. sn\_cti\_core.admin is allowed to configure SN Voice - ITSM related work.

-   **Version 4.0.0 - May 2025**
    -   New:
        -   This versions enables Real Time Transcription. The flows on the Amazon Connect will have to be updated to with the ones that are provided as part of this plugin. If you have custom changes on Amazon Connect they will have to be brought into this new flows
        -   This version also enables Advanced Work Item Assignment routing and call transfers between agents
-   **Version 2.0.10 - February 2024**

    Fixed: Upgraded the Node.js version to 18 bug.

-   **Version 2.0.9 - June 2023**

    Fixed: No functional change; changed the state of the plugin to published.

-   **Version 2.0.8 - February 2023**

    Fixed: minor bug fixes due to buffer length.

-   **Version 2.0.5 - August 2022**

    Fixed: Minor bug fixes for i18n.

-   **Version 2.0.4 - February 2022**

    New: Cloud Call Center for ITSM is now ServiceNow Voice for ITSM.

-   **Version 2.0.2 - August 2021**
    -   New:
        -   Updated cloud formation template to support node.js 14.x runtime for Lambda
        -   Outbound flow template for ITSM Demo Queues for setting up Phone channel Analytics and Queue based routing
-   **Version 2.0.0 - October 2020**
    -   New:
        -   Outbound flow template for ITSM
        -   Demo queues for setting up Phone Channel Analytics and queue based routing
-   **Version 1.0.1 - April 2020**

    Cloud Call Center for ITSM integrates the robust capabilities of ServiceNow's IT Service Management applications with the advanced capabilities of cloud call center providers to provide exciting new experiences for all employees.



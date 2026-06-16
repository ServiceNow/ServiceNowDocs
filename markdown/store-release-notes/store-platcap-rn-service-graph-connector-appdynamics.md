---
title: Service Graph Connector for Observability - AppDynamics release notes
description: Version history for the Service Graph Connector for Observability - AppDynamics integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-appdynamics.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Observability - AppDynamics release notes

Version history for the Service Graph Connector for Observability - AppDynamics integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.6.0 - December 2025**

    New: Added support for multi-instance setup.

-   **Version 1.5.1 - September 2025**
    -   Fixed:
        -   Fixed the issue with Event Push Connector listener for SGO-AppDynamics dropping events and misprocessing payloads.
        -   Bug fixes and other minor improvements.
-   **Version 1.5.0 - August 2025**

    New: Support for OAuth-based authentication. Note: SGC Central supports only OAuth-based authentication for new connections.

-   **Version 1.4.0 - November 2024**

    New: Onboarded to SGC Central.

-   **Version 1.3.1 - June 2024**
    -   Fixed:
        -   Corrected value for "message\_key" in the AppDynamicsEventUtil script
        -   Fixed the metadata field with a valid JSON
        -   Fixed data loading for tags
        -   Fixed the AppDynamicsEventUtil script to reduce delay in loading events
-   **Version 1.2.2 - March 2024**

    Fixed test script for the inbound event.

-   **Version 1.2.1 - August 2022**
    -   Fixed:
        -   Pushing multiple templates to the same instance causes connnection issues.
        -   Remove gs.warn in SGO-AppDynamics Authenticate flow action's output.
        -   Remove the hardcoded user password found in demo user records.
        -   Fixed cross-site scripting \(XSS\) issue has been identified in the AppDynamics Guided Setup page,
        -   Removed port from the controllerName in the data sources.
-   **Version 1.1.0 - December 2021**

    The Service Graph Connector for Observability - AppDynamics enables users to easily and correctly import CIs, Maps and Events from AppDynamics to ServiceNow.



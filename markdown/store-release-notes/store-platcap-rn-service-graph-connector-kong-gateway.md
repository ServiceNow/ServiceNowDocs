---
title: API Service Graph Connector for Kong Gateway release notes
description: Version history for the ServiceNow AI Platform capabilities API Service Graph Connector for Kong Gateway on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-kong-gateway.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# API Service Graph Connector for Kong Gateway release notes

Version history for the ServiceNow AI Platform capabilities API Service Graph Connector for Kong Gateway on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.1 - June 2026**

    Security fix.

-   **Version 2.2.0 - April 2026**
    -   New:
        -   Updated mappings for API policies
        -   Enhanced security controls
        -   Additional metadata stored with cmdb\_key\_value records
-   **Version 2.1.0 - October 2025**

    New: Support for importing Prometheus metrics, including average requests per service.

-   **Version 2.0.1 - July 2025**
    -   Fixed:
        -   Mismatched API count issues
        -   Missing service errors in routes
        -   Improved UI text in the guided setup for the API Service Graph Connector for Kong Gateway
-   **Version 2.0.0 - April 2025**

    Use the ServiceNow Configuration Management Database \(CMDB\) as your normalized source of truth for APIs deployed on Kong Gateway Enterprise. Having your API inventory in the CMDB enables other workflows to be used in managing your API estate, including Security Operations, IT Service Management, IT Operations Management, Integrated Risk, and more. The ServiceNow API Insights workspace also provides a way for teams to interact with the API data so that certain stakeholders can analyze the data without requiring direct access to Kong.

    Configuring this API Service Graph Connector will retrieve the following objects from Kong installations:

    -   Services \(APIs and API Backends\)
    -   Routes \(API Frontends\)
    -   Gateway information
    -   Workspaces
    -   Upstreams and targets
    -   Consumers
    -   Plugins

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)


---
title: API Service Graph Connector for Kong Konnect release notes
description: Version history for API Service Graph Connector for Kong Gateway on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-api-sgc-kong-konnect.html
release: store
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# API Service Graph Connector for Kong Konnect release notes

Version history for API Service Graph Connector for Kong Gateway on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.0 - February 2026**
    -   New:
        -   Added the option to import API usage metrics
        -   Added support for importing control plane groups as gateway records
        -   Added support for importing data plane nodes into a scoped table
-   **Version 1.1.0 - December 2025**
    -   New:
        -   Added mapping of Kong API Dev Portal developers into the API Consumer \[api\_consumer\] table.
        -   Added mapping of Kong API Dev Portal applications, API, and API consumer subscriptions into the API Consumer Access \[api\_consumer\_access\] table.
        -   Mapped Life Cycle Stage and Life Cycle Stage Status attributes in the Managed API \[cmdb\_ci\_managed\_api\] table records.
-   **Version 1.0.0 - October 2025**

    Use the ServiceNow Configuration Management Database \(CMDB\) as your normalized source of truth for APIs deployed in Kong Konnect. Having your API inventory in the CMDB enables other workflows to be used in managing your API estate, including Security Operations, IT Service Management, IT Operations Management, Integrated Risk, and more. The ServiceNow API Insights workspace also provides a way for teams to interact with the API data so that certain stakeholders can analyze the data without requiring direct access to Kong.

    Configuring this API Service Graph Connector will retrieve the following objects from Kong installations:

    -   Services \(APIs and API Backends\)
    -   Routes \(API Frontends\)
    -   Gateway information
    -   Upstreams and targets
    -   Consumers
    -   Plugins


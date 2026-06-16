---
title: Service Graph Connector for SentinelOne release notes
description: Version history for the Service Graph Connector for SentinelOne application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-sentinelone.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for SentinelOne release notes

Version history for the Service Graph Connector for SentinelOne application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - June 2026**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs added to the SentinelOne SGC asset-import, asset tags, and additional-attributes tables: sn\_sec\_sgc\_sntlone\_asset\_import, sn\_sec\_sgc\_sntlone\_asset\_tags, sn\_sec\_sgc\_sntlone\_additonal\_attributes, including a field-specific ACL for first\_discovered to align with ServiceNow Platform Security guidance.
        -   The admin role for the SentinelOne SGC ACLs is replaced by the sgc\_admin role for more role granularity. The sgc\_admin role additionally inherits the sn\_help\_setup\_player role to preserve Guided Setup access.
-   **Version 2.0.1 - December 2024**

    This integration is one of the ServiceNow-developed Service Graph Connectors. The Service Graph Connector for SentinelOne imports hardware assets from the SentinelOne product into your ServiceNow Configuration Management Database \(CMDB\) quickly, seamlessly, and securely. You can use the Guided Setup to help you configure your integration.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)


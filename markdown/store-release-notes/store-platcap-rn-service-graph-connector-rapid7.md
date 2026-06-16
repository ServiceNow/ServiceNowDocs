---
title: Service Graph Connector for Rapid7 release notes
description: Version history for the Service Graph Connector for Rapid7 application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-rapid7.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Rapid7 release notes

Version history for the Service Graph Connector for Rapid7 application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.0 - June 2026**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs added to the Rapid7 SGC asset and asset-import tables: sn\_sec\_sgc\_rapid7\_sgc\_rapid7\_asset and sn\_sec\_sgc\_rapid7\_sgc\_rapid7\_asset\_import, as well as field-specific ACLs for risk\_score, u\_host\_name, u\_tags, and u\_type to align with ServiceNow Platform Security guidance.
        -   The admin role for the Rapid7 SGC ACLs is replaced by the sn\_cmdb\_int\_util.sgc\_admin for more granularity, and the create\_or\_edit\_connection ACL role record has been modified accordingly.
-   **Version 2.0.5 - November 2024**

    Fixed: Issues related to multi-instance functionality that permits you to configure multiple instances of Rapid7 in the Service Graph Connector.

-   **Version 2.0.4 - August 2024**
    -   Changed: Improvements to ServiceNow AI Platform host name processing logic to support cleansing measures that eliminate duplicate configuration items \(CI\)s.
    -   Fixed: Data source improvements so that Test load 20 records' imports a maximum of 20 records.
-   **Version 2.0.2 - June 2024**

    Changed: Modified mapping from CI class 'hardware' to CI class 'unclassed hardware' on the Rapid7 table.

-   **Version 2.0.1 - May 2024**
    -   Fixed:
        -   RemovedCoorelation ID mapping and modified Source, 'Native key' to map to CONNECTIONID and Rapid7ID.
        -   MAC address is mapped to network adapter.
        -   Added the Unique Identifiers column in the Rapid7 Asset table.
-   **Version 2.0.0 - February 2024**

    This integration is part of ServiceNow-developed Service Graph Connectors. The Service Graph Connector for Rapid7 imports hardware assets from the Rapid7 Insightvm product to the ServiceNow CMDB quickly, seamlessly, and securely. You can use the Guided Setup to help you configure your integration.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)


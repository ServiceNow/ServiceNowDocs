---
title: Service Graph Connector for Qualys release notes
description: Version history for the Service Graph Connector for Qualys application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-qualys.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Qualys release notes

Version history for the Service Graph Connector for Qualys application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - June 2026**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs added across 13 Qualys SGC tables: asset details, NIC details, open port details, processor details, service details, software details, asset tags and cloud tags, computer/hardware CI mapping rules, and asset-import staging to align with ServiceNow Platform Security guidance.
        -   The admin role for the Qualys SGC ACLs is replaced by the sgc\_admin role for more granularity. The sgc\_admin role additionally inherits the sn\_help\_setup\_player role to preserve the Guided Setup access.
-   **Version 2.0.9 - October 2025**
    -   Fixed:
        -   Manufacturer details are populated in the Qualys Service Graph Connector \(SGC\) as expected.
        -   The Qualys SGC object\_id is synchronized with other Discovery Sources for Azure Virtual Machines \(VMs\).
        -   Unnecessary attributes retrieved by the Qualys SGC are ignored.
-   **Version 2.0.7 - June 2025**

    Fixed: Removed the Custom attributes field from the service graph connector's import so it no longer causes problems with the payload.

-   **Version 2.0.6 - February 2025**
    -   Fixed:
        -   Network adapter mapping.
        -   Added serial number mapping.
-   **Version 2.0.5 - December 2024**
    -   Fixed:
        -   The hostname is now cleansed before ingesting by Qualys SGC
        -   Addressed performance issue for software ingestion for Global API.
-   **Version 2.0.3 - November 2024**
    -   New: Mapping for Google Cloud Platform \(GCP\) Assets.
    -   Fixed:
        -   Certain information such as open ports, volumes, tags, and software is not imported by default to address memory problems with the Asset Management API for the Qualys Service Graph Connector.
        -   Special characters such as '%' are encoded so if included in the credentials they do not impact Connection tests.
        -   Issues related to multi-instance functionality that permits you to configure multiple instances of Qualys in the Service Graph Connector.
-   **Version 2.0.2 - October 2024**
    -   Fixed:
        -   The relationship between server and virtual machine.
        -   Various unhandled errors.
-   **Version 2.0.1 - August 2024**
    -   Fixed:
        -   You have the option to include or exclude software data for large imports.
        -   Data source improvements so that Test load 20 records' imports a maximum of 20 records.
-   **Version 2.0.0 - February 2024**
    -   This integration is part of ServiceNow-developed Service Graph Connectors. The Service Graph Connector for Qualys imports hardware assets from the Qualys product to the ServiceNow CMDB quickly, seamlessly, and securely. This service graph connector integration was developed by ServiceNow Engineering.
    -   Two Qualys APIs are supported for importing data. Choose one and update a system property to activate it.
        -   Global Asset View API -A CASM license is required.
        -   Qualys Asset Management and Tagging API -A CASM license is not required.


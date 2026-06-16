---
title: Service Graph Connector for Active Directory release notes
description: Version history for the Service Graph Connector for Active Directory application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-active-directory.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Active Directory release notes

Version history for the Service Graph Connector for Active Directory application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - June 2026**
    -   Fixed: The admin role for the Service Graph Connector for Microsoft Active Directory ACLs is replaced with SGC-specific granular admin roles to limit access.
    -   Changed: Updated query ACLs on the Service Graph Connector for Microsoft Active Directory tables to align with internal security directives.
-   **Version 2.0.5 - March 2026**

    Fixed: An issue with Operating System values imported from Active Directory that displayed unexpected special characters.

-   **Version 2.0.4 - June 2025**

    Fixed:The service graph connector is no longer updating configuration items \(CIs\) if there are no changes to them in Active Directory.

-   **Version 2.0.3 - February 2025**

    Fixed: ObjectCategory from Active Directory incorrectly mapped to Category in the computer class.

-   **Version 2.0.2 - November 2024**

    Fixed: Improvements so that you can edit the default values for the LDAP OU Filter. Your edits are no longeroverridden by the scheduled import pre-script.

-   **Version 2.0.1 - June 2024**

    Changed: 'Installed on column' has been added and is mapped to 'LastLogOn Datetime' on the software table of Active Directory.

-   **Version 2.0.0 - February 2024**

    This integration is part of ServiceNow-developed Service Graph Connectors. The Service Graph Connector for Active Directory imports computer and related software details from the Microsoft Active Directory product to the ServiceNow CMDB quickly, seamlessly, and securely. You can use the Guided Setup to help you configure your integration.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)


---
title: Domain separation and Configuration Management Database \(CMDB\)
description: Domain separation is supported in the CMDB. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Configuration Management Database \(CMDB\)

Domain separation is supported in the CMDB. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview of domain separation in CMDB

The following topics provide details about domain separation in Configuration Management \(CMDB\) modules:

-   [Domain separation in CMDB Health](cmdb-health-domain-separation.md)
-   [Domain separation and CMDB Query Builder](domain-separation-groups-query-builder.md)
-   [Domain separation and CMDB Identification and Reconciliation](domain-separation-identification-reconciliation.md)
-   [Domain separation](domain-separation-relationship-formatter-editor.md)
-   [CMDB APIs \(CMDB SDK\)](domain-separation-APIs.md)

**Related topics**  


[Domain separation and Configuration Management Database \(CMDB\)](domain-separation-cmdb.md)


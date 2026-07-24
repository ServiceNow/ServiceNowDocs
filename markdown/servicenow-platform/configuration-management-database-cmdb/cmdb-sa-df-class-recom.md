---
title: CI class recommendations
description: CMDB success advisor analyzes your instance's historical data to recommend which CI classes should be in your Data Foundations scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-recom.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI class recommendations

CMDB success advisor analyzes your instance's historical data to recommend which CI classes should be in your Data Foundations scope.

Recommendations help prioritize classes that provide the most operational value. They are based on:

-   Task activity: Frequency of each CI class appearing in incidents, problems, and changes \(IPC\) over a configurable period \(default 180 days, set in the **sn\_cmdb\_advisor.principal\_class\_suggestion\_period** system property\). For more information about system properties in CMDB success advisor for principal classes, see [Principal classes in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-principal-class.md).

    **Note:** If IPC data is unavailable, classes are ranked by how widely they are used across your CMDB. For new instances with no historical data, a set of default classes is suggested. To configure which classes are suggested on instances with no task history, see [Create the principal class recommendation criteria property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-rec-criteria.md).

-   CI population: Number of CI records in each class.
-   Common Service Data Model \(CSDM\) alignment: Support for service mapping and dependency tracking.

**Note:** You aren't required to accept all recommendations. Recommendations are guidance. Your organization's priorities should drive the final advisor scope selection.

## CI class groups

The **Set principal classes** dialog box organizes available CI classes into groups. The following groups are available for selection:

-   Enterprise architecture
-   IP address management \(IPAM\)
-   IT networking devices
-   Kubernetes
-   Mainframe
-   Middleware applications
-   Recommended
-   SaaS
-   Services and offerings
-   Storage
-   Virtualization infrastructure

**Tip:** The **Recommended** group appears at the top of the list and contains up to 20 CI classes ranked by recent incident, problem, and change \(IPC\) activity. The remaining groups organize classes by technology domain to help you find related classes quickly.


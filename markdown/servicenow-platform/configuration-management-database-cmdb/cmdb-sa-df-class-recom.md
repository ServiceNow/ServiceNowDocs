---
title: CI class recommendations
description: CMDB success advisor analyzes historical data in your instance to recommend which CI classes should be in your Data Foundations scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-recom.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-02-25"
reading_time_minutes: 3
keywords: [CI class recommendations, principal class suggestions, Set principal classes dialog box, recommended CI class groups, incident problem change activity ranking, recommended CI class removals]
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI class recommendations

CMDB success advisor analyzes historical data in your instance to recommend which CI classes should be in your Data Foundations scope.

Recommendations are ranked strictly by task activity: the frequency of each CI class appearing in incidents, problems, and changes \(IPC\) over a configurable period. The default period is 180 days, set in the **sn\_cmdb\_advisor.principal\_class\_suggestion\_period** system property. CI population and Common Service Data Model \(CSDM\) alignment aren't used to rank recommendations. For more information about system properties in CMDB success advisor for principal classes, see [Principal classes in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-principal-class.md).

You aren't required to accept all recommendations. Recommendations are guidance, and your organization's priorities should drive the final advisor scope selection.

**Note:** If fewer than six CI classes have task activity within the suggestion period, CMDB success advisor adds classes from a fixed default list until the minimum is reached. This default list includes Computer \[cmdb\_ci\_computer\], Server \[cmdb\_ci\_server\], Database \[cmdb\_ci\_database\], Cloud Database \[cmdb\_ci\_cloud\_database\], Virtual Machine Instance \[cmdb\_ci\_vm\_instance\], and IP Router \[cmdb\_ci\_ip\_router\]. On instances with no task history at all, all six default classes are recommended. To configure which classes are suggested on instances with no task history, see [Create the principal class recommendation criteria property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-rec-criteria.md).

## CI class groups

The Set principal classes dialog box organizes available CI classes into groups. The following groups are available for selection:

-   AI systems
-   Cloud
-   Databases
-   End user computing devices
-   Enterprise architecture
-   Integrations
-   IP address management \(IPAM\)
-   IT networking devices
-   Kubernetes
-   Mainframe
-   Middleware applications
-   Others
-   Recommended additions
-   Recommended removals
-   SaaS
-   Servers
-   Service instances
-   Services and offerings
-   Storage
-   Virtualization infrastructure

**Tip:** The **Recommended additions** group is displayed at the top of the list and contains up to 20 CI classes ranked by recent incident, problem, and change \(IPC\) activity. The remaining groups organize classes by technology domain to help you find related classes quickly.

## Recommended removals

The **Recommended removals** group is displayed in the Set principal classes dialog box when any of your selected principal classes match the CI class exclusion list. A class matches the list by exact class name, the `cmdb_ci_endpoint_` prefix, or the `_template` suffix. When present, this group is displayed at the top of the list next to **Recommended additions**. If none of your currently selected principal classes match the exclusion list, the group isn't displayed.

The group lists only the currently selected principal classes that match the exclusion list. The check box for each class is already selected to reflect its status as a principal class. Excluded CI classes generally aren't offered for selection in the **Available classes** column. A class is displayed in this group if it was selected as a principal class before being added to the exclusion list. It's also displayed if it was marked as a principal class directly in CI Class Manager.

Clearing the check box for a class in the **Recommended removals** group removes it from your Data Foundations scope when you select **Done**. Selecting the information icon next to the group name displays guidance for reviewing these classes. For the full procedure for updating principal classes, see [Set up the Data Foundations advisor dashboard manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-manual-setup.md).


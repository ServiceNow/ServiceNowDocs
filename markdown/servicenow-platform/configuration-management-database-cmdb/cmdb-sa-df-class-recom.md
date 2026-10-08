---
title: CI class recommendations
description: CMDB success advisor analyzes your instance's CI and task data to recommend which CI classes should be in your Data Foundations scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-recom.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-09-28"
reading_time_minutes: 4
keywords: [CI class recommendations, principal class suggestions, Set principal classes dialog box, recommended CI class groups, incident problem change activity ranking, recommended CI class removals]
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI class recommendations

CMDB success advisor analyzes your instance's CI and task data to recommend which CI classes should be in your Data Foundations scope.

CMDB success advisor ranks each candidate CI class with a weighted score. The score combines three inputs: the class's incident, problem, and change \(IPC\) activity, its CI count, and its category. IPC activity and CI count are both measured within the same suggestion period. The default suggestion period is 180 days, set in the **sn\_cmdb\_advisor.principal\_class\_suggestion\_period** system property. Servers and Cloud classes score highest by category; Services and offerings and Enterprise architecture classes score lowest. IPC activity carries the most weight when any candidate class recorded activity within the suggestion period. On an instance with no IPC activity for any candidate class, the score weights category and CI count only. For more information about system properties in CMDB success advisor for principal classes, see [Principal classes in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-principal-class.md).

Recommendation scores are recalculated once a month by a scheduled job. A recent change in task or CI activity might not affect the Recommended additions group until the next monthly run.

You aren't required to accept all recommendations. Recommendations are guidance, and your organization's priorities should drive the final advisor scope selection.

**Note:** If fewer than six CI classes qualify for a recommendation, CMDB success advisor pads the list with default classes. Padding stops when six recommendations are reached or the default list is exhausted. The default list has five classes: Computer \[cmdb\_ci\_computer\], Server \[cmdb\_ci\_server\], Database \[cmdb\_ci\_database\], Cloud Database \[cmdb\_ci\_cloud\_database\], and Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]. On an instance with no IPC activity for any candidate class, all five default classes are recommended. To configure which classes are suggested on instances with no IPC activity, see [Create the principal class recommendation criteria property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-rec-criteria.md).

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

**Tip:** The **Recommended additions** group is displayed at the top of the list. The group contains up to 20 CI classes ranked by a weighted score of IPC activity, CI count, and category. A CI class that's already a principal class remains in this group, with its check box selected by default. The remaining groups organize classes by technology domain to help you find related classes quickly.

## Recommended removals

The **Recommended removals** group is displayed in the Set principal classes dialog box when any of your selected principal classes match the CI class exclusion list.

A class matches the list by exact class name, the `cmdb_ci_endpoint_` prefix, or the `_template` suffix.

A class matches the list in one of five ways. An exact class name match also excludes every descendant of that class. A specific Level-1 base class matches by exact name only, with no cascading to its subclasses. The list also matches the `cmdb_ci_endpoint_` prefix and the `_template` suffix. Any class outside the native `cmdb_ci` class family also matches, including a customer table, scoped application, or Discovery-populated class.

Because a Level-1 base class match never cascades, other classes in its technology domain group remain available for selection alongside the **Recommended removals** group.

When present, this group is displayed at the top of the list next to **Recommended additions**. If none of your currently selected principal classes match the exclusion list, the group isn't displayed.

The group lists only the currently selected principal classes that match the exclusion list. The check box for each class is already selected to reflect its status as a principal class. Excluded CI classes generally aren't offered for selection in the **Available classes** column. A class is displayed in this group if it was selected as a principal class before being added to the exclusion list. It's also displayed if it was marked as a principal class directly in CI Class Manager.

Clearing the check box for a class in the **Recommended removals** group removes it from your Data Foundations scope when you select **Done**. Selecting the information icon next to the group name displays guidance for reviewing these classes. For the full procedure for updating principal classes, see [Set up the Data Foundations advisor dashboard manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-manual-setup.md).


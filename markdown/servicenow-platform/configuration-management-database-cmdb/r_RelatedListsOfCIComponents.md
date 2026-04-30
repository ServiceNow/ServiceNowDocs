---
title: Related Lists of CI components
description: Related lists in CI records display additional components contained by that CI, such as disk drives on a server and the rules that control the behavior of a network router.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Related Lists of CI components

Related lists in CI records display additional components contained by that CI, such as disk drives on a server and the rules that control the behavior of a network router.

When Discovery runs, the Related List is populated with the components that Discovery finds running on the CI. The CI record might show different lists from scan to scan, depending on whether or not Discovery found the component.

By default, the Related Lists only display those components that are associated with that CI in the CMDB that has been discovered by the last scan. Components that are recorded in the CMDB but are not discovered in a scan, are deemed absent and do not appear in the list.

There are two types of components that appear in the Related List: components that are CIs themselves \(such as hard disks\), and components that are not \(serial numbers and rules\). The default filter condition in the breadcrumbs for components that are CIs is **\[Status\] \[!=\] \[Absent\]**. The filter condition for components that are not CIs is **\[Absent\] \[=\] \[false\]**.

For example, a router can have several Related Lists affected by these filter conditions, including routing rules, disk drives, interfaces, and network adapters. Only those components found during the last Discovery appear in these Related Lists.

## Icons in related lists

Any of the following icons may appear in lists of CI related items.

|Icon|Description|
|----|-----------|
|Currently active incidents|For currently active incidents against this configuration item|
|Currently active problems|For currently active problems against the configuration item|
|Currently active changes|For currently active changes against the configuration item that are not covered in the past, current, pending changes. For example, a request to update the operating system on a server that is currently in progress may display this icon.|
|Recently completed changes|For changes that were recently completed against the configuration item. changes with an "Actual\_end\_date" in the past.|
|Planned changes|For changes that are planned soon against the configuration item. changes with an "Actual start date" in the future.|
|Currently active changes|For currently active changes against the configuration item that have an "Actual start date"|
|Recently completed outages|For outages that were recently completed against the configuration item. outages with an "end" date in the past.|
|Planned outages|For outages that are planned soon against the configuration item. outages with a "begin" date in the future.|
|Currently active outages|For currently active outages against the configuration item that have a "begin" date in the past and no "end" date|
|Issues with downstream CI|This will only show up in the Tree view and indicates that a configuration item that is downstream has at least one of the above issues against it.|

The system looks five calendar days into the past and seven calendar days into the future when looking at recent outages and changes.

-   **[Teams related list](../concept/teams-related-list.md#)**  
The Teams related list associates a user group to a CI based on group type, providing flexibility in tracking the different types of groups assigned to a CI. The Teams related list appears on CI forms for CIs of the Service \[cmdb\_ci\_service\] class and its descendent classes such as the Service Instance \[cmdb\_ci\_service\_auto\] class.

**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](r_CMDBRecordTypes.md)

[Create a CI class](../task/t_CreateCIType.md)

[Reclassify a CI](../task/t_ManuallyReclassifyCI.md)

[Delete CIs](../task/delete-class-records-ci-class-mgr.md)

[View and edit class definitions and metadata](../task/t_ViewTableDefinitions.md)

[Update class list in the Principal Class filter](../task/update-principal-class-filter.md)


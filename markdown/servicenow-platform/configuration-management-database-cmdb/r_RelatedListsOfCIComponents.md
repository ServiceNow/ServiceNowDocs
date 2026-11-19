---
title: Related Lists of CI components
description: Related lists in CI records display additional components contained by that CI, such as disk drives on a server and the rules that control the behavior of a network router.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/r\_RelatedListsOfCIComponents.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [CMDB classifications and class dependency, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Related Lists of CI components

Related lists in CI records display additional components contained by that CI, such as disk drives on a server and the rules that control the behavior of a network router.

When Discovery runs, the Related List is populated with the components that Discovery finds running on the CI. The CI record might show different lists from scan to scan, depending on whether or not Discovery found the component.

By default, the Related Lists only display those components that are associated with that CI in the CMDB that has been discovered by the last scan. Components that are recorded in the CMDB but are not discovered in a scan, are deemed absent and do not appear in the list.

There are two types of components that appear in the Related List: components that are CIs themselves \(such as hard disks\), and components that are not \(serial numbers and rules\). The default filter condition in the breadcrumbs for components that are CIs is **\[Status\] \[!=\] \[Absent\]**. The filter condition for components that are not CIs is **\[Absent\] \[=\] \[false\]**.

For example, a router can have several Related Lists affected by these filter conditions, including routing rules, disk drives, interfaces, and network adapters. Only those components found during the last Discovery appear in these Related Lists.

## Icons in related lists

Any of the following icons may appear in lists of CI related items.

<table id="simpletable_wf2_pjp_pgb"><tbody><tr><td>

\[Omitted image "Incidents.png"\] Alt text: Currently active incidents.

</td><td>

For currently active incidents against this configuration item

</td></tr><tr><td>

\[Omitted image "Problems.png"\] Alt text: Currently active problems.

</td><td>

For currently active problems against the configuration item

</td></tr><tr><td>

\[Omitted image "Changes.png"\] Alt text: Currently active changes.

</td><td>

For currently active changes against the configuration item that are not covered in the past, current, pending changes. For example, a request to update the operating system on a server that is currently in progress may display this icon.

</td></tr><tr><td>

\[Omitted image "ChangePast.png"\] Alt text: Recently completed changes.

</td><td>

For changes that were recently completed against the configuration item. changes with an "Actual\_end\_date" in the past.

</td></tr><tr><td>

\[Omitted image "ChangePlanned.png"\] Alt text: Planned changes.

</td><td>

For changes that are planned soon against the configuration item. changes with an "Actual start date" in the future.

</td></tr><tr><td>

\[Omitted image "ChangePresent.png"\] Alt text: Currently active changes.

</td><td>

For currently active changes against the configuration item that have an "Actual start date"

</td></tr><tr><td>

\[Omitted image "OutagesPast.png"\] Alt text: Recently completed outages.

</td><td>

For outages that were recently completed against the configuration item. outages with an "end" date in the past.

</td></tr><tr><td>

\[Omitted image "OutagesPlanned.png"\] Alt text: Planned outages.

</td><td>

For outages that are planned soon against the configuration item. outages with a "begin" date in the future.

</td></tr><tr><td>

\[Omitted image "OutagesPresent.png"\] Alt text: Currently active outages.

</td><td>

For currently active outages against the configuration item that have a "begin" date in the past and no "end" date

</td></tr><tr><td>

\[Omitted image "Issues.png"\] Alt text: Issues with downstream CI.

</td><td>

This will only show up in the Tree view and indicates that a configuration item that is downstream has at least one of the above issues against it.

</td></tr></tbody>
</table>The system looks five calendar days into the past and seven calendar days into the future when looking at recent outages and changes.

-   **[Teams related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/teams-related-list.md)**  
The Teams related list associates a user group to a CI based on group type, providing flexibility in tracking the different types of groups assigned to a CI. The Teams related list appears on CI forms for CIs of the Service \[cmdb\_ci\_service\] class and its descendent classes such as the Service Instance \[cmdb\_ci\_service\_auto\] class.

**Parent Topic:**[CMDB classifications and class dependency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management]()

[CMDB record types]()

[Create a CI class]()

[Reclassify a CI]()

[Delete CIs]()

[View and edit class definitions and metadata]()

[Principal Class]()

[Update the list of classes in the Principal Class filter]()


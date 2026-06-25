---
title: Understand Service Maps
description: Service maps show active alerts for CIs and the relationships between CIs. By viewing this information, you can better understand the source of alerts and take remediation steps. The service map is available for all application services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/Understand-Service-Maps.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Understand Service Maps

Service maps show active alerts for CIs and the relationships between CIs. By viewing this information, you can better understand the source of alerts and take remediation steps. The service map is available for all application services.

About Service Maps

A service map shows alerts with impacted CIs and CI interdependencies. For example, changes to a connection between a host and hypervisor appear on the service map. As service map definitions change, the service map, alert, and impact information updates accordingly. From the Quebec release, there is enhanced visibility. When the alert is bound to the entry point, the service map identifies an entry point problem.

**Note:** Alerts will not be displayed for the entry points on the service map.

You can open a service map from these places:

-   From the Application services list, you can view service maps for application services.
-   From the Monitored services list, you can view service maps for monitored services.

The following icons are used in service maps. The icon shapes are slightly different for application services.

<table id="table_pvb_n4w_n4b"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\(\[Omitted image "EventManagementAppSvrIcon.png"\] Alt text: Application server icon.\)

</td><td>

Represents applications such as Microsoft IIS or SQL servers.

</td></tr><tr><td>

\(\[Omitted image "EventManagementCallCntrIcon.png"\] Alt text: Call server icon.\)

</td><td>

Represents physical and VM computers and servers.

</td></tr><tr><td>

\(\[Omitted image "EventManagementEntryPtIcon.png"\] Alt text: Entry point icon.\)

</td><td>

Represents the network starting point. For example, Layer 3 devices appear toward the top of the map, and connected software and services appear near the end of the map.

</td></tr><tr><td>

\(\[Omitted image "EM\_RedundancyArrowIcon.png"\] Alt text: Redundancy box icon.\)

</td><td>

Shows the number of redundant CIs.

</td></tr><tr><td>

\(\[Omitted image "EventManagementLBIcon.png"\] Alt text: Load balancer icon.\)

</td><td>

Shows the workload between machines.

</td></tr><tr><td>

\(\[Omitted image "EventManagementArrow.png"\] Alt text: Gray connector icon.\)

</td><td>

The gray connector shows a relationship between CIs.

</td></tr><tr><td>

\(\[Omitted image "EventManagementUnselectBoxNoSeverityIcon.png"\] Alt text: CI with no active alerts box icon.\)

</td><td>

Each CI with no active alerts box represents a network CI. A gray box represents a CI with no active alerts. Information about the CI is hidden.

</td></tr><tr><td>

\(\[Omitted image "EMRedundancyBoxIcon.png"\] Alt text: Redundancy box icon.\)

</td><td>

Hides multiple CIs that are designated as redundant.

</td></tr><tr><td>

\(\[Omitted image "EventManagementUnselectBoxIcon.png"\] Alt text: Box with orange severity color icon.\)

</td><td>

An impacted CI displays the color that represents the severity of the alert associated with the CI.-   **Critical \(red\)**: Immediate action is required. The resource is either not functional or critical problems are imminent.
-   **Major \(orange\)**: Major functionality is severely impaired or performance has degraded.
-   **Minor \(yellow\)**: Partial, non-critical loss of functionality or performance degradation occurred.
-   **Warning \(blue\)**: Attention is required, even though the resource is still functional.
-   **OK \(green\)**: An alert is created. The resource is still functional.
-   **No color**: No active alerts.

</td></tr><tr><td>

\(\[Omitted image "EventManagementStorageIcon.png"\] Alt text: Storage icon.\)

</td><td>

Represents a fiber channel, hard drives, or other data storage devices.

</td></tr><tr><td>

\(\[Omitted image "EventManagementWebSvcIcon.png"\] Alt text: Web server icon.\)

</td><td>

Represents related web services for the network such as NGINX or JBoss web server.

</td></tr></tbody>
</table>**Note:** Session timeout settings don't apply to this screen. The session remains connected, even when there is no human interaction. If this setting is a concern, either log out or close the active tab in the browser.

**Related topics**  


[Alert impact calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/c_EMImpactCalculation.md)

[View an alert impact on CIs in a service map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMViewTopology.md)


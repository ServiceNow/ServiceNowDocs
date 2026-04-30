---
title: Exploring Service Owner Workspace
description: The Service Owner Workspace provides portfolio and service owners with an integrated and graphically intuitive user experience to manage and monitor portfolios and services.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Service Owner Workspace, IT Service Management]
---

# Exploring Service Owner Workspace

The Service Owner Workspace provides portfolio and service owners with an integrated and graphically intuitive user experience to manage and monitor portfolios and services.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Navigate](../image/SOWExploreBanner2.png "Navigate")

</td></tr></tbody>
</table>## How Service Owner Workspace works

Service Owner Workspace is a read only user interface driven by Service Portfolio Management Premium plugin \(com.snc.spm\) functionality. Service Portfolio Management Premium collects service offering metrics and rolls these calculations up to parent services and taxonomy nodes for performance scores and other metrics viewed via Service Owner Workspace. Performance Analytics indicators capture this data and Service Portfolio Management Premium uses the Performance Analytics data as input metrics to calculate a service offering performance score. These indicators can also track data about a service offering without including it in the offering performance score.

Users can create new metric definitions or use the metric definitions provided in the base system application. Assign metrics to service portfolios and define weights for every metric at an offering level to provide more granularity into performance. Daily jobs then calculate the offering performance score and roll the scores up to the service and other associated taxonomy nodes to monitor in Service Owner Workspace.

## Service Owner Workspace browser requirements

ServiceNow workspaces do not support mobile devices, and, starting with the Orlando release, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge-Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US). If you're using New York or an earlier release and you're using Internet Explorer 11 or Microsoft Edge with any workspace, such as ServiceNow® CSM Agent Workspace or ServiceNow® Vendor Manager Workspace, you must migrate to a newer browser before you upgrade to at least the Orlando release. See the [Internet Explorer 11 Performance \[KB0683275\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) article in the Now Support Knowledge Base for more information.

## Service Owner Workspace overview

Manage and monitor your services with premium features. View service offering details in the workspace:

![Service offering details](../image/ServiceOwnerWorkspaceOverviewTab.png "Service offering details")

<table id="table_tpw_tlf_1kb"><thead><tr><th>

Number

</th><th>

Agent Workspace feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Tabs

</td><td>

The multi-tab interface enables you to easily navigate between service-related records.-   All services open in the **Services Home** tab.
-   Associated service offering details open in subtabs. Drill down to the lowest hierarchical level to view details about all related service offerings.

</td></tr><tr><td>

2

</td><td>

Form header

</td><td>

The form header provides you with a quick summary of the service offering and an associated performance score. Estimated spend details appear in the form header when available.

</td></tr><tr><td>

3

</td><td>

Related items menu

</td><td>

Service-related information is available to view in the related items menu. Click an item to see the related information.

</td></tr><tr><td>

4

</td><td>

Ribbon

</td><td>

Ribbon components display service offering performance score, customer satisfaction, and total subscriber trends. Estimated spend data is also viewable when available.

</td></tr><tr><td>

5

</td><td>

Form pane

</td><td>

Additional service-related information is displayed as you scroll down the page and drill deeper into the data. Information includes, service-offering availability, breached SLAs, customer satisfaction, stability, and activity.

</td></tr><tr><td>

6

</td><td>

Contextual side panel details

</td><td>

Unique data details are displayed. Click icons to display **Outages**, **Critical Incidents**, **Change Requests**, or **Attachments** details.

</td></tr><tr><td>

7

</td><td>

Contextual side panel

</td><td>

The contextual side panel displays unique data depending on which icon you select.

</td></tr></tbody>
</table>## Integration with Common Service Data Model

Improve your measurement and evaluation by using services and offering references on multiple IT Service Management task forms, including:

-   Problem
-   Change
-   Continual Improvement Management
-   Incident

Directly reference a service offering as the target of a problem, change, or incident for consistency with the Common Service Data Model \(CSDM\). The system filters available offerings based on the service selected.

View and define the service model **Model ID** reference field on the Service and Offering forms to integrate with the CSDM.


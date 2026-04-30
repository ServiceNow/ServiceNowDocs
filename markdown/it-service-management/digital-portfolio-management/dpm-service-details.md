---
title: View service and service offering details
description: View information about services and service offerings that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the life-cycle phase information in tabs — Plan, Build, Run, and Info.
locale: en-US
release: yokohama
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Digital Portfolio Management life-cycle management, Exploring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# View service and service offering details

View information about services and service offerings that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the life-cycle phase information in tabs — Plan, Build, Run, and Info.

## Status of services and service offerings

When viewing the service and service offering details in DPM, the **Phase** and **Status** of each item is listed on the workspace view and on the list view.

When viewing details of a service or service offering that's retired, an alert banner along the top of the workspace view states that it's retired. In the list view, the Phase is listed as **Retired**, the life-cycle stage is **End of Life**, and the life-cycle stage status is **Retired**.

**Important:** If your organization transitioned from the traditional Service Portfolio Management fields to the CSDM life-cycle fields, then the field names differ from this document. For more information, see [Apply the CSDM guidelines to Digital Portfolio Management](../reference/dpm-csdm.md).

**Important:** For the Yokohama release and later, the labels for the items in the \[cmdb\_ci\_service\_technical\] table and \[service\_offering\] table are Technology Management Service and Technology Management Service Offering, respectively. Prior to the Yokohama release, the labels are Technical Service and Technical Service Offering.

Services and service offerings display information in DPM via the Plan, Build, Run, and Info tabs. If your organization opts to inactivate one or more of the tabs, then the inactivated tabs aren't visible to you. For example, if your organization doesn't work on planning activities and they inactivate the Plan tab, then the Plan tab isn't visible for you. For more information on how Admins can hide or show tabs, see [Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md).

Keep in mind that what you are able to see in DPM depends on what your product license permits from the source application. See [Digital Portfolio Management related applications and data sources](../reference/dpm-related-products.md) for the required installations and plugins to see each data element.

**Note:** The Strategic Planning Workspace \(formerly known as Alignment Planner Workspace\) is a pro version. The Portfolio Planning Workspace is available for users with a Strategic Portfolio Management \(SPM\) standard license.

## Plan tab

<table id="table_xzk_zzp_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Roadmap and backlog**

</td><td>

-   When selected, see roadmap details in the Strategic Planning or Portfolio Planning Workspace.
-   When selected, see backlog information in a shared service support planning backlog list.

</td></tr><tr><td>

**Summary**

</td><td>

Summary cards for the service or service offering. You can select each card to go to a list of the items.

-   Total ideas
-   Approved demands
-   Project starting in the next 30 days
-   New improvement initiatives

</td></tr><tr><td>

**Demands**

</td><td>

Total number of demands on the service or service offering. The number of demands is in a gray box.

 You can select a demand record to view its details, including tasks, stakeholders, requirements, risks, and more.

 You can also create demands on your service or service offerings. See [Create demand from Digital Portfolio Management](../task/dpm-create-demand-initiatives.md).

</td></tr></tbody>
</table>## Build tab

<table id="table_kml_hwp_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Roadmap**

</td><td>

When selected, view roadmap details in the Strategic Planning or Portfolio Planning Workspace.

</td></tr><tr><td>

**Projects**

</td><td>

Project information related to the service or service offering.

-   A donut graph shows the active projects by current status. You can hover over each status of the donut to see its number of projects and percentage. You can also select each status to access a list of the projects records in that status.
-   A bar graph shows projects overdue by month. You can hover over each status of the bar graph to see the month, year, and the number of projects. You can also select each bar to access a list of the projects for that month.
-   A set of cards enable you to select the number \(count\) to see a list of projects for the service or service offering.
    -   Projects with status work in progress
    -   Projects with missed key milestones
    -   Projects with critical issues

 **Active projects**

 Total number of active projects on the service or service offering. The number of active projects is in a gray box. Select an active project record to view its details, including project tasks, agile phase, stories, epics, and more.

</td></tr><tr><td>

**Changes**

</td><td>

**Change graphs**

 -   A donut graph shows the changes by status:
    -   New
    -   Assess
    -   Authorize
    -   Scheduled
    -   Implement
    -   Review
    -   Closed
    -   Canceled
-   A bar graph shows changes overdue by month.
-   A spark line graph shows upcoming changes this week.
-   A bar graph shows the change backlog growth in the last 30 days.

</td></tr><tr><td>

**Improvement initiatives**

</td><td>

-   A donut graph shows the changes by state:
    -   New
    -   In Progress
    -   Monitor/Review
    -   Closed
-   A bar graph shows the improvement initiatives overdue by month.
-   A card enables you to select the number \(count\) of overdue tasks for the service or service offering.
-   A bar graph shows the improvement initiatives that were closed in the last 30 days.

 **Active improvement initiatives**

 The total number of active improvement initiatives on the service or service offering. The number of active improvement initiatives is in the gray box. You can select an active improvement initiative for its details, including its Continual Improvement Management \(CIM\) phase, CIM tasks, impacted key performance indicators \(KPIs\), and approvers.

</td></tr></tbody>
</table>## Run tab

Some of the fields on the Run tab are different for services and for service offerings, as noted in the following table. See [KB1637474](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637474) for more information about KPI results on DPM pages.

<table id="table_csx_qxp_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Service performance** or **Offering performance**

</td><td>

The Performance snapshot KPI group that comes with the base system. The indicators typically show availability, open incidents, and new requests. Each indicator has an information icon \(![Information icon.](../image/information-icon.jpg)\) that when selected, provides a tooltip description for that indicator.

 For information on KPIs that come with the base system, see [KPI groups installed with Digital Portfolio Management](../reference/dpm-kpi-groups-oob.md).

 Admins can modify KPI groups, create KPIs, and create KPI group mappings so you may see more than the Performance snapshot on the Run tab. For information, see [Create KPI groups and mappings in Digital Portfolio Management](../task/dpm-create-kpi-groups.md).

 For information on configuring KPIs, see [Configure KPIs in Digital Portfolio Management with service availability example](../task/dpm-configure-kpi-availability.md).

</td></tr><tr><td>

**Offering breakdown** \(services only\)

</td><td>

List of the offering breakdowns for the service, including each offering's:

-   Availability
-   Open incidents
-   Incidents not updated for 5 days
-   New requests

</td></tr><tr><td>

**Application service dependencies** \(service offerings only\)

</td><td>

List of the application services that the service offering depends on. The number of application services is in a gray box. You can select an application service for its details. For more information, see [View application service details](dpm-app-service-details.md).

</td></tr><tr><td>

**Commitments** \(service offerings only\)

</td><td>

Information about the service offering availability commitments such as the commitment name, type, and target.

</td></tr><tr><td>

**SLA commitments** \(service offerings only\)

</td><td>

Information about the service level agreement \(SLA\) commitments for the service offering.

</td></tr></tbody>
</table>## Info tab

The Info tab provides general information about the service or service offering. Some of the fields are different for services and for service offerings, as noted in the following table. You can't edit the fields in the Info tab.

<table id="table_j5g_zxp_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Service description** or **Service offering description**

</td><td>

Description of the service or the service offering.

</td></tr><tr><td>

**General Info**

</td><td>

General information about the service or the service offering.

-   Service portfolio
-   Taxonomy node
-   Service classification \(business or technical\)
-   Phase and Status \(if using the Service Portfolio Management fields\) or
-   Stage and Status \(if using the CSDM life-cycle fields\)
-   Consumer type
-   Last review date
-   Start and end dates

</td></tr><tr><td>

**Personal portfolios**

</td><td>

The personal portfolios for the service or offering. The number of personal portfolios is in a gray box. Select a personal portfolio for its details.

</td></tr><tr><td>

**Subscribers**

</td><td>

General information about the subscribers on the service or service offering. You can select each card for detailed subscriber information on the following:

-   Locations
-   Departments
-   Groups
-   Companies
-   Individual users

</td></tr><tr><td>

**Price** \(service offerings only\)

</td><td>

General price information about the service offering, like price model, unit, cost, and description.

</td></tr><tr><td>

**Offering commitments** \(service offerings only\)

</td><td>

The service commitment for the offering, for example, 95% 24x7. The number of the commitments is in a gray box. Select a commitment for its details.

</td></tr><tr><td>

**Offerings** \(services only\)

</td><td>

The offerings for the service. The number of service offerings is in a gray box. Select an offering for details.

</td></tr><tr><td>

**Service scope** \(services only\)

</td><td>

-   The business case criticality for the service. Criticality levels are:
    1.  Most critical
    2.  Somewhat critical
    3.  Less critical
    4.  Not critical
-   The business capabilities for the service. The number of business capabilities is in a gray box. Select a business capability for details.

</td></tr><tr><td>

**Service Contracts** \(for services\) or **Contracts** \(for service offerings\)

</td><td>

The list of contracts for the service or the service offering. If available, you can select a contract for its details.

</td></tr></tbody>
</table>## Needs attention panel icons

The Needs attention panel includes the following icons for services and service offerings:

-   Needs attention icon \(![Needs attention icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to show or hide the Needs attention panel. For information on needs attention values, see [Work with Needs attention panels in Digital Portfolio Management](dpm-needs-attn-panels.md).
-   Contacts icon \(![Contacts icon.](../image/contacts.png)\) to view team members and teams for the record.
-   Catalog items icon \(![Catalog items icon.](../image/catalog-items.png)\) to search for catalog items on a service or a service offering record.
-   Knowledge articles icon \(![Knowledge articles icon.](../image/dpm-kb-icon.png)\) to search for related knowledge articles.
-   Attachments icon \(![Attachments icon.](../image/attachment.png)\) to view and add attachments to the record.

**Related topics**  


[Work with Needs attention panels in Digital Portfolio Management](dpm-needs-attn-panels.md)


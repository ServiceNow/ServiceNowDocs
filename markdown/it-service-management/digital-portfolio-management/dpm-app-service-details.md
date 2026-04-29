---
title: View service instance details
description: View information about service instances that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the service instance life-cycle phase information in tabs, primarily Run and Info. The Risk tab displays when you have the Technology Portfolio Management plugin \[sn\_apm\_tpm\] installed.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Life-cycle management, Explore, Digital Portfolio Management, IT Service Management]
---

# View service instance details

View information about service instances that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the service instance life-cycle phase information in tabs, primarily Run and Info. The Risk tab displays when you have the Technology Portfolio Management plugin \[sn\_apm\_tpm\] installed.

As you view the following tables, keep in mind that what you are able to see in DPM depends on what your product license permits from the source application. See [Digital Portfolio Management related applications and data sources](../reference/dpm-related-products.md) for the required installs and plugins to see each data element.

## KPI groups for service instances

If your organization uses the enterprise portfolio module with the latest enterprise portfolio tables, then an service instance rolls up to its related business application. This enables you to create a portfolio with business applications that will have the service instances. You could also create a separate portfolio for service instances which contains the application service. In both cases, the service instances inherit KPI groups from both portfolios.

-   An service instance can be in a business application portfolio because:
    -   Service instances roll up to business applications.
    -   Run data from the service instance shows at the business application level.
-   An service instance can be added to an application-type portfolio.

Incidents, problems, and changes can be added to an service instance's Impacted services or the Affected CIs related list. After this addition, you see the rolled up data in the following areas when you:

-   Select **View details** on any affected solution page.
-   View the **Run** tab of any solution page to view the KPI indicators.
-   View the KPIs and Needs attention panels of the affected business applications.

You can also see the rolled up data in the following areas:

-   Enterprise application portfolios
-   Enterprise service instance portfolios
-   Any business application or service instance that is added to your personal portfolios

Since service instances can be in two different types of portfolios, the service instance inherits KPI groups from two different places. See the table for how KPI groups work in the following use cases.

<table id="table_e25_ll4_zzb"><thead><tr><th>

View

</th><th>

KPIs shown

</th><th>

Conditions

</th></tr></thead><tbody><tr><td>

Enterprise portfolio service instance preview

</td><td>

The inherited KPI groups from the enterprise portfolio.

 If there isn't an enterprise portfolio KPI group, then an empty state is shown.

</td><td>

The service instance enterprise portfolio type contains service instances and isn't linked to a business application type.

 You can link an service instance to a business application enterprise portfolio type using cmdb\_rel\_ci. The parent should be a business application and the supporting item should be an service instance. The required relationship is **Consumes: Consumed by**.

</td></tr><tr><td>

Service instances detail page \(Run tab\) from an enterprise portfolio

</td><td>

-   All inherited KPI groups display, regardless from where you navigated.
-   Also, the KPI groups added directly to that service instance display.

</td><td>

Service instance is added and its parent enterprise portfolio is mapped with its KPI group type.

</td></tr><tr><td>

Service instance from a personal portfolio or from a list

</td><td>

All KPI groups

</td><td>

No conditions.

</td></tr></tbody>
</table>## Run tab

See [KB1637474](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637474) for more information about KPI results on DPM pages.

<table id="table_xzk_zzp_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Service instance performance**

</td><td>

Performance details about the service instance. You can select the graphs and cards for each section to view more details. Each indicator has an information icon \(![Information icon.](../image/information-icon.jpg)\) that when selected, provides a tooltip description for that indicator.The following KPI groups and indicators are in this section.

-   **Portfolio success metrics**
    -   Availability
    -   Incidents with a breached service level agreement \(SLA\)
    -   Incidents caused by changes
    -   Successful changes
-   **Business application performance**
    -   Number of incidents
    -   Number of problems
    -   Number of changes
-   **Service health**
    -   Critical incidents
    -   Critical alerts
    -   Closed changes
-   **Service impact**
    -   Impacted rate
    -   Critical severity over time
-   **Alert trends**
    -   Incidents caused by alerts
    -   Alerts by severity
-   **Availability insights**
    -   Availability
    -   Unplanned outages
    -   Average outage duration

</td></tr><tr><td>

**Commitments**

</td><td>

Commitment data for the service instance. You can select a commitment to view its details.

</td></tr><tr><td>

**Service reliability management** \(with sn\_sow\_srm plugin installed\)

</td><td>

Service reliability management information data for the service instance. To see reliability indicators, the sn\_sow\_srm plugin must be installed. You can select a reliability indicator to view its details.

</td></tr><tr><td>

**Offerings that depend on this service instance**

</td><td>

A list of the offerings that depend on this service instance. The number of offerings is in a gray box. Select an offering for its details.

 For information on offering details, see [View service and service offering details](dpm-service-details.md).

</td></tr></tbody>
</table>## Risk tab

To see the Risk tab, you must have the Technology Portfolio Management plugin \[sn\_apm\_tpm\] installed. The Risk tab displays the Technology Lifecycle Risk using donut reports and lists for service instances software and hardware models.

**Note:** The Technology Portfolio Management plugin \[sn\_apm\_tpm\] has two dependency plugins:

-   Application Portfolio Management \[com.snc.apn\]
-   Software Asset Management \[com.snc.sams\]

## Info tab

The Info tab provides general information about the service instance. You can't edit the fields in the Info tab.

<table id="table_alc_bcq_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Service instance description**

</td><td>

Description about the service instance.

</td></tr><tr><td>

**General Info**

</td><td>

General information about the service instance.-   Business criticality
-   Version
-   Environment
-   Operational status
-   Managed by group
-   Support group
-   Approval group
-   Change group

</td></tr><tr><td>

**Personal portfolios**

</td><td>

The personal portfolios for the service instance. The number of personal portfolios is in a gray box. Select a personal portfolio for its details.

</td></tr><tr><td>

**Service instance commitments**

</td><td>

The service commitments for the service instance. The number of commitments is in a gray box. Select a commitment for its details.

</td></tr><tr><td>

**Software and hardware models**

</td><td>

The software and hardware models for the service instance. The number of each is in a gray box. Select a software or hardware model for its details.

</td></tr><tr><td>

**Relationships**

</td><td>

The configuration items \(CIs\) for the service instance. The number of CIs is in a gray box. Select a CI for its details.

</td></tr></tbody>
</table>## Needs attention panel icons

The Needs attention panel includes the following icons for service instances:

-   Needs attention icon \(![Needs attention icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to show or hide the Needs attention panel.
-   Contacts icon \(![Contacts icon.](../image/contacts.png)\) to view team members and teams for the record.
-   Attachments icon \(![Attachments icon.](../image/attachment.png)\) to view and add attachments to the record.

**Related topics**  


[Enterprise portfolios](dpm-enterprise-portfolios.md)

[Create enterprise portfolios in Digital Portfolio Management](../task/dpm-create-enterprise-portfolios.md)

[Work with Needs attention panels in Digital Portfolio Management](dpm-needs-attn-panels.md)


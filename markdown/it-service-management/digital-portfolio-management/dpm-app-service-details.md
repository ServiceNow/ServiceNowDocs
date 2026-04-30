---
title: View application service details
description: View information about application services that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the application service life-cycle phase information in tabs, primarily Run and Info. The Risk tab displays when you have the Technology Portfolio Management plugin \[sn\_apm\_tpm\] installed.
locale: en-US
release: yokohama
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Digital Portfolio Management life-cycle management, Exploring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# View application service details

View information about application services that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the application service life-cycle phase information in tabs, primarily Run and Info. The Risk tab displays when you have the Technology Portfolio Management plugin \[sn\_apm\_tpm\] installed.

As you view the following tables, keep in mind that what you are able to see in DPM depends on what your product license permits from the source application. See [Digital Portfolio Management related applications and data sources](../reference/dpm-related-products.md) for the required installs and plugins to see each data element.

## KPI groups for application services

If your organization uses the enterprise portfolio module with the latest enterprise portfolio tables, then an application service rolls up to its related business application. This enables you to create a portfolio with business applications that will have the application services. You could also create a separate portfolio for application services which contains the application service. In both cases, the application services inherit KPI groups from both portfolios.

-   An application service can be in a business application portfolio because:
    -   Application services roll up to business applications.
    -   Run data from the application service shows at the business application level.
-   An application service can be added to an application-type portfolio.

Incidents, problems, and changes can be added to an application service's Impacted services or the Affected CIs related list. After this addition, you see the rolled up data in the following areas when you:

-   Select **View details** on any affected solution page.
-   View the **Run** tab of any solution page to view the KPI indicators.
-   View the KPIs and Needs attention panels of the affected business applications.

You can also see the rolled up data in the following areas:

-   Enterprise application portfolios
-   Enterprise application service portfolios
-   Any business application or application service that is added to your personal portfolios

Since application services can be in two different types of portfolios, the application service inherits KPI groups from two different places. See the table for how KPI groups work in the following use cases.

<table id="table_e25_ll4_zzb"><thead><tr><th>

View

</th><th>

KPIs shown

</th><th>

Conditions

</th></tr></thead><tbody><tr><td>

Enterprise portfolio application service preview

</td><td>

The inherited KPI groups from the enterprise portfolio.

 If there isn't an enterprise portfolio KPI group, then an empty state is shown.

</td><td>

The application service enterprise portfolio type contains application services and isn't linked to a business application type.

 You can link an application service to a business application enterprise portfolio type using cmdb\_rel\_ci. The parent should be a business application and the supporting item should be an application service. The required relationship is **Consumes: Consumed by**.

</td></tr><tr><td>

Application services detail page \(Run tab\) from an enterprise portfolio

</td><td>

-   All inherited KPI groups display, regardless from where you navigated.
-   Also, the KPI groups added directly to that application service display.

</td><td>

Application service is added and its parent enterprise portfolio is mapped with its KPI group type.

</td></tr><tr><td>

Application service from a personal portfolio or from a list

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

**Application service performance**

</td><td>

Performance details about the application service. You can select the graphs and cards for each section to view more details. Each indicator has an information icon \(![Information icon.](../image/information-icon.jpg)\) that when selected, provides a tooltip description for that indicator.The following KPI groups and indicators are in this section.

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

Commitment data for the application service. You can select a commitment to view its details.

</td></tr><tr><td>

**Service reliability management** \(with sn\_sow\_srm plugin installed\)

</td><td>

Service reliability management information data for the application service. To see reliability indicators, the sn\_sow\_srm plugin must be installed. You can select a reliability indicator to view its details.

</td></tr><tr><td>

**Offerings that depend on this application service**

</td><td>

A list of the offerings that depend on this application service. The number of offerings is in a gray box. Select an offering for its details.

 For information on offering details, see [View service and service offering details](dpm-service-details.md).

</td></tr></tbody>
</table>## Risk tab

To see the Risk tab, you must have the Technology Portfolio Management plugin \[sn\_apm\_tpm\] installed. The Risk tab displays the Technology Lifecycle Risk using donut reports and lists for application services software and hardware models.

**Note:** The Technology Portfolio Management plugin \[sn\_apm\_tpm\] has two dependency plugins:

-   Application Portfolio Management \[com.snc.apn\]
-   Software Asset Management \[com.snc.sams\]

## Info tab

The Info tab provides general information about the application service. You can't edit the fields in the Info tab.

<table id="table_alc_bcq_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Application service description**

</td><td>

Description about the application service.

</td></tr><tr><td>

**General Info**

</td><td>

General information about the application service.-   Business criticality
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

The personal portfolios for the application service. The number of personal portfolios is in a gray box. Select a personal portfolio for its details.

</td></tr><tr><td>

**Application service commitments**

</td><td>

The service commitments for the application service. The number of commitments is in a gray box. Select a commitment for its details.

</td></tr><tr><td>

**Software and hardware models**

</td><td>

The software and hardware models for the application service. The number of each is in a gray box. Select a software or hardware model for its details.

</td></tr><tr><td>

**Relationships**

</td><td>

The configuration items \(CIs\) for the application service. The number of CIs is in a gray box. Select a CI for its details.

</td></tr></tbody>
</table>## Needs attention panel icons

The Needs attention panel includes the following icons for application services:

-   Needs attention icon \(![Needs attention icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to show or hide the Needs attention panel.
-   Contacts icon \(![Contacts icon.](../image/contacts.png)\) to view team members and teams for the record.
-   Attachments icon \(![Attachments icon.](../image/attachment.png)\) to view and add attachments to the record.

**Related topics**  


[Enterprise portfolios](dpm-enterprise-portfolios.md)

[Create enterprise portfolios in Digital Portfolio Management](../task/dpm-create-enterprise-portfolios.md)

[Work with Needs attention panels in Digital Portfolio Management](dpm-needs-attn-panels.md)


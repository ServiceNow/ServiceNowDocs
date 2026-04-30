---
title: Digital Portfolio Management related applications and data sources
description: Digital Portfolio Management \(DPM\) enables you to use related applications to view and edit service details in the plan-build-run life cycle. All related applications are optional, so they aren't required to use the DPM experience.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Digital Portfolio Management reference, Digital Portfolio Management, IT Service Management]
---

# Digital Portfolio Management related applications and data sources

Digital Portfolio Management \(DPM\) enables you to use related applications to view and edit service details in the plan-build-run life cycle. All related applications are optional, so they aren't required to use the DPM experience.

## Data Sources

By design, DPM offers a broad reach of data sources to give you a high-level view of information that impacts your solutions. Its data sources reach across hundreds of data elements across more than 70 tables, as well as many indicators. This expansive reach gives you a broad perspective of items that may influence your solutions.

DPM has three main data sources:

-   Record and field lookups, either in direct configuration in UIB or in data brokers. The lookups are listed in the data sources Excel file that you can download from [KB1123710](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123710).
-   Needs attention attributes are from data brokers. For more information, see [KB1519343](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1519343).
-   Performance Analytics indicators, data collection jobs, and key performance indicator \(KPI\) groups.

For an overview on how DPM aligns with the Common Service Data Model \(CSDM\), see [Apply the CSDM guidelines to Digital Portfolio Management](dpm-csdm.md).

To view details on the Digital Portfolio Management data sources including data elements, source tables, fields, and required plugins, see [KB1123710](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123710), and select the option to **Download the Data Sources Excel File**.

## Enterprise portfolios

Since the Utah release, you can install the enterprise portfolio plugin \[enterprise portfolio\] that’s available as part of the core ServiceNow AI Platform. Installing the plugin installs two new roles:

-   The enterprise portfolio admin \[sn\_ep.enterprise\_portfolio\_admin\] can create, read, update, and delete \(CRUD\) enterprise portfolios.
-   The enterprise portfolio viewer \[sn\_ep.enterprise\_portfolio\_viewer\] can read enterprise portfolios.

    Installing the enterprise portfolio plugin results in the following:

    -   The DPM admin role inherits the enterprise portfolio admin role.
    -   The DPM manager role inherits the enterprise portfolio viewer role.

## Services and service offerings

**Note:** Your data view in DPM is the same as what your product license permits from the application that you pull data from \(standard or pro\).

<table id="table_arq_5zx_rrb"><thead><tr><th>

To see in DPM

</th><th>

Required installs

</th><th>

Required roles

</th><th>

Use cases

</th></tr></thead><tbody><tr><td>

-   Contextual side panel
-   Needs attention

</td><td>

There are no special installs required to use the contextual side panel or to see items that need attention.

</td><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

-   Use the contextual side panel to navigate to portfolios and list modules in DPM.
-   See items that need attention based on criticality.

</td></tr><tr><td>

Plan tab

</td><td>

To see roadmap data:

 Install the plugin for Strategic Planning: com.sn\_align\_ws

 To see improvement initiatives:

 Install the plugin for ServiceNow® Continual Improvement Management com.sn\_cim

 To see demand data:

 Install plugins for Demand Management: idea\_core, dmn\_demand, and pm\_project

</td><td>

For Strategic Planning:

 -   sn.align\_ws
-   sn\_align\_core. apw\_user
-   sn\_align\_core.apw\_admin
-   sn\_roadmap\_plng.roadmap\_editor

 For Continual Improvement Management and demands:

 DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

-   Select **View roadmap** to launch Strategic Planning to view roadmap details in the context of the selected service or service offering.
-   You can edit roadmaps with the sn\_roadmap\_plng.roadmap\_editor role.
-   Use Continual Improvement Management to see ideas and improve processes across services and service offerings.
-   Create demands on your services and service offerings in DPM.

</td></tr><tr><td>

Build tab

</td><td>

To see roadmap data:

 Install the plugin for Strategic Planning: com.sn\_align\_ws

 To see project data:

 Install the plugin for Project Portfolio Management com.snc.financial\_planning\_pmo

 To see changes:

 No required install. Change data is standard with IT Service Management \(ITSM\).

 To see improvement initiatives:

 Install the plugin for Continual Improvement Management com.sn\_cim

</td><td>

For Strategic Planning:

 -   sn.align\_ws
-   sn\_align\_core. apw\_user
-   sn\_align\_core.apw\_admin
-   sn\_roadmap\_plng.roadmap\_editor

 For PPM, Changes, and Continual Improvement Management:

 DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

-   Select **View roadmap** in DPM to have Strategic Planning launch for you. You can view roadmap details in the context of the selected service or service offering.
-   Edit roadmaps with the sn\_roadmap\_plng.roadmap\_editor role.
-   See project data that may impact your services or service offerings.
-   Select any of the change graphs to view details about change records that may impact your services or service offerings.
-   Use Continual Improvement Management to see ideas and improve processes across services and service offerings.

</td></tr><tr><td>

Run tab

</td><td>

The key performance indicator \(KPI\) group \[sn\_team\_perf\_kpi\_group\] is automatically installed for you to see performance data:

 The Performance snapshot indicator sources come from Performance Analytics:

 -   serviceoffering.availability.daily
-   incidents.open
-   incidents.resolved
-   \[DPM\]requests.new

 See [KB1160281](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1160281) for important criteria to see performance data.

</td><td>

-   DPM Manager \[sn\_dpm.dpm\_manager\] to view KPIs
-   DPM Admin \[sn\_dpm.dpm\_admin\] to create KPIs

</td><td>

View the Performance snapshot KPI group that includes the following supporting KPIs:

-   Service availability
-   New incidents on the service
-   Subscribers of the service
-   Service customer satisfaction score

 View additional KPI groups for service offerings:

-   Outages and availability
-   Incidents
-   Changes
-   Problems
-   Catalog activity

 View availability and service level agreements \(SLA\) commitments reporting.

</td></tr><tr><td>

Info tab

</td><td>

No special installs required.

</td><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

View general information about the service and service offering.

</td></tr></tbody>
</table>## Business applications

**Note:** Your data view in DPM is the same as what your product license permits from the application that you pull data from \(standard or pro\).

<table id="table_mtz_rvs_gsb"><thead><tr><th>

To see in DPM

</th><th>

Required installs

</th><th>

Required roles

</th><th>

Use cases

</th></tr></thead><tbody><tr><td>

-   Contextual side panel
-   Needs attention

</td><td>

To see audits, install the plugin for Audit Management \(sn\_audit\)

 To see technical risks, install the plugin for Technology Portfolio Management: sn\_apm\_tpm. This plugin has two dependency plugins:

-   Application Portfolio Management \(com.snc.apm\)
-   Software Asset Management \(com.snc.sams\)

</td><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

-   Use the contextual side panel to navigate to portfolios and list modules in DPM.
-   See items that need attention based on criticality.

</td></tr><tr><td>

Plan tab

</td><td>

To see roadmap data:

 Install the plugin for Strategic Planning: com.sn\_align\_ws

 To see improvement initiatives:

 Install the plugin for Continual Improvement Management com.sn\_cim

 To see demand data:

 Install plugins for Demand Management: idea\_core, dmn\_demand, and pm\_project

</td><td>

For Strategic Planning:

 -   sn.align\_ws
-   sn\_align\_core. apw\_user
-   sn\_align\_core.apw\_admin
-   sn\_roadmap\_plng.roadmap\_editor

 For Continual Improvement Management and demands:

 DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

-   Select **View roadmap** to launch Strategic Planning to view roadmap details in the context of the selected business application.
-   You can edit roadmaps with the sn\_roadmap\_plng.roadmap\_editor role.
-   Use Continual Improvement Management to see ideas and improve processes across business applications.
-   Create demands on your business applications in DPM.

</td></tr><tr><td>

Build tab

</td><td>

To see roadmap data:

 Install the plugin for Strategic Planning: com.sn\_align\_ws

 To see project data:

 Install the plugin for Project Portfolio Management \(PPM\): com.snc.financial\_planning\_pmo

 To see agile data:

 Install the plugin for Agile Development: com.snc.sdlc.agile.2.

 To see changes:

 No required install. Change data is standard with IT Service Management \(ITSM\).

 To see flow metrics and accelerate metrics:

 Enable DevOps for DPM \(see [Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md)\)

-   To see details in the DevOps Change Workspace, select **View DevOps Insights** from the Flow metrics section.
-   To see details in the DevOps Change Workspace, select **View Accelerate metrics in DevOps** from the Accelerate metrics section.

</td><td>

For Strategic Planning:

 -   sn.align\_ws
-   sn\_align\_core. apw\_user
-   sn\_align\_core.apw\_admin
-   sn\_roadmap\_plng.roadmap\_editor

 For PPM, Changes, and Agile Development:

 DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

-   Select **View roadmap** in DPM to launch Strategic Planning launches for you. You can view roadmap details in the context of the selected business application.
-   Edit roadmaps with the sn\_roadmap\_plng.roadmap\_editor role.
-   See project data that may impact your business applications.
-   View data from Agile Development to view details on epics, stories, sprints, and releases in the context of the selected business application.
-   Manage scrum and waterfall development in DPM to gain visibility into your software development life cycle.
-   Select any of the change graphs to view details about change records that may impact your business applications.

</td></tr><tr><td>

Run tab

</td><td>

Install the plugin for Application Portfolio Management \(APM\):

 com.snc.apm

 To see accelerate metrics:

 Enable DevOps for DPM

 **Note:** To see details in the DevOps Change Workspace, select **View Accelerate metrics in DevOps** from the Accelerate metrics section.

</td><td>

-   DPM Manager \[sn\_dpm.dpm\_manager\] to view KPIs
-   DPM Admin \[sn\_dpm.dpm\_admin\] to create KPIs

</td><td>

View the Performance snapshot, which includes the following metrics:

-   Number of incidents
-   Number of problems
-   Number of changes
-   Total change hours

 View deployments data:

-   Deployments breakdown
-   Deployment hardware and software models \(technology data\)

 **Note:** Technology Portfolio Management data comes from APM.

</td></tr><tr><td>

Risk tab

</td><td>

Install plugins for Governance, Risk, and Compliance and ServiceNow® Risk Management:

 -   com.sn\_risk
-   com.snc.governance
-   sn.grc.common
-   com.snc.risk\_asmt
-   com.snc.grc\_risk\_dep
-   com.snc.grc.common
-   com.snc.grc\_policy\_dep

 Install the plugin for ServiceNow® Audit Management \(sn\_audit\)

</td><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

View risks related to your business applications.

</td></tr><tr><td>

Info tab

</td><td>

No special installs required.

</td><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

View general information about the business applicaton.

</td></tr></tbody>
</table>## Application services

**Note:** Your data view in DPM is the same as what your product license permits from the application that you pull data from \(standard or pro\).

<table id="table_rlt_zks_3tb"><thead><tr><th>

To see in DPM

</th><th>

Required installs

</th><th>

Required roles

</th><th>

Use cases

</th></tr></thead><tbody><tr><td>

Needs attention

</td><td>

To see alerts and alert data, install the plugin for Event Management \(com.glide.platform\_ml\)

 To see technical risks, install the plugin for Technology Portfolio Management: sn\_apm\_tpm. This plugin has two dependency plugins:

-   Application Portfolio Management \(com.snc.apm\)
-   Software Asset Management \(com.snc.sams\)

</td><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

See items that need attention, including alerts and technical risk information.

</td></tr><tr><td>

Run tab

</td><td>

To see reliability indicators, install the plugin for Site Reliability Metrics:

 sn\_srm

 To see alerts and alert data, install the plugin for Event Management \(com.glide.platform\_ml\)

</td><td>

-   DPM Manager \[sn\_dpm.dpm\_manager\] to view KPIs
-   DPM Admin \[sn\_dpm.dpm\_admin\] to create KPIs

</td><td>

View the following information:

 View application service performance

-   Service health
-   Service impact
-   Alert trends

 View site reliability management

-   Number of reliability indicators
-   Description of reliability indicators

 View offerings that depend on this application service

-   Number of reliability offerings
-   Drill down to offering to see the related records

 View technology risk

-   Software models by:
-   Hardware models
-   Drilling down in each model to see the related records

</td></tr><tr><td>

Info tab

</td><td>

No special installs required.

</td><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

View general information about the application service.

</td></tr></tbody>
</table>## Examples

## Plan data sources for services and service offerings

**Note:** Your data view in DPM is the same as what your product license permits from the application that you pull data from \(standard or pro\).

Strategic Planning \(formerly known as Alignment Planner Workspace\) is a pro version. Portfolio Planning is available for users with a Strategic Portfolio Management \(SPM\) standard license.

![Plan data sources for services and service offerings.](../image/dpm-ref-plan.png)

## Build data sources for services and service offerings

![Build data sources for services and service offerings.](../image/dpm-ref-build-projects.png)

## Run data sources for services and service offerings

![Run data sources for services and service offerings.](../image/dpm-ref-run.png)

**Parent Topic:**[Digital Portfolio Management reference](dpm-reference-cfw.md)


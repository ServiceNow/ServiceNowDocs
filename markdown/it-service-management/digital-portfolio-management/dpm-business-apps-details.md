---
title: View business application details
description: View information about business applications that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the business application life-cycle phase information in tabs — Plan, Build, Run, Risk, and Info.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Digital Portfolio Management life-cycle management, Exploring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# View business application details

View information about business applications that may impact your solutions. Each Digital Portfolio Management \(DPM\) page presents the business application life-cycle phase information in tabs — Plan, Build, Run, Risk, and Info.

## Status of business applications

When viewing the business application details in DPM, the **Status** of each item is listed on the workspace view and on the list view.

When viewing details of a business application that's retired, an alert banner along the top of the workspace informs you. In the list view, the **Life Cycle Stage** is **End of Life** and the **Life Cycle Stage Status** is **Retired**.

**Important:** If your organization transitioned from the traditional Service Portfolio Management fields to the CSDM life-cycle fields, then the field names differ from this document. For more information, see [Apply the CSDM guidelines to Digital Portfolio Management](../reference/dpm-csdm.md).

Business application information is displayed in DPM via the Plan, Build, Run, Risk, and Info tabs. If your organization opts to inactivate one or more of the tabs, then the inactivated tabs aren't visible to you. For example, if your organization doesn't work on planning activities and they inactivate the Plan tab, then the Plan tab isn't visible for you. For more information on how Admins can hide or show tabs, see [Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md).

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

-   When selected, see roadmap details in the Strategic Planning or the Portfolio Planning Workspace.
-   When selected, see backlog information in a shared service support planning backlog list.

</td></tr><tr><td>

**Summary**

</td><td>

Summary cards for the business application. You can select each card to go to a list of the items.

-   Total ideas
-   Approved demands
-   Project starting in 30 days
-   Planned epics

</td></tr><tr><td>

**Demands**

</td><td>

Total number of demands on the business application. The number of demands is in a gray box.

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

When selected, see roadmap details in the Strategic Planning or the Portfolio Planning Workspace.

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

 **Note:** Both the Active projects by current status and the Projects overdue by month graphs include the following:

-   Project updates that are directly related to the business application.
-   Project updates of the related application services that roll up to the business application.

 **Active projects**

 Total number of active projects on the service or service offering. The number of active projects is in a gray box. Select an active project record to view its details.

</td></tr><tr><td>

**Epics**

</td><td>

Epic cards provide the count of each of the following for the business application. You can select a card to go to a list of the items.

-   Epics in backlog that are ready
-   Epics in progress

</td></tr><tr><td>

**Stories**

</td><td>

Story cards provide the count of each of the following for your business application. You can select a card to go to a list of the items.

-   Stories in backlog that are ready
-   Stories in progress
-   Blocked stories

</td></tr><tr><td>

**Sprints**

</td><td>

Current sprints related to the business application. The number of sprints is in a gray box. You can select a sprint to see its details.

</td></tr><tr><td>

**Releases**

</td><td>

Current releases related to the business application. The number of current releases is in a gray box. You can select a current release to see its scrum release details.

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
-   A bar graph shows the changes overdue by month.

</td></tr></tbody>
</table>## Build tab with DevOps enabled

After a DPM Admin enables the DevOps system property, you can see the flow metrics and accelerate metrics on the Build tab. The epics, stories, sprints, and releases don't show when DevOps is enabled. For Admin instructions to turn on or off the DevOps system property, see [Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md).

<table id="table_lpg_npv_5zb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Roadmap**

</td><td>

When selected, see roadmap details in the Strategic Planning or the Portfolio Planning Workspace.

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

 **Note:** Both the Active projects by current status and the Projects overdue by month graphs include the following:

-   Project updates that are directly related to the business application.
-   Project updates of the related application services that roll up to the business application.

 **Active projects**

 Total number of active projects on the service or service offering. The number of active projects is in a gray box. Select an active project record to view its details.

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
-   A bar graph shows the changes overdue by month.

</td></tr><tr><td>

**Flow metrics**

</td><td>

Overview of the DevOps Change Workspace flow metric information related to the business application. You can also select **View Flow metrics in DevOps** to go to the DevOps Change Workspace, Flow metrics tab.

 The following flow metrics are in number of days, donut reports, and graphs:

-   Average flow time for epics \(last 30 days\)
-   Average flow time for epic and feature
-   Average number of bugs and stories \(last 30 days\)
-   Distribution of bugs and stories
-   Work in progress cycle time for epics \(last 30 days\)
-   Work in progress cycle time for stories \(last 30 days\)
-   Work in progress cycle time for bugs \(last 30 days\)
-   Work in progress items \(count plotted weekly\)

</td></tr><tr><td>

**Accelerate metrics**

</td><td>

Overview of the DevOps Change Workspace accelerate metric information related to the business application. You can also select **View Accelerate metrics in DevOps** to go to the DevOps Change Workspace, Accelerate metrics tab.

 The following accelerate metrics are shown in number of days and graphs:

-   Average lead time for deployment \(last 30 days\)
-   Commit to deploy lead time \(plotted daily for last 6 months\)
-   Average deployment frequency \(last 30 days\)
-   Production deployment frequency \(plotted daily for last 6 months\)

</td></tr></tbody>
</table>## Run tab

See [KB1637474](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637474) for more information about KPI results on DPM pages.

<table id="table_lvp_4kv_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Business application performance**

</td><td>

Performance details about the business application. You can select a card indicator in each section to view its details. Each indicator has an information icon \(![Information icon.](../image/information-icon.jpg)\) that when selected, provides a tooltip description for that indicator.

 **Portfolio success metrics**

-   Availability
-   Incidents with a breached SLA
-   Incidents caused by changes
-   Successful changes

 **Business application performance**

-   Number of incidents
-   Number of problems
-   Number of changes

 Each of these indicators also includes records when:

-   The record references an application service that is related to the business application, and
-   The record directly references the business application.

</td></tr><tr><td>

**Application service breakdown**

</td><td>

Key performance indicator \(KPI\) group breakdown grid that shows the lowest ordered KPI group mapped \(or inherited\) by the business application.

</td></tr></tbody>
</table>## Run tab with DevOps enabled

After a DPM Admin enables the DevOps system property, you can see the accelerate metrics on the Run tab. For Admin instructions to turn on or off the DevOps system property, see [Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md).

See [KB1637474](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637474) for more information about KPI results on DPM pages.

<table id="table_umz_chz_hbc"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Business application performance**

</td><td>

Performance details about the business application. You can select a card indicator in each section to view its details. Each indicator has an information icon \(![Information icon.](../image/information-icon.jpg)\) that when selected, provides a tooltip description for that indicator.

 **Portfolio success metrics**

-   Availability
-   Incidents with a breached SLA
-   Incidents caused by changes
-   Successful changes

 **Business application performance**

-   Number of incidents
-   Number of problems
-   Number of changes

 Each of these indicators also includes records when:

-   The record references an application service that is related to the business application, and
-   The record directly references the business application.

</td></tr><tr><td>

**Application service breakdown**

</td><td>

Key performance indicator \(KPI\) group breakdown grid that shows the lowest ordered KPI group mapped \(or inherited\) by the business application.

</td></tr><tr><td>

**Accelerate metrics**

</td><td>

The following accelerate metrics are shown in number of days and graphs. The DevOps system property must be enabled for this data to show.

-   Average mean time to restore \(last 30 days\)
-   Mean time to restore from incidents caused by change
-   Average change failure rate \(last 30 days\)
-   Change failure rate over time

</td></tr></tbody>
</table>## Risk tab

<table id="table_mc3_tmv_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Governance, Risk, and Compliance**

</td><td>

Information about risks related to the business application. You can select a card to see its details.

 Risk summary

 -   Risk rating \(low, medium, or high\)
-   Risk count \(number\)

 Compliance summary

 -   Controls out of compliance \(count\)
-   Attestations count \(number\)
-   Total controls count \(number\)

 Engagements

-   Total engagements \(count\)
-   In progress engagements \(count\)

 Issues &amp; tasks

 -   Total issues \(count\)
-   Risk response task \(count\)
-   Remediation task \(count\)

</td></tr><tr><td>

**Technology lifecycle risk**

</td><td>

The technology lifecycle risk for the business application with software and hardware models presented in donut reports and lists.

</td></tr><tr><td colspan="2">

**Note:** To see the technology lifecycle risk information, you must have the Technology Portfolio Management plugin \[sn\_apm\_tpm\] installed. The \[sn\_apm\_tpm\] plugin has two dependency plugins:

-   Application Portfolio Management \[com.snc.apn\]
-   Software Asset Management \[com.snc.sams\]

</td></tr></tbody>
</table>## Info tab

The Info tab provides general information about the business application. You can't edit fields in the Info tab.

<table id="table_mft_jlv_vwb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Application description**

</td><td>

Description of the business application.

</td></tr><tr><td>

**General Info**

</td><td>

General information about the business application.-   Enterprise portfolio
-   Taxonomy node
-   Department
-   Business unit
-   Application family
-   Application category
-   Architecture type
-   Status
-   Lifecycle stage
-   Lifecycle stage status
-   Install type
-   User base count
-   Active user count

</td></tr><tr><td>

**Personal portfolios**

</td><td>

The personal portfolios that contain the business application. The number of the personal portfolios is in a gray box. You can select a personal portfolio to view its details.

</td></tr><tr><td>

**Business capabilities** and **Application services**

</td><td>

Cards that show the number of business capabilities and application services that are related to the business application. You can select each card to go to a list of each item respectively.

</td></tr><tr><td>

**Contract**

</td><td>

General information about the contract related to the business application:

-   Vendor
-   Support vendor
-   Contract end date

</td></tr><tr><td>

**Additional information**

</td><td>

Cards that show the number of the following additional information related to the business application. You can select each card to go to a list of the items.

-   Business Unit Strategy
-   Goals
-   Information objects

</td></tr></tbody>
</table>## Needs attention panel icons

The Needs attention panel includes the following icons for business applications:

-   Needs attention icon \(![Needs attention icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to show or hide the Needs attention panel.
-   Contacts icon \(![Contacts icon.](../image/contacts.png)\) to view team members and teams for the record.
-   Attachments icon \(![Attachments icon.](../image/attachment.png)\) to view and add attachments to the record.

**Related topics**  


[Enterprise portfolios](dpm-enterprise-portfolios.md)

[Create enterprise portfolios in Digital Portfolio Management](../task/dpm-create-enterprise-portfolios.md)


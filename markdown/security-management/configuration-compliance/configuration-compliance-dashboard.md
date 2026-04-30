---
title: Viewing the Performance Analytics for Configuration Compliance dashboard
description: You can manage your most important configuration issues and remediate them quickly by viewing the reports on the Configuration Compliance Performance Analytics \(PA\) dashboard.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Configuration Compliance dashboard, Analytics and reporting for Configuration Compliance, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Viewing the Performance Analytics for Configuration Compliance dashboard

You can manage your most important configuration issues and remediate them quickly by viewing the reports on the Configuration Compliance Performance Analytics \(PA\) dashboard.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|



## Required ServiceNow AI Platform roles

The following roles are required for the Configuration Compliance Performance Analytics dashboard:

-   admin: An admin can install and activate the Performance Analytics for Configuration Compliance and make changes to the system properties.
-   pa\_admin: A performance analytics administrator can create and review the background jobs, indicators, breakdowns, widgets, and dashboards. This admin can also set up and start the data collection.
-   sn\_vulc.read: A user with the read role can review the dashboard data.

## Access the Configuration Compliance dashboard

To open the dashboard, navigate to **All** &gt; **Configuration Compliance** &gt; **Overview**.

Starting with version 14.9 of Configuration Compliance, this dashboard can also be viewed in the New Experience UI. To view the dashboard in the new UI, navigate to **Workspaces** &gt; **Vulnerability Manager Workspace** and click the **Dashboards** icon. Depending on your role, the default dashboard is displayed. To view other dashboards, click the drop-down next to the dashboard name. For more information, see the [Dashboards in the Vulnerability Manager Workspace](../../../product/vulnerability-response/task/vr-ws-dashboards.md) and [Dashboards in the IT Remediation Workspace](../../../product/vulnerability-response/task/itr-ws-dashboards.md).

**Note:** If you are on Tokyo, you can view the dashboards in the Next Experience UI but with some functional loss.

## Configuration Compliance \[PA\] dashboard tabs

The **Overview** tab provides five filters. These filters are the Asset category, Cloud resource type, Cloud service provider, Cloud account, and Cloud region, which you can apply to visualize the reports for the filters applied. If you select a category and apply the changes, all the widgets that support the category get refreshed. Each widget displays the applied filter at the bottom and the number of filters applied on the filter icon of the widget. Click the report in a widget to view the additional information on the **KPI Details** tab. On the **KPI Details** tab, you can:

-   Show the records.
-   Compare the records.
-   Change the chart type.
-   Select the date range.
-   View the trends that are based on the duration.
-   Apply the additional filters including the filters that are unavailable on the **Overview** tab. An example is the Host tag.

The following example shows how you can apply the filters in the **Overview** tab and perform the actions in the **KPI Details** tab.

Overview tab in Configuration Compliance dashboard

The **Compliance** tab displays the compliance percentage for the various authoritative sources, such as the Health Insurance Portability and Accountability Act \(HIPAA\) and the Data Interchange Standards Association \(DISA\). You can refine this list by using the column header filters and selecting a category.

The following example shows how you can filter the data in the **Compliance** tab.

Compliance tab in Configuration Compliance dashboard

The **Remediation** tab displays the information about the progress of how remediation is going. You can use this tab to see into the misconfiguration remediation hygiene.

The following example shows the **Remediation** tab.

![Remediation tab](../image/cc-remediation-tab.png "Remediation tab")

The reports on the **Approvals** tab display the information about the exception requests and their approval status.

The following example shows the **Approvals** tab.

![Approvals tab](../image/cc-approvals-tab.png "Approvals tab")

## Breakdowns

The breakdowns that are used by the indicators are as follows:

-   Deferred Reason
-   Age
-   Assignment group
-   Remediation status
-   Result
-   Risk rating
-   Asset category
-   Host tag
-   Configuration test
-   Cloud service provider
-   Cloud region
-   Cloud account
-   Cloud resource type

## Filters

In the **Overview** tab, you can apply the following filters to the widgets to visualize the filtered data.

<table id="table_mml_b3y_vtb"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset category

</td><td>

Choice

</td><td>

Type of asset.

 The four options are:

-   Cloud
-   Container
-   Infra
-   OT

</td></tr><tr><td>

Cloud resource type

</td><td>

Choice

</td><td>

Type of resource. An example is a virtual machine.

 The data in the filter is filled in when you run the integration.

</td></tr><tr><td>

Cloud service provider

</td><td>

Choice

</td><td>

Service provider for the cloud.

 The three options are:

-   Amazon Web Services \(AWS
-   Microsoft Azure
-   Google Cloud Platform \(GCP\)

</td></tr><tr><td>

Cloud account

</td><td>

Choice

</td><td>

Account ID that is created when an account is created in a cloud service. For example, AWS. The account ID data is filled into the filter when you run the integration.

</td></tr><tr><td>

Cloud region

</td><td>

Choice

</td><td>

Location where the resource is hosted.

</td></tr></tbody>
</table>**Note:** You can select multiple options from the filters and select **Apply**. Each widget shows the filters that are applied and the filters that aren’t applied. Depending on the data available, the report is generated. The widget also shows the count of the filter that is supported.

## Data visualizations

<table id="table_kml_b3y_vtb"><thead><tr><th>

Report name

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compliance Trend

</td><td>

Line chart![Line chart that shows the compliance trend.](../../../reuse/reporting/image/line-multiple.svg)

</td><td>

Test Results

</td><td>

Information about the compliance trend:

-   Resources: Total number of resources that are available in the system.
-   Fail: Number of resources with at least one failed test result.
-   Pass: Number of resources with all the test results in the passed state.

</td></tr><tr><td>

Remediation Task

</td><td>

Single score

 ![Single score that shows the test result group.](../../performance-analytics/image/single-score.png)

</td><td>

Test Results

</td><td>

Number of remediation tasks, which are present in the system and are in an active state.

</td></tr><tr><td>

Critical remediation tasks near due

</td><td>

Single score

 ![Single score that shows the critical remediation tasks that are approaching the target.](../../performance-analytics/image/single-score.png)

</td><td>

Test Results

</td><td>

Number of remediation tasks where the risk rating is "critical" and the remediation status is "approaching target."

</td></tr><tr><td>

Test results by risk rating

</td><td>

Bar

 ![Bar that shows the test results by the risk rating.](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

Test Results

</td><td>

Test results in the failed state, which are grouped according to the risk rating.

</td></tr><tr><td>

Test results by age

</td><td>

Bar

 ![Bar that shows the test results by age.](../../../reuse/reporting/image/trend.svg)

</td><td>

Test Results

</td><td>

Test results in the failed state, which are grouped according to when the test results were created.

</td></tr><tr><td>

Closed test results by remediation target adherence

</td><td>

Bar

 ![Bar that shows the closed test results by the remediation target adherence.](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

Test Results

</td><td>

Test results in the passed state, which indicates that this test is closed.

</td></tr><tr><td>

Overdue critical test results by assignment group

</td><td>

List and Score

 ![List and score that show the overdue critical test results by the assignment group.](../../../reuse/reporting/image/score-list-tile.svg)

</td><td>

Test Results

</td><td>

Number of test results where the risk rating is "critical" and the remediation status is "target missed". The report indicates that the test results are in an Open state. If the test results cross the remediation target date, it’s considered as overdue.

</td></tr><tr><td>

Overdue test results- services

</td><td>

List, Score, and Trend

 ![List and score that show the overdue test results-services.](../../../reuse/reporting/image/score-list-tile.svg) ![Trend of the overdue test results-services.](../../../reuse/reporting/image/line-trend.svg)

</td><td>

PA dashboards database view for Services

</td><td>

Number of test results for services where the remediation status is "target missed". This report also displays the name of the services or departments with the highest test results.

</td></tr><tr><td>

Overdue test results- service owners

</td><td>

List, Score, and Trend

 ![List and score that show the Overdue test results-service owners.](../../../reuse/reporting/image/score-list-tile.svg) ![Trend of the overdue test results-service owners.](../../../reuse/reporting/image/line-trend.svg)

</td><td>

PA dashboards database view for Services

</td><td>

Number of test results for service owners whose remediation status is "target missed". This report also displays the name of the services or departments with the highest test results.

</td></tr></tbody>
</table><table id="table_ob1_g5f_c5b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remediation task by risk rating

</td><td>

Bar![Bar chart that shows the remediation task by the risk rating.](../../../reuse/reporting/image/trend.svg)

</td><td>

Remediation task

</td><td>

Breakdown of the risk ratings of all the test results groups that are in the active state.

</td></tr><tr><td>

Remediation task by remediation target status

</td><td>

Bar

 ![Bar chart that shows the remediation task by the remediation target status.](../../../reuse/reporting/image/trend.svg)

</td><td>

Remediation task

</td><td>

Breakdown of the remediation targets of all the test results groups that missed the target, have no target, and are approaching the target.

</td></tr><tr><td>

Remediation task by assignment group

</td><td>

List, Score, and Trend

 ![List and score that show the remediation task by the assignment group.](../../../reuse/reporting/image/score-list-tile.svg) ![Trend of the remediation task by the assignment group.](../../../reuse/reporting/image/line-trend.svg)

</td><td>

Remediation task

</td><td>

Breakdown of the remediation tasks that are based on an assignment group.

</td></tr><tr><td>

Overdue critical remediation task by assignment group

</td><td>

List, Score, and Trend

 ![List and score that show the overdue critical remediation task by the assignment group.](../../../reuse/reporting/image/score-list-tile.svg) ![Trend of the overdue critical test result group by the assignment group.](../../../reuse/reporting/image/line-trend.svg)

</td><td>

Remediation task

</td><td>

Breakdown of the remediation tasks that are based on an assignment group. These remediation tasks have a risk rating as "critical", and their remediation target hasn’t been met.

</td></tr><tr><td>

Expiring remediation task by age

</td><td>

Bar

 ![Bar chart that shows the expiring remediation task by age.](../../../reuse/reporting/image/trend.svg)

</td><td>

Remediation Task

</td><td>

Remediation tasks that are going to expire within a certain duration. A maximum of 10 duration buckets can be created.

</td></tr><tr><td>

All pending exception requests grouped by reason

</td><td>

Bar

 ![Bar chart that shows all pending exception requests that are grouped by reason](../../../reuse/reporting/image/trend.svg)

</td><td>

State change approval

</td><td>

State change approval requests that are grouped by the reason for the exception.

</td></tr><tr><td>

Critical exceptions on test results by assignment group

</td><td>

List, Score, and Trend

 ![List and score that show the critical exceptions on the test results by the assignment group.](../../../reuse/reporting/image/score-list-tile.svg) ![Trend of the critical exceptions on the test results by the assignment group.](../../../reuse/reporting/image/line-trend.svg)

</td><td>

Test Results

</td><td>

Test results that are in a deferred and critical state and are grouped based on the assignment group.

</td></tr></tbody>
</table><table id="table_y5x_35f_c5b"><thead><tr><th>

Reports

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Exception requests by age pending my approval

</td><td>

Bar![Bar chart that shows the exception requests by age pending my approval.](../../../reuse/reporting/image/trend.svg)

</td><td>

Approval

</td><td>

Exception requests that are created by you and that are pending approval. The requests are grouped according to the duration of the request.

</td></tr><tr><td>

Approval requests by reason

</td><td>

Bar

 ![Bar chart that shows the approval requests by reason.](../../../reuse/reporting/image/trend.svg)

</td><td>

State change approval

</td><td>

State change approval requests for creating an exception and include the reason for the exception.

</td></tr><tr><td>

Remediation tasks having approval request by risk rating

</td><td>

Bar

 ![Bar chart that shows the remediation tasks that have an approval request by risk rating.](../../../reuse/reporting/image/trend.svg)

</td><td>

Remediation task

</td><td>

Remediation tasks that have an approval request that is based on the criticality.

</td></tr><tr><td>

My approval requests by approved and rejected status

</td><td>

Bar

 ![Bar chart that shows my approval requests by the approved and rejected status.](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

State change approval

</td><td>

Exception requests that are grouped by the approved and rejected statuses.

</td></tr><tr><td>

Expiring exception requests by me by age

</td><td>

Bar

 ![Bar chart that shows the expiring exception requests by me by age.](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

State change approval

</td><td>

Exception requests that are going to expire in the coming weeks. The exception requests are grouped based on weeks.Whenever an exception request is created, a date is selected for the validity of the exception request. The calculation for the age of the request is based on this date.

</td></tr><tr><td>

Status of exception requests requested by me

</td><td>

Bar

 ![Bar chart that shows the status of the exception requests requested by me.](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

State change approval

</td><td>

Exception requests that are created by you and that are grouped according to the following statuses:-   In review
-   Approved
-   Rejected

</td></tr></tbody>
</table>**Parent Topic:**[Configuration Compliance dashboard](../../application-content-packs/concept/cc-content-pack.md)


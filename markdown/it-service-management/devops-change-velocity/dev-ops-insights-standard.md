---
title: DevOps Insights Standard dashboard - Classic
description: Use the DevOps Insights application with ServiceNow Performance Analytics to gain insight into your DevOps environment.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# DevOps Insights Standard dashboard - Classic

Use the DevOps Insights application with ServiceNow Performance Analytics to gain insight into your DevOps environment.

**Important:** The Insights Standard dashboard is deprecated for new users. Instead, you can use the Insights dashboard from the DevOps Workspace. For more information, see [DevOps Insights dashboard - Workspace](devops-insights-dboard-ws.md#)

**Note:** To collect daily or historical Insights data, unless these jobs were previously customized, you must select **Active** and set the **Run As** credentials to **System Administrator**:

-   **\[DevOps\] Daily Data Collection \(Daily\)** \(active by default\)

    **Note:** This is a scheduled job \(to be run regularly\) to collect daily DevOps data. For optimal performance, set this job to run during periods of low usage.

-   **\[DevOps\] Historical Data Collection \(On Demand\)** \(inactive by default\)

    For new DevOps Insights installations, if you have already been using the DevOps app and you Installed DevOps Insights at a later date, run the Historical Data Collection job to collect historical Insights data.

    **Note:** This is a one-time job to collect historical DevOps data, and not meant to be on a schedule. It might take awhile, so plan on running this job during a period of low usage.


Reports in the dashboard tabs get updated when the dashboard is refreshed.

## Change Acceleration

![DevOps Insights standard](../image/dev-ops-insights-standard.png)

<table id="table_ztj_thg_3hb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total Changes Submitted - Yearly

</td><td>

Change Request

</td><td>

Total DevOps changes submitted yearly.

</td></tr><tr><td>

Avg Time to Close - Last 30 days

</td><td>

Change Request

</td><td>

Average time to close DevOps changes in the last 30 days.

 **Note:** This widget uses average aggregation and does not support multi-element selection.

</td></tr><tr><td>

Change Approval Rate - Last 30 days

</td><td>

Change Request

</td><td>

DevOps average change success rate for change requests in the last 30 days:

 \(\[\[DevOps Change Success\]\] / \[\[DevOps Change\]\]\) \* 100

 **Note:** This widget uses average aggregation and does not support multi-element selection.

</td></tr><tr><td>

Non-DevOps Change Approval Rate - Last 30 days

</td><td>

Change Request

</td><td>

Non- DevOps change approval rate for change requests in the last 30 days:

 \(\[\[Non-DevOps Change Approval\]\] / \[\[Non-DevOps Change\]\]\) \* 100

 **Note:** Filter is not applicable to this widget.

</td></tr><tr><td>

Change Request Volume

</td><td>

Change Request

</td><td>

Volume of change requests created for DevOps in the last 7 days.

 Compare the number of change requests created after your transition to DevOps so you can see the advantage of running DevOps in your environment.

</td></tr><tr><td>

Pending Changes per Pipeline

</td><td>

Step Execution

</td><td>

Number of change requests that have not been closed for each pipeline.

 See the blockages in each pipeline that are keeping the change request from being completed so you can investigate the cause.

</td></tr><tr><td>

Average Time to Close Changes

</td><td>

Change Request

</td><td>

Average time to close DevOps changes by app.

 Compare DevOps change request statistics with non- DevOps change requests to see that DevOps change requests are getting resolved faster.

</td></tr><tr><td>

Changes Awaiting Approval

</td><td>

Change Request

</td><td>

Number of DevOps changes awaiting approval by date range.

 Compare DevOps change request statistics with non- DevOps change requests to see that DevOps change requests are getting resolved faster.

</td></tr><tr><td>

Non-DevOps Changes Awaiting Approval

</td><td>

Change Request

</td><td>

Number of Non-DevOps changes awaiting approval by date range.

 Compare DevOps change request statistics with non- DevOps change requests to see that DevOps change requests are getting resolved faster.

</td></tr></tbody>
</table>## Accelerate Metrics

The Accelerate Metrics tab shows deployment frequency, lead time, MTTR, and change failure rate info.

![DevOps Insights accelerate metrics](../image/dev-ops-insights-standard6.png)

<table id="table_nxx_flr_5lb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deployment Frequency - Monthly

</td><td>

Step Execution

</td><td>

Number of successful production deployments in a month.

 Applies to steps of type **Prod Deploy** that are in completed state.

</td></tr><tr><td>

Average Lead Time

</td><td>

Pipeline Execution

</td><td>

Average of:

 \(\[Time the code is successfully pushed to production\] - \[Earliest commit time\]\)

 Applies to steps of type **Prod Deploy** that are in completed state.

 **Note:** This widget uses average aggregation and does not support multi-element selection.

</td></tr><tr><td>

Mean Time to Resolve - Last 30 days

</td><td>

Database view joined by Incident, Change Request, Step Execution, Step, Pipeline, and App lists.

</td><td>

Average resolve time for an incident caused by a DevOps change in the last 30 days.

 **Note:** This widget uses average aggregation and does not support multi-element selection.

</td></tr><tr><td>

Change Failure Rate - Monthly

</td><td>

Change Request

</td><td>

Average change failure rate in a month.

 **Note:** This widget uses formula and does not support multi-element selection.

</td></tr><tr><td>

Deployment Frequency

</td><td>

Step Execution

</td><td>

Number of successful production deployments in the last 30 days.

 Applies to steps of type **Prod Deploy** that are in completed state.

</td></tr><tr><td>

Change Failure Rate

</td><td>

Change Request

</td><td>

Average change failure rate in the last 30 days.

</td></tr><tr><td>

Mean Time to Resolve Trend

</td><td>

Database view joined by Incident, Change Request, Step Execution, Step, Pipeline, and App lists.

</td><td>

Daily average resolve time for an incident caused by a DevOps change.

</td></tr><tr><td>

Lead Time

</td><td>

Pipeline Execution

</td><td>

\(\[Time the code is successfully pushed to production\] - \[Earliest commit time\]\)

 Applies to steps of type **Prod Deploy** that are in completed state.

 **Note:** This widget uses average aggregation and does not support multi-element selection.

</td></tr></tbody>
</table>## Operational Stability

The Operational Stability tab shows:

-   Service availability

    Average service availability and daily service availability.

-   Mean time to resolve \(MTTR\)

    Mean time to resolve and daily mean time to resolve.


**Note:** You must install the Service Portfolio Management Foundation \(com.snc.service\_portfolio\) plugin to see service availability widgets.

Demo data is also provided for the service availability widgets.

**Note:** You must install the Service Portfolio Management Foundation \(com.snc.service\_portfolio\) plugin before installing the DevOps Insights application to see demo data.

![DevOps Insights Stability tab](../image/dev-ops-insights-stability-tab.png)

<table id="table_wrl_ryc_llb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mean Time to Resolve - Last 30 days

</td><td>

Database view joined by Incident, Change Request, Step Execution, Step, Pipeline, and App lists.

</td><td>

Average resolve time for an incident caused by a DevOps change in the last 30 days.

 **Note:** This widget uses average aggregation and does not support multi-element selection.

</td></tr><tr><td>

Incidents - Monthly

</td><td>

Incident

</td><td>

Number of incidents in a month \(based on pipeline steps of type **Prod Deploy**\) linked to business service in CMDB.

 This report provides an indication of environment stability.

</td></tr><tr><td>

Average Service Availability - Last 30 days

</td><td>

Database view joined by Service Availability, Service Offering, Business Service, Step, Pipeline, and App lists.

</td><td>

Average service availability in the last 30 days \(based on pipeline steps of type **Prod Deploy**\) linked to application service in CMDB.

 This report provides an indication of environment stability.

</td></tr><tr><td>

Outages - Monthly

</td><td>

Outage

</td><td>

Number of outages in a month \(based on pipeline steps of type **Prod Deploy**\) linked to the associated business service in CMDB.

 This report provides an indication of environment stability.

</td></tr><tr><td>

Mean Time to Resolve Trend

</td><td>

Database view joined by Incident, Change Request, Step Execution, Step, Pipeline, and App lists.

</td><td>

Daily average resolve time for an incident caused by a DevOps change.

</td></tr><tr><td>

Service Availability Trend

</td><td>

Database view joined by Service Availability, Service Offering, Business Service, Step, Pipeline, and App lists.

</td><td>

Daily average service availability \(based on pipeline steps of type **Prod Deploy**\) linked to application service in CMDB.

 This report provides an indication of environment stability.

</td></tr><tr><td>

Incidents Trend

</td><td>

Incident

</td><td>

Daily number of incidents \(based on pipeline steps of type **Prod Deploy**\) linked to business service in CMDB.

 This report provides an indication of environment stability.

</td></tr><tr><td>

Outage Trend

</td><td>

Outage

</td><td>

Daily number of outages \(based on pipeline steps of type **Prod Deploy**\) linked to business service in CMDB.

 This report provides an indication of environment stability.

</td></tr></tbody>
</table>## Development

![DevOps Insights standard tab3](../image/dev-ops-insights-standard3.png)

<table id="table_o3s_1jg_3hb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Commit Frequency

</td><td>

Commit

</td><td>

Number of commits measured daily.

 Smaller more frequent commits are preferred over larger less frequent ones.

</td></tr><tr><td>

Average Branches per Repository

</td><td>

Branches, Repository

</td><td>

Average branches per repository on a given day.

 **Note:** This widget uses formula and does not support multi-element selection.

</td></tr><tr><td>

Average Commits per Pipeline Execution

</td><td>

Commit, Pipeline Execution

</td><td>

Average commits per pipeline on in the last 30 days:

 \[\[Total number of commits\]\] / \[\[Number of pipeline executions\]\]

 **Note:** This widget uses average aggregation and does not support multi-element selection.

 A low number is preferable, which indicates a concentrated effort, versus switching from task to task without completion.

</td></tr><tr><td>

Commits without Work Item

</td><td>

Commit

</td><td>

Commits made that are not tied to a work item, grouped by committer, in the last 30 days.

 This report is useful for investigating and resolving why a commit is not tied to a work item, because all commits should be tied to a work item.

</td></tr><tr><td>

Work Items

</td><td>

Work Item

</td><td>

Number of work items that are complete or working in progress in the last 30 days.

 **Note:** Filter is not applicable to this widget.

</td></tr></tbody>
</table>## Commit Insights

![CommitInsightsStandard](../image/dev-ops-insights-standard4.png)

<table id="table_ccl_gzd_jjb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active Committers

</td><td>

Commit

</td><td>

Committers that submitted commits in the last 30 days.

 Shows how many active committers there are.

 **Note:** This widget uses count distinct aggregation and does not support multi-element selection.

</td></tr><tr><td>

Average Commits per Committer

</td><td>

Commit

</td><td>

Total number of commits in the last 30 days / Active committers.

 Shows how often committers are committing. A higher value is more favorable.

 **Note:** This widget uses formula and does not support multi-element selection.

</td></tr><tr><td>

Average Files Added per Commit

</td><td>

Commit, Commit Details

</td><td>

Total number of files added in the last 30 days / Total number of commits in the last 30 days.

 Shows how few files are committed at a time. A lower value is more favorable.

 **Note:** This widget uses formula and does not support multi-element selection.

</td></tr><tr><td>

% Commits Reverted

</td><td>

Commit

</td><td>

Commits reverted in the last 30 days / Total number of commits in the last 30 days.

 Shows how many commits have been reverted. A lower value is more favorable.

 **Note:** This widget uses formula and does not support multi-element selection.

</td></tr><tr><td>

Top Committers

</td><td>

Commit

</td><td>

Committers with the highest number of commits in the last 30 days.

 Provides visibility into the users that commit the most.

</td></tr><tr><td>

Top Reverters

</td><td>

Commit

</td><td>

Committers with the highest number of reverts in the last 30 days.Provides visibility into the users that revert commits the most.

</td></tr><tr><td>

Commits Added per App

</td><td>

Commit, Commit Details

</td><td>

Number of commits added per app in the last 30 days.

 Provides visibility into the development activity for each app.

 **Note:** Filter is not applicable to this widget.

</td></tr></tbody>
</table>## Deployments

![InsightsDeploymentStandard](../image/dev-ops-insights-standard5.png)

Deployment frequency lets you know how often you are delivering value based on production deployments. Typically, more frequent deployments are desired.

**Note:** Metrics are based off production deployments \(**Type** field is set to Prod Deploy in the app step\).

<table id="table_oz3_ly4_vjb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deployment Frequency - Monthly

</td><td>

Step Execution

</td><td>

Number of successful production deployments in a month.

 Applies to steps of type **Prod Deploy** that are in completed state.

</td></tr><tr><td>

Failed Deployments

</td><td>

Step Execution

</td><td>

Number of failed production deployments in the last 30 days.

 Applies to steps of type **Prod Deploy** that are in failed or user-canceled state.

</td></tr><tr><td>

Deployment Success Rate

</td><td>

Step Execution

</td><td>

Deployments success rate over the last 30 days.

 Deployment Success Rate = \(Number of Successful Deployments in the last 30 days / Total Number of Deployments in the last 30 days\) \* 100

 Applies to steps of type **Prod Deploy** in completed state.

 **Note:** This widget uses formula and does not support multi-element selection.

</td></tr><tr><td>

Average Lead Time

</td><td>

Pipeline Execution

</td><td>

Average of:

 \(\[Time the code is successfully pushed to production\] - \[Earliest commit time\]\)

 Applies to steps of type **Prod Deploy** that are in completed state.

 **Note:** This widget uses average aggregation and does not support multi-element selection.

</td></tr><tr><td>

Successful Production Deployments

</td><td>

Step Execution

</td><td>

Frequency of successful production deployments over time broken down by app.

 More frequent production deployments are preferred.

</td></tr><tr><td>

Failed Production Deployments

</td><td>

Step Execution

</td><td>

Frequency of failed production deployments over time broken down by app.

</td></tr><tr><td>

Commit-to-Deploy Lead Time

</td><td>

Pipeline Execution

</td><td>

Duration from the earliest commit time to production deployment \(for a successful pipeline execution\).

 Minimizing the time it takes from committing code to successfully running it in production is preferable.

 When the lead time is high, you can investigate the pipeline to identify the slowest steps. For example, a manual change approval process could increase lead time.

</td></tr></tbody>
</table>## System Health

![DevOps Insights standard tab2](../image/dev-ops-insights-standard2.png)

<table id="table_ikb_1jg_3hb"><thead><tr><th>

Report

</th><th>

Source list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task Execution Success Rate

</td><td>

Task Executions

</td><td>

Success rate for tasks run by the execution tools over time:

 \[\[Task Execution Success\]\] / \[\[Task Execution\]\] \* 100

 **Note:** This widget does not support multi-element selection.

</td></tr><tr><td>

Number of Task Executions

</td><td>

Task Executions

</td><td>

Default number of tasks executions in the last 30 days.

</td></tr><tr><td>

Number of API calls

</td><td>

Event

</td><td>

Default number of API calls in the last 30 days.

 **Note:** Filter is not applicable to this widget.

</td></tr></tbody>
</table>**Parent Topic:**[DevOps Change Velocity reference](../reference/devops-change-velocity-reference.md)


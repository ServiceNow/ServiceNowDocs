---
title: DevOps Insights dashboard - Workspace
description: The DevOps Insights dashboard provides a flexible graphical view of operational and business reports. Use the dashboard to evaluate the results of your overall DevOps process.The DevOps Insights Summary dashboard enables an overview of key metrics across various categories from accelerate to quality metrics along with a quick glance of the most active applications.The DevOps Insights Flow metrics reports help you visualize how work is moving through your development process. Uncover bottlenecks by determining which kinds of work \(such as stories or bugs\) are taking the longest.The DevOps Insights Change acceleration tab displays change acceleration metrics that focus on your path to automation, comparing automated changes to manual changes, change policy decisions, and ROI. You can use this information to verify that automated change requests are being resolved more quickly than manually approved change requests.The DevOps Insights Accelerate metrics are four key DevOps metrics that measure software delivery performance. Deployment frequency and lead time measure DevOps speed, while change failure rate and mean time to recovery are used to measure stability.The DevOps Insights Quality metrics dashboard enables a quick glance at data from tools such as SonarQube for code coverage, test pass percentage from your orchestration tools, vulnerabilities from security tools, and even overall bug counts.Development metrics focus on commit data that provides insights into how active and agile your teams are. With this information, you can reach full traceability of work by ensuring that commits are being tagged with the appropriate work items.Operational metrics reflect on the stability of your applications to enable you to ensure that your teams are moving fast without compromising release quality.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Insights reports, DevOps Change Velocity, IT Service Management]
---

# DevOps Insights dashboard - Workspace

The DevOps Insights dashboard provides a flexible graphical view of operational and business reports. Use the dashboard to evaluate the results of your overall DevOps process.

## Summary dashboard

The DevOps Insights Summary dashboard enables an overview of key metrics across various categories from accelerate to quality metrics along with a quick glance of the most active applications.

**Summary reports**

![DevOps Insights Summary dashboard.](../image/devops-insights-summary-tab.png)

<table id="table_n1m_h5d_ytb"><thead><tr><th>

Report

</th><th>

Description

</th><th>

Source

</th></tr></thead><tbody><tr><td>

Average WIP cycle time

</td><td>

Average time in days that a work item is in the WIP state before completion.

</td><td>

Calculation: Time to complete WIP items divided by the number of completed work items

</td></tr><tr><td>

Average lead time

</td><td>

Daily average lead time for prod deploy pipeline executions.

</td><td>

Calculation: Sum of successful prod deploy lead times divided by the number of successful production pipeline executions.

</td></tr><tr><td>

Average deployment frequency

</td><td>

Average number of successful production deployments.

 Applies to pipeline steps of type **Prod Deploy** that are in the completed state.

</td><td>

Step execution

</td></tr><tr><td>

Average test pass %

</td><td>

Daily average test pass percentage for pipeline executions.

</td><td>

Database view joined by test summary, test summary relations, step execution, change request repository detail, step, pipeline, app, and application product detail.

</td></tr><tr><td>

Work items completed

</td><td>

Work items, grouped by work item type, that were set to the complete state during the last 30 days.

</td><td>

Database view joined by work item, metric instance, commit work item, commit, commit execution, step execution, step, pipeline, app, and application product detail.

</td></tr><tr><td>

Activity — last 30 days

</td><td>

For each application, the summary of activity during the last 30 days.

</td><td>

Database view joined by commit, commit work item, repository, commit execution, app, test summary relations, step execution, test summary.

</td></tr></tbody>
</table>## Flow metrics dashboard

The DevOps Insights Flow metrics reports help you visualize how work is moving through your development process. Uncover bottlenecks by determining which kinds of work \(such as stories or bugs\) are taking the longest.

**Flow metrics reports**

![DevOps Insights Flow metrics dashboard](../image/devops-insights-flow-metrics-tab.png)

<table id="table_jsc_zth_ytb"><thead><tr><th>

Report

</th><th>

Description

</th><th>

Source

</th></tr></thead><tbody><tr><td>

Average flow time

</td><td>

Average time, in days, that a work item spent from the created state to step execution end time of a successful prod pipeline deployment.

</td><td>

Database view joined by work item, metric instance, commit work item, commit, commit execution, step execution, step, pipeline, app, and application product detail.

</td></tr><tr><td>

Average WIP cycle time

</td><td>

Average time in days that a work item is in a specific state.

</td><td>

Database view joined by Work Item, Metric Instance, Commit, Step Execution, Commit execution, and Commit work item lists.

</td></tr><tr><td>

Average WIP count

</td><td>

Average number of work items that are WIP during the last 30 days.

</td><td>

Average count of Work Items with State set to Work In Progress.

</td></tr><tr><td>

Work items completed

</td><td>

Number of work items in the complete state that are associated to commits through a successful production pipeline deploy in the last 30 days.**Note:** Filters don’t apply for this chart.

</td><td>

Average count of Work Items associated to Step Execution type set to Prod deploy. This requires commit to work item association as only work items deployed through a pipeline are in production.

</td></tr><tr><td>

Average work item cycle time

</td><td>

Average time in days that a work item is in a specific state.

</td><td>

Database view joined by Work Item, Metric Instance, Commit, Step Execution, Commit execution, and Commit work item lists.

</td></tr><tr><td>

Throughput and distribution

</td><td>

Number of work items, by type, that are associated to commits through a successful production pipeline deploy.

</td><td>

Database view joined by Work Item, Metric Instance, Commit, Step Execution, Commit execution, and Commit work item lists.

</td></tr><tr><td>

Average planned to deploy flow time

</td><td>

Average duration from the time that a work item associated to a commit was created to the time that the item was successfully deployed to production through pipelines.

</td><td>

Database view joined by Work Item, Metric Instance, Commit, Step Execution, Commit execution, and Commit work item lists.

</td></tr><tr><td>

Work in progress

</td><td>

Number of work items that are currently in the work in progress state.

</td><td>

Database view joined by Work Item, Metric Instance, Commit, Step Execution, Commit execution, and Commit work item lists.

</td></tr></tbody>
</table>## Change acceleration dashboard

The DevOps Insights Change acceleration tab displays change acceleration metrics that focus on your path to automation, comparing automated changes to manual changes, change policy decisions, and ROI. You can use this information to verify that automated change requests are being resolved more quickly than manually approved change requests.

**Change acceleration reports**

![DevOps Insights Change acceleration dashboard](../image/devops-insights-change-accel-tab.png)

Change requests that are part of step executions qualify as DevOps change requests.

<table id="table_msf_35h_ytb"><thead><tr><th>

Report

</th><th>

Description

</th><th>

Source

</th></tr></thead><tbody><tr><td>

DevOps change volume

</td><td>

Number of DevOps change requests created.

</td><td>

Database view joined by Step Execution, Change request, and change request repository.

</td></tr><tr><td>

Time to close changes

</td><td>

Average time in hours to close DevOps changes by application. For each month, this is the average for \(Time that change request was closed\) minus \(Time that change request was opened\).

</td><td>

Database view joined by Step Execution, Change request, and change request repository.

</td></tr><tr><td>

Automated vs manual changes

</td><td>

Comparison between the numbers of DevOps change requests using change approval policies and DevOps change requests requiring manual approval.

 -   A change request is considered automated when a change policy performs the approve/reject action.
-   A manual change is any change request that is assigned to a user or group for the approve/reject action and isn’t acted on by a change policy.

</td><td>

Database view joined by Step Execution, Change request, and change request repository.

</td></tr><tr><td>

Changes awaiting approval

</td><td>

Number of DevOps changes that are pending approval by date range.

 By default, change requests in the New or Assess state are considered awaiting approval.

 To specify the states that are considered awaiting approval, update the **Change Request Awaiting States** property setting. For details, see [DevOps Insights properties](../reference/devops-insights-workspace-properties.md).

</td><td>

Database view joined by Step Execution, Change request, System properties, and change request repository detail lists.

</td></tr><tr><td>

Change policy decision: auto-accept

</td><td>

The number of change policy decisions by decision type that automatically accept change requests.

 Point to a value on the chart to view the list of policy decisions that were used for auto-approval and the number of times that a decision was used for auto-approval.

</td><td>

Database view joined by Step Execution, Change request, System properties, and change request repository detail lists.

</td></tr><tr><td>

Change policy decision: auto-reject

</td><td>

The number of change policy decisions by decision type that automatically reject change requests.

 Point to a value on the chart to view the list of policy decisions that were used for auto-rejection and the number of times that a decision was used for auto-rejection.

</td><td>

Database view joined by Step Execution, Change request, Policy applied, Auto approval rejection action, Change approval definition, and change request repository detail lists.

</td></tr><tr><td>

Change acceleration savings

</td><td>

Net amount saved per month by automating DevOps changes.

 When a change is automated, a developer doesn’t have to manually fill out the change request and associate each work item, code commits, test results and other evidence and artifacts to the change. After this activity is automated, hours that would have been spent on filling out the change, searching, tracking down and attaching items from other tools to a change, will now be saved. More work items require a relatively increasing number of hours to associate them manually. Therefore, higher numbers of work items should result in more hours saved after the change is automated. Change acceleration savings are calculated by multiplying the hours saved by the average hourly developer cost.

 To change the default value of the average hourly developer cost, update the **Average Hourly developer Cost** property setting. For details, see [DevOps Insights properties](../reference/devops-insights-workspace-properties.md).

</td><td>

Calculation: Average hourly developer cost multiplied by developer hours saved.

</td></tr><tr><td>

Developer hours saved

</td><td>

Number of developer hours saved per month by automating DevOps changes.To change the default value of 1 \(one\) hour per developer, update the **X hours per Developer time** property setting. For details, see [DevOps Insights properties](../reference/devops-insights-workspace-properties.md).

</td><td>

Calculation: Number of work items in a change request multiplied by 1 hour per developer.

</td></tr></tbody>
</table>## Accelerate metrics dashboard

The DevOps Insights Accelerate metrics are four key DevOps metrics that measure software delivery performance. Deployment frequency and lead time measure DevOps speed, while change failure rate and mean time to recovery are used to measure stability.

**Accelerate metrics reports**

![DevOps Insights Accelerate metrics dashboard](../image/devops-insights-accel-metrics-tab.png)

<table id="table_vrs_p5h_ytb"><thead><tr><th>

Report

</th><th>

Description

</th><th>

Source

</th></tr></thead><tbody><tr><td>

Average lead time

</td><td>

Average of:

 \(\[Time the code is successfully pushed to production\] minus \[Earliest commit time\]\)

 Applies to pipeline steps of type **Prod Deploy** that are in the completed state.

 **Note:** This widget uses average aggregation and doesn’t support multi-element selection.

</td><td>

Pipeline execution

</td></tr><tr><td>

Average deployment frequency

</td><td>

Average number of successful production deployments.

 Applies to pipeline steps of type **Prod Deploy** that are in the completed state.

</td><td>

Step execution

</td></tr><tr><td>

Average MTTR

</td><td>

Average resolve time for an incident caused by a DevOps change.

 **Note:** This widget uses average aggregation and doesn’t support multi-element selection.

</td><td>

Database view joined by Incident, Change Request, Step Execution, Step, Pipeline, and App lists.

</td></tr><tr><td>

Average DevOps change failure rate

</td><td>

Daily average ratio of DevOps change requests that are associated to an incident divided by all DevOps change requests.

 **Note:** This widget uses formula and doesn’t support multi-element selection.

</td><td>

Change request

</td></tr><tr><td>

Commit to deploy lead time

</td><td>

Duration from the earliest commit time to production deployment for a successful pipeline execution.

 The value includes only steps of type **Prod deploy** that are in the completed state.

 You might investigate high lead times by identifying the slowest pipeline steps. For example, a manual change approval process could increase lead time.

</td><td>

Calculation: Sum of successful prod deploy Lead times divided by the number of successful production pipeline executions.Needs 'Commits to Task Execution' association. Both Repository and Pipeline must be tracked and associated to the same App.

Needs Step type to be Prod Deploy.

Needs Task Execution result to be Successful.

</td></tr><tr><td>

Mean time to restore from incidents caused by DevOps changes

</td><td>

Daily average time to resolve an incident that was caused by a DevOps change.

</td><td>

Database view joined by step execution, change request, change request repository detail, and incident lists.

 Calculated only for DevOps incidents by considering incident opened and closed time.

</td></tr><tr><td>

Production deployment frequency

</td><td>

Number of successful production deployments. The value includes only pipeline steps of type **Prod deploy** that are in the completed state.

To change the default value of 30 days, update the **Date range** setting.

</td><td>

Database view joined by Change Request, Step Execution, change request repository detail.

 Needs Step Execution state to be Completed.

 Needs Step type to be Prod Deploy.

</td></tr><tr><td>

DevOps change failure rate from incidents

</td><td>

Percentage of DevOps changes that caused incidents divided by all DevOps changes deployed to production.

 If a change request caused multiple incidents, then only the change that caused or triggered the incident is considered. The number of incidents that the change caused isn’t considered.

</td><td>

Needs DevOps Change Request \(Change associated to a Step Execution\).

 Needs Step Execution state to be Completed.

 Needs Step type to be Prod Deploy.

 Needs Incident caused by to be DevOps Change Request.

</td></tr><tr><td>

Deployment Success Rate

</td><td>

Deployments success rate over the last 30 days.

 Deployment Success Rate = \(Number of Successful Deployments in the last 30 days / Total Number of Deployments in the last 30 days\) \* 100

 Applies to steps of type **Prod Deploy** in completed state.

 **Note:** This widget uses formula and does not support multi-element selection.

</td><td>

Step Execution

</td></tr><tr><td>

Deployment Frequency

</td><td>

Number of successful production deployments in the last 30 days.

 Applies to steps of type **Prod Deploy** that are in completed state.

</td><td>

Step Execution

</td></tr><tr><td>

Deployments failed

</td><td>

Number of failed production deployments in the last 30 days.

 Applies to steps of type **Prod Deploy** that are in failed or user-canceled state.

</td><td>

Step Execution

</td></tr></tbody>
</table>## Quality metrics dashboard

The DevOps Insights Quality metrics dashboard enables a quick glance at data from tools such as SonarQube for code coverage, test pass percentage from your orchestration tools, vulnerabilities from security tools, and even overall bug counts.

**Quality metrics reports**

![DevOps Insights Quality metrics dashboard](../image/devops-insights-qual-metrics-tab.png)

<table id="table_fvw_v5h_ytb"><thead><tr><th>

Report

</th><th>

Description

</th><th>

Source

</th></tr></thead><tbody><tr><td>

Code coverage %

</td><td>

Percentage of code that is covered by testing.

</td><td>

Needs Software Quality Scan Detail with Category = Coverage \(%\)

 Needs Software Quality Scan Summary Relations related to Task Execution

</td></tr><tr><td>

Test pass %

</td><td>

Test pass percentage.

</td><td>

Needs Test Summary related to Task Execution

</td></tr><tr><td>

Security vulnerabilities

</td><td>

Count of security vulnerabilities over time.

</td><td>

Needs Software Quality Scan Detail with Category = Vulnerabilities

 Needs Software Quality Scan Summary Relations related to Task Execution.

</td></tr><tr><td>

Bug counts

</td><td>

Number of work items of type bug.

</td><td>

Needs **Commits to Work Items** association. Both Repository and Plan must be tracked and associated to the same app.

 Needs **Commits to Task Execution** association. Both Repository and Pipeline must be tracked and associated to the same App

 Needs Work Item to be of type Bug.

</td></tr></tbody>
</table>## DevOps Insights Development dashboard

Development metrics focus on commit data that provides insights into how active and agile your teams are. With this information, you can reach full traceability of work by ensuring that commits are being tagged with the appropriate work items.

**Development reports**

![DevOps Insights Development dashboard](../image/devops-insights-development-tab.png)

<table id="table_pk3_z5h_ytb"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Commit frequency

</td><td>

Number of commits associated to pipeline executions.Smaller, more frequent commits are preferred over larger less frequent commits.

</td></tr><tr><td>

Active committers

</td><td>

Number of committers that submitted commits.Because this report uses metric aggregation, it doesn’t support multi-element selection.

</td></tr><tr><td>

Top committers \(30-day running sum\)

</td><td>

Committers with the highest number of commits.

</td></tr><tr><td>

Top reverters \(30-day running sum\)

</td><td>

Committers with the highest number of reverts.

</td></tr><tr><td>

Average commits per committer

</td><td>

Average calculated as: `(total number of commits)/(active committers)`. A higher value is more favorable.

 Because this report uses metric aggregation, it doesn’t support multi-element selection.

</td></tr><tr><td>

Average commits per pipeline execution

</td><td>

Average commits per pipeline, calculated as \(Total number of commits\)/\(Number of pipeline executions\).

 A low number is preferable, which indicates a concentrated effort, versus switching from task to task without completion.

 Because this report uses metric aggregation, it doesn’t support multi-element selection.

</td></tr><tr><td>

Commits without work items

</td><td>

Commits made that aren’t associated to a work item, grouped by committer.

 This report is useful for investigating and resolving why a commit isn’t tied to a work item, because all commits should be tied to a work item.

</td></tr><tr><td>

Pipeline pass percentage

</td><td>

Ratio of successful pipeline executions divided by total number of pipeline executions.

</td></tr></tbody>
</table>## DevOps Insights Operational stability dashboard

Operational metrics reflect on the stability of your applications to enable you to ensure that your teams are moving fast without compromising release quality.

**Operational stability reports**

![DevOps Insights Operational stability dashboard](../image/devops-insights-op-stability-tab.png)

<table id="table_olv_qvh_ytb"><thead><tr><th>

Report

</th><th>

Description

</th><th>

Source

</th></tr></thead><tbody><tr><td>

Incidents

</td><td>

Number of incidents for pipeline steps of type Prod deploy that are linked to a service in the CMDB.

</td><td>

Needs Step type to be Prod Deploy.

 Needs Incident associated to a Service that matches the one in the prod deploy Step.

</td></tr><tr><td>

Outages

</td><td>

Number of outages for pipeline steps of type Prod deploy that are linked to a service in the CMDB.

</td><td>

Needs Step type to be Prod Deploy.

 Needs Outage \(cmdb\_ci\_outage\) associated to a Service that matches the one in the prod deploy Step.

</td></tr><tr><td>

Service availability

</td><td>

Average service availability for pipeline steps of type Prod deploy that are linked to a service in the CMDB.

</td><td>

Needs Step type to be Prod Deploy.

 Needs parent Service Offering associated to a Service that matches the one in the prod deploy Step.

</td></tr><tr><td>

Error budget remaining

</td><td>

Percentage of error budget left to spend in a month, for pipeline steps of type Prod deploy that are linked to a service in the CMDB. This data is from the Site Reliability operations application.

 An error budget is the amount of Service Level Objective \(SLO\) that you can spend over a specified time. It can be used to manage release velocity. It’s typically based on availability, latency, and so on.

</td><td>

Needs Step type to be Prod Deploy.

 Needs parent Service Offering associated to a Service that matches the one in the prod deploy Step.

 Needs SRO application.

</td></tr></tbody>
</table>
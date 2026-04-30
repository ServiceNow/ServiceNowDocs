---
title: DevOps Pipeline UI
description: Use the Pipeline UI to visualize interactions and results across a pipeline execution. This graphical view shows pipeline step progression and other details for each pipeline.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# DevOps Pipeline UI

Use the Pipeline UI to visualize interactions and results across a pipeline execution. This graphical view shows pipeline step progression and other details for each pipeline.

From DevOps, get a quick view of how everything is connected to see exactly what is happening with the pipeline and when. From the ServiceNow Change Management application, you can access the Pipeline UI and quickly see the commits, the committers, and other details for the change request in one place.

The Pipeline UI displays parallel stages as modeled in Azure DevOps release pipelines. The pipeline UI displays the real-time state of the pipeline as it appears in Azure DevOps. The associated artifact details sourced from the build pipeline, Test Results, Software Quality Summary Results also display on the pipeline UI. For more information, see [Parallel stages in Azure DevOps release pipelines](parallel-stages-ado-release-pipelines.md).

The Pipeline UI shows all attempts of any stage or job that has been rerun or restarted. For more information, see [Restarting failed build or release pipeline jobs and stages](restart-pipeline-stage-devops-ado.md).

The Pipeline UI shows the pipeline steps that ran instead of the steps configured in DevOps.

You can access the Pipeline UI using the related link from within certain DevOps forms, and also from a DevOps change request form:

-   DevOps Pipeline form
-   DevOps Pipeline Execution form
-   Change Request form created by DevOps

**Note:** You must reload the view to update the status buttons in the pipeline execution History.

<table id="table_pjs_gmf_rjb"><tbody><tr><td>

Green

</td><td>

Successful.

 All step executions associated to the pipeline execution passed.

</td></tr><tr><td>

Grey

</td><td>

Not yet run.

</td></tr><tr><td>

Yellow

</td><td>

Waiting \(pending, building, validating\).

 At least one step execution is waiting.

</td></tr><tr><td>

Red

</td><td>

Failed.

 At least one step execution failed.

 Task execution end date is populated even when the change is rejected.

 **Note:** To enable the canceling of the change request associated with the step when the step fails, you must set the **sn\_devops.cancel\_change\_on\_pipeline\_cancel** property to Yes. For more information, see [Properties installed with DevOps](dev-ops-administration.md).

</td></tr></tbody>
</table>**Note:** The order the cards appear in the Pipeline UI is determined by the **Order** field in each pipeline step when you modeled your pipeline in DevOps. Skipped stages are not shown.

The order the cards appear in the Pipeline UI by task execution.

![DevOpsPipelineUI](../image/dev-ops-pipeline-ui.png)

<table id="table_nnb_3rc_rjb"><thead><tr><th>

UI feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pipeline steps

</td><td>

Timing.

-   Start
-   Last run
-   Duration for each step

When the downstream task execution starts immediately after the upstream task execution, the duration is 0 seconds.

-   Wait times in between task executions.

Wait time is calculated as:

Start time of the task execution minus the end time of the upstream task execution.


</td></tr><tr><td>

View change request

</td><td>

Change request record.

 Click directly into the change request of the step that was created by DevOps to view details of the change and take action.

 **Note:**

-   The change request record for the associated with the latest task execution displays.
-   Commits reverted in the same pipeline execution are not shown in the commit list.

</td></tr><tr><td>

Pipeline history

</td><td>

Pipeline Execution.

 Click a history tile to view the previous step details for a pipeline execution.

 **Note:** Pipeline history is displayed for only the most recent 20 pipeline executions.

</td></tr><tr><td>

View all attempts

</td><td>

All attempts that the job has run in a step.Click the link in the relevant step to view all attempt details.

</td></tr><tr><td>

Artifacts

</td><td>

-   Artifact versions
    -   Work items
    -   Commits
    -   Packages
-   Commits
-   Work items

 **Note:** Commits reverted in the same pipeline execution are not shown in the commit list.

</td></tr><tr><td>

Test Results

</td><td>

View the build test results to see what tests passed or failed. The quality card contains test summaries:

-   Test type and test category in the format:

`test type/test category`

-   Native ID of the step
-   Test pass percentage \(unit and functional tests only\)
-   Throughput \(performance tests only\)
-   Step name

</td></tr><tr><td>

Software Quality Results

</td><td>

View all the software quality \(SonarQube scan\) results grouped by project name that were fetched as part of the selected pipeline. You can view the scan results for all categories in a pipeline execution step.

 You can customize the results that are displayed in the Pipeline UI by configuring the columns in the **Software quality categories shown by default in the Pipeline UI view** \(**DevOps** &gt; **Administration** &gt; **Properties** &gt; **DevOps Properties Category** &gt; ****\) property in a comma separated format.

 -   Click the gear icon to modify the column view in the pipeline UI.
-   Click the step execution record to view the corresponding Software Quality Scan Summary record.
-   Click the Vulnerabilities count record to view the Software Quality Scan Detail record and the corresponding sub category details.

</td></tr><tr><td>

Security Results

</td><td>

View all the security results that were retrieved as part of the selected pipeline. You can view the scan results for all categories in a pipeline execution step.

 You can customize the results that are displayed in the Pipeline UI.

 -   Click the gear icon to modify the view in the pipeline UI.
-   Click the step execution record to view the corresponding Security scan summary record.
-   Click the Detected flaws count record to view the Security scan details.

</td></tr></tbody>
</table>**Note:** When you reattempt running a stage or a pipeline job in Azure DevOps, which contains a test or a software quality scan, the results get appended with the attempt number.

Click directly into DevOps change requests, step executions, artifacts, artifact versions, work items, test summaries, and reattempts in flyout windows.

![DevOpsPipelineUILink](../image/dev-ops-pipeline-ui3.png "Pipeline UI — Artifact version flyout")

![DevOps Reuse Change request flyout](../image/devops-pipeline-reuse-flyout.png "Pipeline UI - Reuse change request - Step execution flyout")

![Pipeline UI with parallel stages- Azure DevOps](../image/devops-parallel-stages-pipeline-ui.png "Azure DevOps - Pipeline UI with parallel stages")

**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)


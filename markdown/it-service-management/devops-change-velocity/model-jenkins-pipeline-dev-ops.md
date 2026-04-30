---
title: Model a Jenkins pipeline in DevOps
description: Model a Jenkins pipeline by mapping the pipeline to an app, and mapping DevOps pipeline steps to Jenkins stages.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Model a Jenkins pipeline in DevOps

Model a Jenkins pipeline by mapping the pipeline to an app, and mapping DevOps pipeline steps to Jenkins stages.

## Before you begin

The Jenkins plugin for ServiceNow DevOps is provided to enable change acceleration so your orchestration tool can communicate with ServiceNow DevOps and control certain aspects of pipeline executions.

Install the plugin from the Jenkins Marketplace. Navigate to **Manage Jenkins &gt; System configuration &gt; Plugins** in your Jenkins instance. Search for **ServiceNow DevOps Plugin** and select it, and then select **Install**.

Ensure that your Jenkins tool is connected and configured. For more information, see [Onboard Jenkins to DevOps Change Velocity — Workspace](onboard-jenkins-to-devops-change-velocity-workspace.md).

Role required: sn\_devops.admin

## About this task

Both [scripted pipelines](../concept/dev-ops-scripted-pipeline.md) \(Jenkinsfile\) and freestyle jobs are supported.

For Jenkinsfile pipelines, pipeline steps are created, mapped, and associated to orchestration tasks automatically, instead of manually.

## Procedure

1.  Map your pipeline to an app in DevOps.

    1.  Navigate to **DevOps** &gt; **Apps &amp; Pipelines** &gt; **Apps** and open the application record to associate with the pipeline.

    2.  In the Pipelines related list, click **Edit...** to select a pipeline to associate with the app, or click **New** to create the pipeline.

        For a new pipeline, fill in the **Orchestration pipeline** field using the full project name as specified in Jenkins.

        **Note:** While associating a pipeline with an app, the pipeline steps are also fetched during import.

    3.  Click **Submit**.

2.  Open the pipeline record again and select the **Track** check box so events from the pipeline are received.

    **Note:** The **Track** check box must be selected to integrate the pipeline with DevOps.

3.  Create DevOps steps automatically or manually to map to each Jenkins pipeline stage so an orchestration task is created.

    -   For declarative or scripted pipelines, run your Jenkins pipeline to automatically create and map pipeline steps in DevOps.

        Pipeline steps are automatically created, mapped, and associated when DevOps receives step notifications from your Jenkins pipeline during the run.

    -   For freestyle jobs, manually create and map each pipeline step to a Jenkins pipeline job.

        In the Steps related list, click **New** to create a DevOps step for each Jenkins pipeline stage \(**Orchestration stage** field\)

        **Note:** The **Orchestration stage** field value of each step is case-sensitive and must match the original name of the corresponding Jenkins pipeline stage.

<table id="table_gcg_z4f_gnb"><tbody><tr><td>

Name

</td><td>

Name of the pipeline step.

</td></tr><tr><td>

Pipeline

</td><td>

Pipeline in which the step is configured.

</td></tr><tr><td>

Type

</td><td>

Pipeline step type.-   Build and Test
-   Test
-   Deploy
-   Deploy and Test
-   Manual
-   Prod Deploy


</td></tr><tr><td>

Order

</td><td>

Order in which the steps are run.

 **Note:** The step order determines the order of the cards in the [Pipeline UI](../concept/dev-ops-pipeline-ui.md).

The order of the cards in the Pipeline UI is by task execution.

</td></tr><tr><td>

Orchestration stage

</td><td>

Jenkins pipeline stage name \(case-sensitive\).

 **Note:** For step association with Jenkins pipeline stages, the **Orchestration stage** field must be configured.

</td></tr><tr><td>

Business service

</td><td>

Configuration service that applies to the step.

</td></tr></tbody>
</table>        Once orchestration tasks are created, associate each orchestration task in the Orchestration Tasks related list with a DevOps pipeline step.

4.  Enable change control automatically or manually based on the type of pipeline.

    -   For declarative or scripted pipelines, if you have used the snDevOpsChange script in your pipeline, run your Jenkins pipeline to automatically enable change control. You can also enable change control manually by following the steps provided for freestyle jobs.
    -   For freestyle jobs, select the **Change control** check box in a step to enable [change acceleration](../concept/dev-ops-change-acceleration.md) and the corresponding configuration fields.

        **Note:** ServiceNow [Change Management](../../change-management/concept/c_ITILChangeManagement.md) must be installed for change acceleration.

<table id="table_xm1_tdf_llb"><tbody><tr><td>

Change receipt

</td><td>

Select to enable change receipt for the step so the pipeline doesn't pause when a change request is created.

 All pipeline data is included in the change, but approval is not required for the pipeline to proceed.

</td></tr><tr><td>

Change approval group

</td><td>

Approval group for the change request.

 The change approval group becomes the **Assignment group** in the DevOps change request.

 **Note:** Ensure that the selected group has members and a group manager so the approver field is not empty.

</td></tr><tr><td>

Change type

</td><td>

Change request type to create.-   Normal \(default\)
-   Standard
-   Emergency


</td></tr><tr><td>

Change model

</td><td>

Change model for the change request. For more information, see [DevOps change models](../concept/devops-change-multimodel.md).

</td></tr><tr><td>

Template

 **Note:** This field is shown only when **Change type** is Normal or Emergency.

</td><td>

List of templates to use to auto populate fields for Normal or Emergency change requests.

 Select a template or create a new one.

</td></tr><tr><td>

Standard change template

 **Note:** This field is shown only when **Change type** is Standard.

</td><td>

List of standard change templates to use for Standard change requests.**Note:** This field is required for Standard change type.

</td></tr><tr><td>

Change controlled branches

</td><td>

\(Multibranch only\) Comma-separated list of branches under change control. Wildcards are supported.

</td></tr></tbody>
</table>
## Example

![DevOps pipeline](../image/dev-ops-pipeline.png "DevOps app")

![DevOps Pipeline Steps](../image/dev-ops-pipeline-steps.png "DevOps pipeline")

![DevOps pipeline stages](../image/dev-ops-pipeline-stages.png "DevOps pipeline step")

**Parent Topic:**[Jenkins integration with DevOps Change Velocity](../concept/jenkins-integration-dev-ops.md)


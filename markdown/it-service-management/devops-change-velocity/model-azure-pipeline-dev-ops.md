---
title: Model an Azure pipeline in DevOps
description: Model an Azure pipeline by mapping the pipeline to an app, and mapping DevOps Change Velocity pipeline steps to Azure pipeline jobs.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Model an Azure pipeline in DevOps

Model an Azure pipeline by mapping the pipeline to an app, and mapping DevOps Change Velocity pipeline steps to Azure pipeline jobs.

## Before you begin

Role required: sn\_devops.admin

## Procedure

1.  Map your pipeline to an app in DevOps.

    1.  Navigate to **DevOps** &gt; **Apps &amp; Pipelines** &gt; **Apps** and open the application record to associate with the pipeline.

    2.  In the Pipelines related list, click **Edit...** to select a pipeline to associate with the app, or click **New** to create the pipeline.

        **Note:** While associating a pipeline with an app, the pipeline steps are also fetched during import.

        For a new pipeline, fill in the **Orchestration pipeline** field using the project name and pipeline name as specified in Azure DevOps Pipelines in path format.

        For example, `My Project/My Classic Build Pipeline`.

        **Note:** The `project` name must be specified with the pipeline because there could be multiple pipelines with the same name in different projects.

    3.  Click **Submit**.

2.  Open the pipeline record again and select the **Track** check box so events from the pipeline are received.

    The **Track** check box must be selected to integrate the pipeline with DevOps Change Velocity.

3.  Create DevOps steps automatically or manually to map to each Azure pipeline job so an orchestration task can be created.

    **Note:** Manual creation of steps is not required when you [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](config-dev-ops-extensions-azure.md#).

    -   Automatically create and map pipeline steps in DevOps by running your Azure pipeline when you [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](config-dev-ops-extensions-azure.md#).

        Pipeline steps are automatically created, mapped, and associated when DevOps receives step notifications from your Azure pipeline during the run.

    -   Manually create and map each pipeline step to an Azure pipeline job.

        In the Steps related list, click **New** to create a DevOps step for each Azure pipeline job \(**Orchestration stage** field\).

        **Note:** The **Orchestration stage** field value of each step is case-sensitive and must match the original name of the corresponding Azure pipeline job.

<table id="table_qs3_nvm_wmb"><tbody><tr><td>

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

Azure pipeline job name \(case-sensitive\).

 **Note:** For step association with Azure pipeline jobs, the **Orchestration stage** field must be configured.

</td></tr><tr><td>

Business service

</td><td>

Configuration service that applies to the step.

</td></tr></tbody>
</table>        Once orchestration tasks are created, [associate](associate-pipeline-steps-dev-ops.md) each orchestration task in the Orchestration Tasks related list with a DevOps pipeline step.

4.  Enable change control automatically or manually.

    -   If you are using the ServiceNow DevOps extension for Azure DevOps, run your Azure DevOps pipeline to automatically enable change control.
    -   If you are configuring change control manually, select the **Change control** check box in a step to enable [change acceleration](../concept/dev-ops-change-acceleration.md) and the corresponding configuration fields. For Azure release \(CD\) pipelines, enable change control in the first step of the required stage only. Change control for Azure release \(CD\) pipelines is supported only in pre-deployment gates.

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
</table>        You can set up change control in your Azure DevOps YAML or Classic Azure pipeline using the [Azure Invoke REST API](../concept/dev-ops-azure-change-control-api.md) or the [ServiceNow DevOps extension for Azure DevOps](config-dev-ops-extensions-azure.md#).


## What to do next

[Configure the Azure pipeline for DevOps](../concept/config-azure-pipeline-dev-ops.md)

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)


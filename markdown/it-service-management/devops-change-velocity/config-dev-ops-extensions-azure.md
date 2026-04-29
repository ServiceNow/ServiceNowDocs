---
title: Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions
description: Install and configure DevOps extension for Azure DevOps to send build and release notifications from your Azure pipeline to DevOps Change Velocity.Use the ServiceNow DevOps extension for Azure DevOps to configure change control and artifacts and packages in your Azure build \(CI\) pipeline.Use the ServiceNow DevOps extension for Azure DevOps to configure change control, and artifacts and packages in your Azure release \(CD\) pipeline.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configuring the Azure pipeline for DevOps, Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions

Install and configure DevOps extension for Azure DevOps to send build and release notifications from your Azure pipeline to DevOps Change Velocity.

## Before you begin

Role required: sn\_devops.admin

## About this task

You can use **ServiceNow DevOps** extension on [Visual Studio Marketplace - Extensions for Azure DevOps](https://marketplace.visualstudio.com/azuredevops) to integrate your Azure pipeline with the ServiceNow DevOps application. For more information about artifacts and packages in DevOps Change Velocity, see [Artifacts and packages](../concept/using-dev-ops-release-change.md).

-   **ServiceNow DevOps** service connection

    Required to connect the Azure pipeline to ServiceNow

-   **ServiceNow DevOps Release Gate**

    Required to enable change control in Azure release \(CD\) pipelines \(in pre-deployment conditions only\).


Azure build \(CI\) pipeline custom tasks:

-   Agentless \(server\) job
    -   **ServiceNow DevOps Server Artifact Registration** custom task

        Required for agentless \(server\) jobs to register an artifact in the ServiceNow instance

    -   **ServiceNow DevOps Server Package Registration** custom task

        Required for agentless \(server\) jobs to register a package in the ServiceNow instance

    -   **ServiceNow DevOps Server Change Acceleration** custom task

        Required for agentless \(server\) jobs to automatically create a change request in ServiceNow Change Management as part of the Azure pipeline.

        **Note:** The **ServiceNow DevOps Server Change Acceleration** task does not require **ServiceNow DevOps Server Job Notification** tasks.

    -   **ServiceNow DevOps Server Get Change** custom task

        Required to retrieve the change request number in a pipeline based on specific change details for a server job.

    -   **ServiceNow DevOps Server Update Change** custom task

        Required to update the change request details associated with a pipeline for a server job.

-   Agent job

    -   **ServiceNow DevOps Agent Artifact Registration** custom task

        Required for agent jobs to register an artifact in the ServiceNow instance

    -   **ServiceNow DevOps Agent Package Registration** custom task

        Required for agent jobs to register a package in the ServiceNow instance

    -   **ServiceNow DevOps Agent Get Change** custom task

        Required to retrieve the change request number in a pipeline based on specific change details for an agent job.

    -   **ServiceNow DevOps Agent Update Change** custom task

        Required to update the change request details associated with a pipeline for an agent job.

    **Note:** The **ServiceNow DevOps Agent Artifact Registration** and **ServiceNow DevOps Agent Package Registration** tasks are not supported for Release pipelines.

-   Software Quality scans \(SonarQube/SonarCloud\)

    -   **ServiceNow DevOps Build Sonar Registration** custom task \(for Build pipelines\)
    -   **ServiceNow DevOps Release Sonar Registration** custom task \(for Release pipelines\)
    **Note:** The **ServiceNow DevOps Build Sonar Registration** task is not supported for Release pipelines.

-   Security scans:

    -   **ServiceNow DevOps Build Security Results** custom task \(for Build pipelines\)
    -   **ServiceNow DevOps Release Security Results** custom task \(for Release pipelines\)
    **Note:** The **ServiceNow DevOps Build Security Result** task is not supported for Release pipelines.


## Procedure

1.  Go to [Visual Studio Marketplace](https://marketplace.visualstudio.com/), search for the **ServiceNow DevOps** extension, and click **Get it free**.

    ![DevOps Azure extension](../image/dev-ops-azure-extension.png)

2.  Select your Azure DevOps organization and select **Install**.

3.  From your Azure DevOps project, navigate to **Project settings** &gt; **Pipelines** &gt; **Service connections**.

4.  Select **New service connection** and from the list select **ServiceNow DevOps**.

5.  Select **Next** and enter the following details:

<table id="table_mpl_d11_ykb"><tbody><tr><td>

Authentication method

</td><td>

Select whether authentication is done through the token-based or basic method.

</td></tr><tr><td>

ServiceNow instance

</td><td>

`https://<your-instance>.service-now.com/`

</td></tr><tr><td>

Tool ID

</td><td>

The sys\_id of the orchestration tool.

 You can copy this value using the `Copy sys_id` command on the Orchestration Tool form. If you are using the workspace, select **More form options \(![More form options icon](../image/more-form-actions-icon.png)\) &gt; Copy sys\_id** on the Azure DevOps tool connection form. If you are using Service Catalog or Classic, select **Additional actions \(![Additional actions icon](../image/additional-actions.png)\) &gt; Copy sys\_id** on the Azure DevOps tool connection form.

</td></tr><tr><td>

Username

</td><td>

Enter `devops.integration.user`.**Note:** The step to enter the integration user name and password is required to configure only when DevOps Config is installed or the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property is disabled. If this step is not required, webhooks are configured using token-based authentication.

</td></tr><tr><td>

Password

</td><td>

Password for DevOps Integration User.**Note:** The step to enter the integration user name and password is required to configure only when DevOps Config is installed or the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property is disabled. If this step is not required, webhooks are configured using token-based authentication.

</td></tr><tr><td>

API Token

</td><td>

API token for connection to the endpoint.

</td></tr><tr><td>

Service connection name

</td><td>

Enter `DevOps Connection`

</td></tr><tr><td>

Grant access permission to all pipelines

</td><td>

Select check box.

</td></tr></tbody>
</table>
## Example

![New Service Connection in Azure DevOps for basic authentication method](../image/azure-service-connection-basic.png "Azure pipeline - ServiceNow DevOps service connection basic authentication method")

![New Service Connection in Azure DevOps for token based authentication method](../image/azure-service-connection-token.png "Azure pipeline - ServiceNow DevOps service connection token based authentication method")

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

## Set up an Azure build \(CI\) pipeline in DevOps

Use the ServiceNow DevOps extension for Azure DevOps to configure change control and artifacts and packages in your Azure build \(CI\) pipeline.

### Before you begin

Role required: sn\_devops.admin

### Procedure

1.  Navigate to **Pipelines** in your Azure DevOps instance.

2.  Select the pipeline for which you want to enable change control.

3.  Select **View**.

    The YAML editor for the pipeline is displayed along with the **Tasks** search pane on the right.

4.  Search for the required custom action in the **Tasks** pane and select it.

<table id="table_a2l_311_ykb"><thead><tr><th>

Custom action

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

**ServiceNow DevOps Server Change Acceleration**

</td><td>

1.  In the **Display name** field, enter **ServiceNow Change Acceleration**.
2.  In the **ServiceNow endpoint** field, enter `My Connection`.
3.  In the **Upstream job executed** field, enter the value that indicates the previous job in line. For example, the job before Server might be `Test`.
4.  In the **Change request details** field, set [closure code and change request fields](../concept/dev-ops-config-change-details.md) from within the pipeline.
 Select the information icon to view sample output. For more information regarding change acceleration, see [change acceleration](../concept/dev-ops-change-acceleration.md).

</td></tr><tr><td>

**ServiceNow DevOps Agent Artifact Registry**

</td><td>

1.  In the **ServiceNow endpoint** field, enter `My Connection`.
2.  In the **Artifacts payload** field, enter the JSON containing list of artifacts.
 For more information regarding artifacts, see [Artifacts and packages](../concept/using-dev-ops-release-change.md).

</td></tr><tr><td>

**ServiceNow DevOps Agent Package Registry**

</td><td>

1.  In the **ServiceNow endpoint** field, enter `My Connection`.
2.  In the **Package name** field, enter the name of the package that contains artifacts.
3.  In the **Artifacts payload** field, enter the JSON containing build details and list of artifacts.
 For more information regarding artifacts, see [Artifacts and packages](../concept/using-dev-ops-release-change.md).

</td></tr><tr><td>

**ServiceNow DevOps Server Get Change**

</td><td>

[Get and update change request details in Azure DevOps pipeline](update-change-request-details-in-an-azure-devops-pipeline.md)

</td></tr><tr><td>

**ServiceNow DevOps Server Update Change**

</td><td>

[Get and update change request details in Azure DevOps pipeline](update-change-request-details-in-an-azure-devops-pipeline.md)

</td></tr><tr><td>

**ServiceNow DevOps Agent Get Change**

</td><td>

[Get and update change request details in Azure DevOps pipeline](update-change-request-details-in-an-azure-devops-pipeline.md)

</td></tr><tr><td>

**ServiceNow DevOps Agent Update Change**

</td><td>

[Get and update change request details in Azure DevOps pipeline](update-change-request-details-in-an-azure-devops-pipeline.md)

</td></tr></tbody>
</table>5.  Select **Add**, to add the custom task to the Tasks section of your Azure pipeline.


### Example

![DevOps Azure Change extension](../image/dev-ops-azure-change-server.png "Azure pipeline: ServiceNow DevOps Change Acceleration custom task")

![DevOps ServiceNow Change Acceleration extension](../image/dev-ops-azure-job-config-all.png)

![Azure DevOps server custom tasks](../image/dev-ops-yaml-server.png)

![DevOps Azure change details](../image/dev-ops-azure-change-details.png "Change request details example")

## Set up an Azure release \(CD\) pipeline in DevOps

Use the ServiceNow DevOps extension for Azure DevOps to configure change control, and artifacts and packages in your Azure release \(CD\) pipeline.

### Before you begin

Role required: sn\_devops.admin

### About this task

**Note:** Change control in Azure release \(CD\) pipelines is supported in pre-deployment gates only. Pre-deployment gate change requests are mapped to the step execution of the first job in that stage.

Phases in an Azure release pipeline are mapped to a step. The step name for a multi-config or multi-agent job must include the phase name only, and not the actual job name derived at pipeline execution run time.

Task executions for skipped jobs are marked as failed.

### Procedure

1.  In Azure DevOps Pipelines, select **Pipelines &gt; Releases**, and then select your release pipeline.

2.  Select **Edit** to open the pipeline editor.

3.  Select the pre-deployment \(![Pre-deployment icon](../image/pre-deployment-icon.png)\)icon for your stage, and then select the toggle button to enable **Gates**. ![Enable Gates in Pre-deployment conditions](../image/deployment-enable-gates.png)

4.  Select **+Add**, and select **ServiceNow DevOps Release Gate**. ![Add ServiceNow DevOps Release Gate](../image/ado-release-gate-add.png)

5.  Select **ServiceNow DevOps Release Gate** and select the ServiceNow endpoint. ![ServiceNow DevOps Release Gate fields](../image/ado-release-gate-servicenow-endpoint.png)

6.  Exit the release gate configuration, and expand the Evaluation options section to configure the following timing fields.

<table id="table_tg3_2hq_wmb"><tbody><tr><td>

The time between re-evaluation of gates

</td><td>

Re-evaluation interval in minutes, hours, or days.

 If the change request is canceled or rejected, the Azure pipeline release gate keeps re-evaluating the change request status at the configured interval until timeout.

 No user intervention is required for further attempts of re-evaluation after the change request has already been approved, rejected, or canceled.

</td></tr><tr><td>

The timeout after which gates fail

</td><td>

Timeout value in minutes, hours, or days.If the pre-deployment conditions fail, the subsequent jobs of the stage are marked as failed, and the start and end time defaults to the current system time.

</td></tr></tbody>
</table>    ![DevOps Azure gate config](../image/dev-ops-azure-gate.png "Azure release pipeline pre-deployment gate configuration")

7.  Configure artifacts in your Azure release \(CD\) pipeline.

    To set up artifacts using the build pipeline as the source, these names must match.

    -   Repository name, and build pipeline name \(for example, DeployableRepo\).
    -   Name property of the build pipeline artifact, and source alias property of the release pipeline artifact \(for example, BuildDrop\).
    In addition to the build pipeline, you can select artifacts from any other eight sources. To track commit &amp; work item details, follow these rules.

    -   When the source is the build pipeline, the `semantic version` property of the artifacts should be in the format `MAJOR.MINOR.PATCH` \(for example 5.1.3\).
    -   When the source is not the build pipeline, define a `semantic version` by implementing the **DevOpsArtifactSemanticVersionAPI** extension interface.
    See [Artifacts and packages](../concept/using-dev-ops-release-change.md) for more information regarding artifacts.


### Example

![DevOps artifact YAML config](../image/dev-ops-artifact-repo-yaml.png "Artifact setup - build pipeline source")

![DevOps artifact pipeline config](../image/dev-ops-artifact-build-pipeline.png "Artifact setup - release pipeline")


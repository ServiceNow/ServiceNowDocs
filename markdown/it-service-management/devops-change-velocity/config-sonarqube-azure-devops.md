---
title: Configure SonarQube scans on Azure DevOps pipelines
description: Configure SonarQube or SonarCloud scans on MS Azure DevOps pipelines. Check Azure DevOps pipeline executions for SonarQube scans on every stage of the pipeline's execution and fetch lists and details of scans from any stage to DevOps Change Velocity. Drill down on the Scan Details based on categories.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure SonarQube scans on Azure DevOps pipelines

Configure SonarQube or SonarCloud scans on MS Azure DevOps pipelines. Check Azure DevOps pipeline executions for SonarQube scans on every stage of the pipeline's execution and fetch lists and details of scans from any stage to DevOps Change Velocity. Drill down on the Scan Details based on categories.

## Before you begin

Ensure that you meet the following prerequisites before you configure SonarQube scans on your Azure DevOps pipeline:

-   You are using a compatible SonarQube version. See [DevOps Change Velocity integrations](../concept/dev-ops-overview.md) for supported tool versions.
-   Connect, configure the Azure DevOps tool and discover existing repositories, orchestration tasks, and pipelines.
-   Create a SonarQube tool record. For more information, see [SonarQube integration with DevOps Change Velocity](../concept/sonarqube-devops-integration-devops.md).
-   Install the SonarQube extension from the Visual Studio Marketplace and configure branch analysis to use the Azure Devops tasks in your build definitions to analyze your projects. For more information, see [SonarQube documentation](https://docs.sonarqube.org/latest/analysis/azuredevops-integration/).
-   Install the following custom extension tasks on your Azure DevOps instance.
    -   ServiceNow extension to integrate Azure Pipelines with DevOps Change Velocity. For more information, see [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](config-dev-ops-extensions-azure.md#).
    -   ServiceNow DevOps Build Sonar Registration \(for Build pipelines\)
    -   ServiceNow DevOps Release Sonar Registration task \(for Release pipelines\)

Role required:

-   admin or sn\_devops.admin in DevOps Change Velocity
-   admin in Azure DevOps
-   admin role in SonarQube with access to all projects that the SonarQube scans are configured on.

## About this task

By default, Azure DevOps provides you with the following tasks to run a SonarQube scan on build and release pipelines:

-   Prepare analysis on SonarCloud
-   Run Code analysis
-   Publish Quality Gate Result

Add and configure custom ServiceNow extension tasks in order to them default tasks, to fetch the scan details to ServiceNow DevOps from Azure DevOps build and release pipelines. The scan details that are fetched are:

-   pipelineName
-   buildNumber
-   stageName
-   branchName
-   sonarProjectKey
-   sonarInstanceUrl

## Procedure

1.  Set up and configure the Azure DevOps and SonarQube Integration to fetch scan analysis from Build pipelines.

    1.  In the Azure DevOps console, navigate to **Organization** &gt; **SonarIntegrations** &gt; **Pipelines** &gt; **Jobs**.

    2.  Click the **Add Tasks** icon \(![Add additional tasks](../image/add-task-ado-sonar.png)\), and search for the ServiceNow extensions in the **Add tasks** search bar.

    3.  Add the following tasks.

        -   ServiceNow DevOps Build Sonar Registration task.
        -   ServiceNow DevOps Release Sonar Registration task.
    4.  On the form, fill in the fields.

<table id="table_kyj_x2t_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Auto-populates on entering key and URL.

</td></tr><tr><td>

ServiceNow endpoint

</td><td>

The ServiceNow instance endpoint that is automatically created during Tool configuration. Use the same service connection for this task.

</td></tr><tr><td>

Sonar project Key

</td><td>

Enter the same project key value which you used while configuring the **Prepare analysis on SonarCloud** task.

</td></tr><tr><td>

Sonar Instance Url

</td><td>

Enter the same URL which you used to connect to the Sonar tool during tool creation.

</td></tr><tr><td>

Job Name

</td><td>

The name of the Azure DevOps pipeline job. This field appears only for the **ServiceNow DevOps Release Sonar Registration** task.

</td></tr></tbody>
</table>        **Important:** In the list of tasks for the pipeline job, ensure that the **ServiceNow DevOps Build Sonar Registration** or **ServiceNow DevOps Release Sonar Registration** task is added after the **Run Code Analysis** task.

    You have configured the build pipelines to send sonar scan results to your DevOps application. Scan results are mapped to the Software Quality capability are processed by an associated base system sub flow \(**FetchSonarScanId**\), once an event is created and processed in the Inbound Events table.

2.  Associate Azure pipelines steps in DevOps.

3.  Run the pipeline.


## Result

Based on the scan results on various stages of pipeline's execution, the results are shown in the corresponding step of the pipeline in ServiceNow DevOps. Inbound events are created for notifications and subflows are triggered based on the notification type and capability.

## What to do next

-   View scan details as part of Task Executions. View details of all the Sonar scans that are part of the task execution mapped to a build or release pipeline execution step.

    1.  Navigate to **DevOps** &gt; **Orchestrate** &gt; **Task Execution** click a relevant Task Execution record.
    2.  Click the Software Quality Summary related list.
    3.  Click a relevant Scan ID record.
    The Software Quality Scan Summary and Scan Details are displayed.

-   View scan details as part of Change Request. View all the scans that were part of this build/release pipeline in the **Software Quality Results** &gt; **Software Quality Summary** related list.

    1.  Navigate to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Change Requests**
    2.  Click the Software Quality Summary related list.
    3.  Click a relevant Scan ID record.
    The Software Quality Scan Summary and Scan Details are displayed.


**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)


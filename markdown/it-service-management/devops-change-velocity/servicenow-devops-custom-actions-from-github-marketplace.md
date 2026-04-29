---
title: ServiceNow DevOps custom actions from GitHub marketplace
description: Use the custom actions from the GitHub marketplace to collect SonarQube scan data, security data, pause or resume workflow, or resume workflow until a change request is approved or rejected in your instance, or get and update change request details and so on.Save the SonarQube scan results of a project initiated by the workflow run in your ServiceNow instance. You must create the SonarQube tool in your instance and use the ServiceNow DevOps SonarQube custom action at the steps level of a job in the workflow.Save unit test results of the project initiated by the workflow run in your ServiceNow instance. The ServiceNow DevOps Test Report custom action must be used at the steps level of job in the workflow.Save artifacts created or deployed by the workflow run in your ServiceNow instance. Use the ServiceNow DevOps Register Artifact custom action at steps level of job in the workflow.Save packages created or deployed by the workflow run in the ServiceNow instance. Use the ServiceNow DevOps Register Package custom action at steps level of job in the workflow.Create a change request in the ServiceNow instance to pause and resume the workflow run from the ServiceNow instance.Retrieve the change request number in a GitHub Actions pipeline based on specific change details.Update change request details associated with a GitHub Actions pipeline.Retrieve security scan results in ServiceNow.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# ServiceNow DevOps custom actions from GitHub marketplace

Use the custom actions from the GitHub marketplace to collect SonarQube scan data, security data, pause or resume workflow, or resume workflow until a change request is approved or rejected in your instance, or get and update change request details and so on.

Alternatively, you can use Docker container images to implement custom actions for GitHub Actions pipelines. For more information, see [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md).

**Parent Topic:**[GitHub integration with DevOps Change Velocity](github-integration-dev-ops.md)

## ServiceNow DevOps SonarQube custom action

Save the SonarQube scan results of a project initiated by the workflow run in your ServiceNow instance. You must create the SonarQube tool in your instance and use the ServiceNow DevOps SonarQube custom action at the steps level of a job in the workflow.

View the SonarQube analysis results using one of the following methods:

-   Navigate to **DevOps** &gt; **Software Quality Results** &gt; **Software Quality Summary**.
-   Navigate to **DevOps** &gt; **Orchestrate** &gt; **Task Execution** and selecting a relevant **Task Execution** record.

Perform the following tasks to use the custom action.

-   Create SonarQube tool in your instance.

    Generate token from **User** &gt; **My Account** &gt; **Security** page in your SonarQube tool and create tool in the ServiceNow instance using the generated token. For more information, see [Onboard SonarQube to DevOps Change Velocity — Workspace](../task/sonar-connect-workspace.md) and [Onboard SonarQube to DevOps Change Velocity — Classic](../task/create-sonar-tool-devops.md).

-   Create the following Secrets to save SonarQube scan results in the ServiceNow instance.
    -   SONAR\_HOST\_URL: SonarQube instance URL. For example, `https://sonarcloud.io`
    -   SONAR\_PROJECT\_KEY: The key to identify a project in the SonarQube instance. For example, `org.examples:demo`
-   Configure the ServiceNow DevOps SonarQube custom action in the workflow.

    The custom action `servicenow-devops-sonar` must be configured at steps level of job in the workflow with **uses** keyword. The inputs of this custom action must not be tampered to save SonarQube analysis results in the ServiceNow instance. For more information, see [ServiceNow DevOps Sonar](https://github.com/marketplace/actions/servicenow-devops-sonar-scan-results).


## ServiceNow DevOps Test Report custom action

Save unit test results of the project initiated by the workflow run in your ServiceNow instance. The ServiceNow DevOps Test Report custom action must be used at the steps level of job in the workflow.

View the unit test results saved in your ServiceNow instance by navigating to **DevOps** &gt; **Test Results** &gt; **Test Summaries**.

You can also view by navigating to **DevOps** &gt; **Orchestrate** &gt; **Task Execution** and clicking a relevant **Task Execution** record.

Perform the following tasks to use the custom action.

-   Create Secrets in the GitHub Repository.
-   Configure the DevOps Test Report custom action in the workflow.

    The custom action `servicenow-devops-test-report` must be configured at steps level of job in the workflow with **uses** keyword. The inputs of this custom action must not be tampered to save the unit test results in your ServiceNow instance. For more information, see [ServiceNow DevOps Test Report](https://github.com/marketplace/actions/servicenow-devops-unit-test-results).


## ServiceNow DevOps Register Artifact custom action

Save artifacts created or deployed by the workflow run in your ServiceNow instance. Use the ServiceNow DevOps Register Artifact custom action at steps level of job in the workflow.

View the artifacts details saved in your instance by navigating to **DevOps** &gt; **Artifact** &gt; **Artifacts**.

Perform the following tasks to use the custom action:

-   Create Secrets in the GitHub Repository.
-   Configure ServiceNow DevOps Register Artifact custom action in the workflow.

    The custom action `servicenow-devops-register-artifact` must be configured at steps level of job in the workflow with **uses** keyword. The inputs of this custom action must not be tampered to save artifact details in your instance. For more information, see [ServiceNow DevOps register artifacts](https://github.com/marketplace/actions/servicenow-devops-register-artifact).


## ServiceNow DevOps Register Package custom action

Save packages created or deployed by the workflow run in the ServiceNow instance. Use the ServiceNow DevOps Register Package custom action at steps level of job in the workflow.

View the package details saved in the ServiceNow instance by navigating to **DevOps** &gt; **Artifact** &gt; **Packages**.

Perform the following tasks to use the custom action.

-   Create Secrets in the GitHub Repository.
-   Configure ServiceNow DevOps Register Artifact custom action in the workflow.

    The custom action `servicenow-devops-register-package` must be configured at steps level of job in the workflow with **uses** keyword. The inputs of this custom action must not be tampered to save artifact details in your instance. For more information, see [ServiceNow DevOps register package](https://github.com/marketplace/actions/servicenow-devops-register-package).


## ServiceNow DevOps Change Automation custom action

Create a change request in the ServiceNow instance to pause and resume the workflow run from the ServiceNow instance.

Use the ServiceNow DevOps Change Automation custom action at steps level of job in the workflow. If the change is not created within the time period specified in the threshold \(changeCreationTimeOut\), and the **abortOnChangeCreationFailure** parameter is enabled, the pipeline will be aborted.

This custom action creates a change request in ServiceNow, enables the **Change Control** option, and polls the ServiceNow instance at the defined time interval for change status until either the change is approved or rejected or the timeout threshold \(timeout\) is reached. GitHub aborts the workflow run if the timeout threshold is reached and the **abortOnChangeStepTimeout** parameter is enabled. ![GitHub Actions console - change step timeout](../image/github-actions-console-2.png)

This custom action immediately resumes the workflow run when change receipt is enabled for pipeline in ServiceNow without waiting for the change to be approved or rejected in the ServiceNow instance.

View the change created for the workflow run in the ServiceNow instance by navigating to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Change Requests**.

The change number with status **pending\_decision** is displayed in the GitHub Actions console while polling the ServiceNow instance for change status. The details like change comments, approved by, approved on, and status are logged in GitHub Actions console after the change is approved or rejected or canceled by the user in the ServiceNow instance. ![GitHub Actions console - change approved](../image/github-action-console1.png)

You can navigate to the console logs in your pipeline to view the state of a change request when a change request is created, change details will be displayed as per the polling time interval. The policy conditions associated with the change request state will also be evaluated and displayed in the logs. For example, if the DevOps Change Request Advanced Automation policy is activated, the policy conditions will be evaluated and the corresponding decision made \(auto-approve/auto-reject/manual-approval\) will be displayed in the logs.

The following change request details are displayed:

-   number
-   details
-   status
-   sys\_id
-   type
-   risk
-   priority
-   changeState
-   plannedStartDate
-   plannedEndDate
-   changeRequestURL

![Change state in GitHub pipeline console logs](../image/github-change-state.png)

**Note:** **changeState** is the state of the change request, and **status** is the status of the step execution.

The logs for policy conditions will be displayed for the base system change flows as follows:

-   DevOps Model Change Policy: Only logs will be displayed on change creation and when the change state is updated.
-   DevOps Change Request Minimal Automation Policy: Logs along with change decision and policy conditions corresponding to the change decision will be displayed.
-   DevOps Change Request Advanced Automation Policy: Logs along with change decision and policy conditions corresponding to the change decision will be displayed.

The change policy input and decision conditions are stored in the Decisions \[sys\_decision\_question\] table. Logs will be displayed if the following fields and operators are used as input for policy conditions:

-   **Fields**
    -   code\_coverage
    -   commits\_without\_work\_item
    -   integration\_tests\_failed
    -   load\_tests\_failed
    -   regression\_tests\_failed
    -   num\_of\_outages\_in\_last\_7\_days
    -   num\_of\_current\_outages
    -   num\_of\_open\_incidents
    -   total\_num\_of\_commits
    -   tests\_passing\_percent
    -   risk
    -   code\_security
    -   commits
-   **Operators**
    -   &lt;=
    -   &gt;=
    -   !=
    -   =
    -   &lt;
    -   &gt;
    -   ISNOTEMPTY
    -   ISEMPTY
    -   BETWEEN
    -   ANYTHING
    -   NSAMEAS
    -   SAMEAS
    -   GT\_FIELD
    -   LT\_FIELD

**Note:** If any field is modified in a change policy other than the base system fields, then those fields must be manually added to the flow for policy conditions to be evaluated.

Perform the following tasks to use the custom action.

-   Create Secrets in the GitHub Repository.
-   Configure ServiceNow DevOps Change Automation custom action in the workflow.

    The custom action `servicenow-devops-change` must be configured at steps level of job in the workflow with **uses** keyword. The inputs of this custom action must not be tampered to create change in your instance and poll for change status every number of seconds. For more information, see [ServiceNow DevOps change automation](https://github.com/marketplace/actions/servicenow-devops-change-automation).


## ServiceNow DevOps Get Change Github Action

Retrieve the change request number in a GitHub Actions pipeline based on specific change details.

The [ServiceNow DevOps Get Change Github Action](https://github.com/ServiceNow/servicenow-devops-get-change) custom action must be added at the step level in a pipeline job to retrieve the change request number from a ServiceNow instance by specifying change details.

## ServiceNow DevOps Update Change Github Action

Update change request details associated with a GitHub Actions pipeline.

The [ServiceNow DevOps Update Change Github Action](https://github.com/ServiceNow/servicenow-devops-update-change) custom action must be added at the step level in a pipeline job to update the change request in a ServiceNow instance. The change request number whose details need to be updated and the change request details to be updated must be specified as input.

## ServiceNow DevOps Security Results Action

Retrieve security scan results in ServiceNow.

The [ServiceNow DevOps Security Results Action](https://github.com/ServiceNow/servicenow-devops-security-result) custom action must be added at the step level in a pipeline job to retrieve security scan results in ServiceNow.


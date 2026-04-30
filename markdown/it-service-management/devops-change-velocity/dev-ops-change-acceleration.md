---
title: Accelerating your DevOps change process
description: Enable the change acceleration feature of DevOps Change Velocity for automatic change request creation in your pipeline, and use change approval flows and policies to automate approval under certain conditions.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 17
breadcrumb: [DevOps Change Velocity, IT Service Management]
---

# Accelerating your DevOps change process

Enable the change acceleration feature of DevOps Change Velocity for automatic change request creation in your pipeline, and use change approval flows and policies to automate approval under certain conditions.

**Note:** ServiceNow [Change Management](../../change-management/concept/c_ITILChangeManagement.md) must be installed for change acceleration.

Enable and set up change control when you model your pipeline in DevOps:

-   [Model an Azure pipeline in DevOps](../task/model-azure-pipeline-dev-ops.md)
-   [Model a GitLab basic CI pipeline in DevOps](../task/model-gitlab-pipeline-dev-ops.md)
-   [Model a Jenkins pipeline in DevOps](../task/model-jenkins-pipeline-dev-ops.md)

You can view details for active change requests by navigating to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Change Requests**.

## Change control process

When change control is enabled for a job in your DevOps development pipeline, a change request is automatically created and set to Assess state to request approval for the execution of the current stage or job if an assignment group is added for the change request. Change requests can be approved automatically by configuring conditions in a change approval policy.

Pipeline steps can be configured to enable change receipts, which do not pause the pipeline. Change requests created with change receipts enabled include all pipeline data, but do not require approval to proceed in the pipeline and the change request will be in post implement states. For change requests created without enabling change receipt, the pipeline will be paused until the change request is approved, and upon approval, the pipeline will be resumed.

If you want to stop the automatic transition of the change request states even when change receipt is turned on, you must disable the sn\_devops.enable\_change\_receipt\_state\_transition property. For more information, see [DevOps Change Velocity properties](dev-ops-administration.md).

Once approved, either automatically or manually, change requests move to Implement state and the job is run. Once the job is run, the change request is moved to the closed state with Close code as successful on a successful job run or Unsuccessful on error in the job run. For information on customizing your change request states, see [Custom change request process](dev-ops-change-acceleration.md#section_www_tzz_jjb).

If a change request is not approved and moved to the canceled or closed state, the associated Jenkins, GitHub, or ADO job is marked as failed and a console message is shown:

For Jenkins: `[ServiceNow DevOps] Job was not approved for execution`

For GitHub: `Error: **** Change has been created but the change is either rejected or cancelled`

For ADO: `"changeState":"Closed"`

## Automatic approval of change requests using flows and policies

You can automate the change approval process for all your DevOps change requests. DevOps Change Velocity uses flows and DevOps data \(such as work items, commits, code coverage, code security, risk, and test results\) to update the state of a change request and automatically approve it based on change approval policies. Three flows are available in the base system that you can clone, customize, and activate \(in Flow Designer\). By default, the DevOps Change Request Manual Approval Flow is activated. DevOps flows are applicable to only automatically created change requests or change requests that have change receipt turned off.

## Flows

A flow is an automated process consisting of a trigger \(which specifies when to run the flow\) and a sequence of reusable actions \(where the actions perform a sequence of operations on your data\). Flows are built in Flow Designer, a ServiceNow AI Platform feature that enables process automation. For more information, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

You can use one of the DevOps flows available in the base system as a template; clone the flow and customize it to your business requirements. Ensure that only one DevOps flow is in the active state at any time to avoid conflicts and errors. A DevOps flow is applicable to change requests that have the DevOps category or if the devops\_change property is set to true. \(An automatically created DevOps change request sets the category to DevOps by default\).

By default, the flows are configured to update the state of the step execution based on the change request state, and any additional default behavior. Based on the step execution state, a callback is made to the pipeline:

-   If the DevOps change request is approved, the flow will update the step execution state to approved, and the change request state is updated to implement. After that the pipeline will be resumed.
-   If the DevOps change request is rejected, the flow will update the step execution state to rejected, and the change request state is updated to new. After that the pipeline will be terminated.
-   If the DevOps change request is canceled, the flow will update the step execution state to canceled by user, and the change request is updated to canceled. After that the pipeline will be canceled.

If a business rule or data policy causes an error while updating a change in the DevOps Change Request Manual Approval Flow, DevOps Change Request Minimal Automation Approval Flow, or DevOps Change Request Advanced Automation Approval Flow, the corresponding error will be displayed in the worknotes of the change request and logged in the console logs of the pipeline tool.

<table id="table_xlb_syr_zyb"><thead><tr><th>

DevOps flow

</th><th>

Default behavior

</th></tr></thead><tbody><tr><td>

DevOps Change Request Manual Approval Flow

</td><td>

This flow is activated by default. With this flow, DevOps change requests must go through a manual approval process, where the flow waits for the change request to reach an eligible state \(rejected, implemented, or specific implementation state\). When reached, this flow will update the state of the step execution based on the state of the change request.

 If the change request is type-based, the flow will wait for the change to get rejected, implemented, or canceled. If the change request is model-based, the flow will wait for the change to get rejected, get canceled, or reach one of the implementation states defined in the model or the implement state specified in the DevOps property. This flow won’t trigger for DevOps change requests whose model is a base system DevOps change model \(DevOps or DevOps simplified\) to avoid conflicts and errors. ![DevOps Change Request Manual Approval Flow](../image/change-manual-flow.png)

 You can clone this flow and customize it to make changes. Ensure that the other DevOps flows are deactivated.

</td></tr><tr><td>

DevOps Change Request Minimal Automation Approval Flow

</td><td>

This flow gathers DevOps data and runs the DevOps Change Request Minimal Automation Policy, which determines if the change should be auto-rejected, auto-approved, or sent for manual approval. This flow is triggered for DevOps change requests whose type or model is set to normal.

 Activate this flow if you want to automate change request approvals, but start minimally. ![DevOps Change Request Minimal Automation Approval flow](../image/change-minimal-automation-flow.png)

 You can clone this flow and customize it to make changes. Ensure that the other DevOps flows are deactivated.

 You can also add the DevOps - Update Minimal Automation Policy Decision Reason action to this flow to update the policy decisions to the step execution change comment and the change request worknotes to know the reasons for the decision. You can add this action inside every decision block and specify the required input. ![Update minimal automation policy decision action](../image/action-minimal-automation-policy.png)

</td></tr><tr><td>

DevOps Change Request Advanced Automation Approval Flow

</td><td>

This flow gathers DevOps data and runs the DevOps Change Request Advanced Automation Policy, which determines if the change should be auto-rejected, auto-approved, or sent for manual approval. This flow is triggered for DevOps change requests whose type or model is set to normal.

 If the DevOps change request is approved, the flow will update the change request to the scheduled state, and the planned start date will be used to set the change request start date. On the change request start date, the flow will update the change request state to implement. After that the pipeline will be resumed. Activate this flow if you want to automate change request approvals with a robust change policy. ![DevOps Change Request Advanced Automation Approval Flow](../image/change-flow-advanced.png)

 You can clone this flow and customize it to make changes. Ensure that the other DevOps flows are deactivated.

</td></tr><tr><td>

DevOps  Demo  Change Automation flow 

</td><td>

When demo data is installed, the  DevOps  Demo  Change Automation flow  is available where  normal type of change request or normal model change request can be auto-approved based on the decision policies.  As a part of demo data, the decision policies available are: -   DevOps Low Risk Auto Approval policy, where the failed test count is zero  .
-   DevOps High risk manual approval policy, where the failed test count is greater than zero .

![DevOps Demo Change Automation flow](../image/dev-ops-demo-chg-automation-flow.png) You can clone this flow and customize it to make changes. Ensure that the other DevOps flows are deactivated.

</td></tr></tbody>
</table>To read guidelines on how to use flows, subflows, and actions more effectively, see [General guidelines for Workflow Studio flows, subflows, and actions](https://www.servicenow.com/docs/access?context=design-considerations-consolidated&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Change approval policies

A change approval policy is a course of action that can be applied to a change request. It consists of the following:

-   Policy input: Variable sources evaluated within a condition.
-   Decisions: Determines whether the change approval definition must be applied based on conditions.
-   Approval definitions: Defines the type of approval that can be applied.

The DevOps Change Request Minimal Automation Policy and DevOps Change Request Advanced Automation Policy are available by default. The three normal change policies available are:

-   DevOps Model Change Policy
-   DevOps Change Request Minimal Automation Policy
-   DevOps Change Request Advanced Automation Policy

For more information on change approval policies, see [Change approval policies](../../change-management/concept/change-approval-policy.md).

The DevOps automated approval flows use change approval policies and DevOps data \(such as work items, commits, pull requests, test summaries, security summaries, and quality summaries\) to automatically update the change record state and step execution state to approved, rejected, or canceled. You can view and edit these policies based on your business requirements, or create your own in the decision table. See the following decision tables.

The DevOps Change Request Minimal Automation Policy has the following conditions and criteria by default: ![Change Request Minimal Automation Policy conditions](../image/change-policy-minimal.png)

The DevOps Change Request Advanced Automation Policy has the following conditions and criteria by default:![Change Request Advanced Automation Policy conditions](../image/change-policy-advanced.png)

The three outcomes for the DevOps Change Request Minimal Automation and DevOps Change Request Advanced Automation policies \(depending on the conditions that you specify\) are:

-   Auto approval: If the conditions specified in the policy are met, the change request is automatically approved.
-   Auto reject: If one or more of the conditions specified in the policy are not met, the change request is automatically rejected.
-   Manual approval: If one or more conditions need manual approval by a user or group, that is specified in the policy. Notifications are sent by the policy to the relevant users or groups to expedite the manual approval and progress the change request.

You can apply your change approval policy in the Change Management Workflow Studio action to control the approval process for a change request. For more information, [Use the Apply Change Approval Policy flow action](../../change-management/task/use-apply-change-approval-policy-flow-activity.md).

## Change approval work notes

When a change request is updated based on a flow and change approval policy, the work notes associated with the change request are updated to one of the following hard-coded messages:

-   Change Approval Policy not found. Change Request has been rejected \(%s\).
-   %s is inactive. Change Request has been rejected \(%s\).
-   No Decisions matched. %s has been skipped \(%s\).
-   No approvals were generated from matched Decisions. %s has been skipped \(%s\).
-   Change Request has been rejected by %s \(%s\).
-   Change Request has been approved by %s \(%s\).

The work notes are updated based on a logic which uses the combination of one of the hard-coded messages + the policy name + action label used in the flow associated with the change request. In this combination, you can change only the value of policy name and the action label but not the hard-coded message. For example,

```
if (APPROVED.equals(state))
38 message = String.format(APPROVED_MSG, policyName, actionLabel);
```

## Default Change Handler subflow

Use the Default Change Handler subflow to populate these change request fields with default values.

-   Requested by
-   Justification
-   Implementation Plan
-   Backout plan
-   Test Plan
-   Short Description
-   Description
-   Start Date
-   End Date
-   Risk Impact Analysis

The Default Change Handler subflow overrides the field values that were populated using a template while creating the change request record.

If desired, you can write a custom subflow in place of this flow by modifying the **\[sn\_devops.change\_request\_handler\_subflow\]** [DevOps property](dev-ops-administration.md).

## Custom change request templates

When you enable change control in the ServiceNow DevOps step , you can select a custom template to populate fields automatically while creating the change request. The change request **Category** field is automatically set to DevOps.

**Note:** Do not configure the **Category** and **changeType** fields from the custom template.

The type of change request corresponds to the change request table in global scope.

## Automatic change request related lists

For a change request automatically created by DevOps, the **Category** field is automatically set to DevOps, and these related lists are added:

-   **Commits**

    Commits associated with the change request.

-   **Work Items**

    Work items associated with the change request.

-   **Artifact Versions**

    List of artifact versions associated to the package linked to pipeline execution for packages created before the change request is approved.

    If no package is linked to the pipeline execution, then the list is empty.

-   **Test Summaries \(replaces Test Results related list\)**

    List of test summaries for a pipeline execution associated with an artifact, package, or task execution before the change request.

    See [Test Results](dev-ops-change-acceleration.md#section_ccp_nbb_dlb) for more details.

-   **Software Quality Summary**

    List of software quality summaries for a pipeline execution associated with an artifact, package, or task execution before the change request.

-   **Security Summaries**

    List of security summaries for a pipeline execution associated with an artifact, package, or task execution before the change request.

    **Note:** Security scan results on the change record associated to a pipeline execution with a linked package are also displayed in the Security Summaries tab.


![DevOps Change Related Lists](../image/dev-ops-change-rel-lists.png)

**Note:** Implementation details from the orchestration tool are automatically added to the **Work notes** field on the change request form. Detail added to the work notes is limited to 5 KB of the task execution log for the step.

## Custom change request process

These [DevOps change properties](dev-ops-administration.md) are available to customize your change request flow.

-   DevOps change request implement state
-   DevOps change request post implement state
-   DevOps change request cancel state
-   DevOps change request approval text

To customize your change request flow, you must first create a **System Definition** &gt; **Choice List**. For example, `DevOps_Implement (value - 10)`.

Then, add the choice list to **System Definition** &gt; **Script Include** &gt; **ChangeRequestStateHandlerSNC**.

Once you have created the choice list and added it to the script include, you can update [DevOps change properties](dev-ops-administration.md) with the new choice list values. For example, **DevOps change request implement state** `-10`.

## DevOps Risk Condition

You can use the DevOps risk and impact calculation based on committer risk score.

This condition is inactive by default.

## Test Results related list

Lists the tests that were run in a pipeline after a package was created. If no package was created, then the list includes the tests that were run after an artifact version was created.

Scenarios:

-   **A package is created in the pipeline, but no artifact versions are registered.**
    -   If the change request is created in the package creation stage:

        No test results are displayed because a package is not yet linked to the pipeline execution.

    -   If the change request is created in a stage after the package creation stage:

        Build test summaries include those associated with stages after the package creation stage, up to the change-controlled stage.

-   **Artifact versions are registered, but no package is created.**
    -   If the change request is created in the artifact version stage:

        No test results will be displayed, because no tests are associated until the task execution is completed.

    -   If the change request is created in a stage after the artifact version stage:

        Build test summaries include those in the artifact version stage, as well as the stages afterward, up to the change-controlled stage.

-   **Both artifact versions and package are created in the pipeline.**
    -   If the change request is part of the stage after artifact version and package creation stages:

        Build test summaries include those associated with the package creation stage, as well as the stages afterward, up to the change-controlled stage.

    -   If the change request is part of the package creation stage, and artifact versions are created as part of an earlier stage;

        -   or the change request is created in a stage \(not package creation\) after the artifact version stage, but before package creation stage;
        -   or the change request is part of the package creation stage and artifact versions are created as part of an earlier stage:
        Build test summaries include those associated with the artifact version stage, as well as stages afterward, up to the change-controlled stage.


## Pipeline executions view

You can view pipeline activity by navigating to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Executions**.

![DevOps pipeline execution](../image/dev-ops-pipeline-executions.png)

-   **[Customizing DevOps flows](using-dev-ops-model-change-flow.md)**  
Customize or recreate the DevOps Change Request Manual Approval, DevOps Change Request Minimal Automation Approval, and DevOps Change Request Advanced Automation Approval flows based on your requirements using a flow or a script.
-   **[Automate DevOps change request creation](../task/automate-devops-change-request.md)**  
Modify your pipeline to automatically create a DevOps change request.
-   **[Create a DevOps Change request and associate existing DevOps data — Workspace](../task/devops-wkspc-chg-create-manual.md)**  
Create a DevOps change request and associate existing DevOps data through the Workspace UI.
-   **[Create a DevOps change request and associate existing DevOps data — Classic](../task/create-devops-change-request-manual.md)**  
Create a DevOps change request and associate existing DevOps data through the Classic UI.
-   **[DevOps change request without mandating category as DevOps](../task/create-devops-change-any-category.md)**  
Enable categorizing DevOps change request from DevOps properties. Change requests that are created as part of pipeline execution steps can be created with a category other than DevOps.
-   **[Change request creation with DevOps data retrieval errors](change-request-creation-with-devops-data-retrieval-errors.md)**  
Create change requests even with errors in DevOps data retrieval.
-   **[Artifacts and packages](using-dev-ops-release-change.md)**  
Artifacts and packages enable DevOps Change Velocity to track development and testing activities across a wide range of deployment and release models. This feature ensures that pipeline activity stored in the DevOps data model can be retrieved and applied when artifacts are created and released at different times or in different pipelines.
-   **[DevOps Pipeline UI](dev-ops-pipeline-ui.md)**  
Use the Pipeline UI to visualize interactions and results across a pipeline execution. This graphical view shows pipeline step progression and other details for each pipeline.
-   **[Configuring DevOps change request details within the pipeline](dev-ops-config-change-details.md)**  
Configure how the closure information, change state, and change request fields are updated from within a pipeline in the change step of the pipeline.
-   **[DevOps change models](devops-change-multimodel.md)**  
DevOps Change Velocity enables you to use fit-for-purpose change models that allow better flexibility in defining change models or processes to reflect modern development practices.
-   **[Retrieve change request data using DevOpsChangeRelationshipHelper script](../task/retrieve-change-request-data-using-devopschangerelationshiphelper-script.md)**  
Retrieve data associated with a change request based on the specified relation type using the DevOpsChangeRelationshipHelper script include.
-   **[Manage Pull Requests \(PR\) or Merge Requests in DevOps Change Velocity](../task/manage-pull-request-pipelines.md)**  
Manage Jenkins, GitHub Actions, and Azure DevOps \(ADO\) pipeline’s pull requests for GitHub, Bitbucket, and ADO coding sources from ServiceNow DevOps. You can enable the change approval process on your pull request to control pull request merge approvals from ServiceNow DevOps and monitor pull request details associated with the change request.
-   **[DevOps change request attributes](apis-for-change-actions-in-devops.md)**  
Add or update DevOps change request attributes using the changeInfo REST API, the Default Change Handler subflow, by passing attributes through the pipeline, Update function, or automated flows.
-   **[Import based evidence collection](import-based-evidence-collection-for-orchestration-capability.md)**  
Reduce instance overhead by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), Jenkins and GitLab orchestration tools.

**Parent Topic:**[DevOps Change Velocity](devops-landing-page-new.md)


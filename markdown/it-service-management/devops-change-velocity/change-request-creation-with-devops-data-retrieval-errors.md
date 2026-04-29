---
title: Change request creation with DevOps data retrieval errors
description: Create change requests even with errors in DevOps data retrieval.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Change request creation with DevOps data retrieval errors

Create change requests even with errors in DevOps data retrieval.

## Change request creation overview

**Note:** Change request creation with DevOps data retrieval errors is supported only for Azure DevOps, GitHub Actions, GitLab, Jenkins, and Harness pipelines.

You can create a change request with or without errors in DevOps data retrieval. This functionality can be controlled by the **Enable change request creation even with errors in DevOps data retrieval** property. When the **Enable change request creation even with errors in DevOps data retrieval** property is enabled, and an error occurs in retrieving DevOps data like work items, commits, test summaries, or security summaries, the corresponding change request is still created. The data that can be retrieved will still be associated with the change request. For the data that can’t be retrieved, the reason for the error will be notified to the user in the third-party console, and the same information will also be added in the **Change Comments** field in the Step Execution record and the change **Worknotes**.

If the **Enable change request creation even with errors in DevOps data retrieval** property isn’t enabled, a change request is created only when there’s no error in any step of a pipeline run. When an error occurs, the pipeline is aborted and the reason for the error is added in the inbound event's **Processing details** field, and the same is notified to the user in the third-party console.

For more information, see [DevOps Change Velocity properties](dev-ops-administration.md).

## Approval for change requests with DevOps data retrieval errors

For change requests created with DevOps data retrieval errors, the **is\_change\_with\_partial\_data** policy input is set to **True** for all the change approval policies. Only a manual change approval decision is applied to such changes so that you can approve or reject the change after manually verifying the DevOps data in it. In the DevOps Gather Change Policy Data subflow, the **Is change with partial data** action determines whether a change is created with DevOps data retrieval errors or not.

## Pipeline UI for change requests with DevOps data retrieval errors

When a change request gets created with DevOps data retrieval errors, the card specifying the stage where the error occurred will be displayed in the Yellow color. ![Pipeline UI displaying error stage card in yellow for change with errors](../image/pipeline-ui-change-partial.png)

**Note:** If your build pipeline \(CI\) is set up to trigger a release \(CD\) pipeline and a change is created in the release pipeline, the data is collected from the build pipeline and associated with the change request. There may be a situation where ServiceNow DevOps Change Velocity will receive and process the release pipeline events before build pipeline events. In this case, the change will be created with DevOps data from the build pipeline even though there’s an error in retrieving some of the data. You can observe this behavior even though the **Enable change request creation even with errors in the DevOps data retrieval** property is enabled. Also, the **is\_change\_with\_partial\_data** policy input will be false in this case, and the approval process will be applied in the way it’s defined in the approval flows unlike always manual in case of change requests with DevOps data retrieval errors.

## Callback timeout

If an inbound event goes into the waiting state during a pipeline run, the system tries to process the change until the timeout value in the **sn\_devops.change \_request\_callback\_timeout** property is exceeded, after that the pipeline is aborted. The reason for the error is displayed in your third-party tool's console logs. When a pipeline is canceled because of callback timeout, the same information is added in the callback record of the corresponding step execution. You can contact your DevOps admin to increase the timeout value in the **sn\_devops.change\_request\_callback\_timeout** property. The default value of this property is 120 minutes, and the minimum value is 60 minutes. For more information, see [DevOps Change Velocity properties](dev-ops-administration.md).

**Note:** If you are using GitHub change automation custom action, GitLab Docker change automation custom action, or Harness Docker change automation custom action in your corresponding pipeline to create change requests, you need to provide the **interval** in the custom action, which enables GitHub, GitLab, or Harness to poll ServiceNow DevOps for the change status. When the change reaches an appropriate state in ServiceNow within the specified interval, the appropriate status depending on the outcome of the change will be sent to GitHub, GitLab, or Harness pipeline, which will resume or abort the pipeline. See [ServiceNow DevOps custom actions from GitHub marketplace](servicenow-devops-custom-actions-from-github-marketplace.md#) and [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md) for more details. So, when your pipeline with the change custom action is run, and if any of the step notification from GitHub, GitLab, or Harness did not reach ServiceNow DevOps, then the association of callback, step execution, and task execution will not happen in ServiceNow DevOps. As the association is not available, the change will not be created and ServiceNow DevOps will wait until the association is in place. At the same time, GitHub, GitLab, or Harness will poll ServiceNow for the change status until the time specified in the interval is reached. If the interval is passed and also the timeout specified in the**sn\_devops.change\_request\_callback\_timeout** property is reached, ServiceNow DevOps will not terminate your pipeline as it should but will leave it for the default timeout set in the GitHub, GitLab, or Harness step that will eventually terminate the pipeline. The important information in this scenario is that ServiceNow DevOps will not be able to notify the user that the step events did not reach ServiceNow DevOps in the GitHub, GitLab, or Harness console logs.

## Upgrade

After you upgrade, the property will be set to false by default. Your current change process will function as is, but the only difference you’ll see is that, when an error occurs in retrieving DevOps data the pipeline is aborted \(instead of waiting indefinitely\) and the reason for the error is added in the inbound event **Processing details** field, and the same is notified to the user in the third-party console. If you want to create change requests with errors in retrieving DevOps data and also not fail your pipeline, you can enable the **Enable change request creation even with errors in DevOps data retrieval** property. This provides value to your change approvers and AppDev teams by getting the changes created automatically with DevOps evidence that is gathered and appropriately notified in the change request work notes and third-party console logs with errors or data that may be missing.

## Limitation

If the **Enable change request creation even with errors in DevOps data retrieval** property is enabled, and the ADO artifact package step in your pipeline results in error, the change will be created without ADO artifacts associated with it, but the corresponding error will not be notified in Worknotes, or Step Execution change comments, or in the ADO console log.

**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)


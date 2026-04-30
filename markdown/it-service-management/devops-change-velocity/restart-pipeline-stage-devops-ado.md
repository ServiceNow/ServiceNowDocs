---
title: Restarting failed build or release pipeline jobs and stages
description: Rerun or redeploy Azure DevOps build, release changes, or pipelines that are failed or canceled in that stage or pipeline. The reattempts display on the DevOps pipeline UI as continuous runs instead of creating new executions.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Restarting failed build or release pipeline jobs and stages

Rerun or redeploy Azure DevOps build, release changes, or pipelines that are failed or canceled in that stage or pipeline. The reattempts display on the DevOps pipeline UI as continuous runs instead of creating new executions.

## Rerun Azure DevOps pipelines or stages

You can rerun a failed or canceled build or release pipelines or change jobs in Azure DevOps. The reruns are processed as part of the same pipeline execution as the first run in ServiceNow DevOps. You can rerun entire pipelines or specific failed or canceled jobs and stages. You can now choose to reuse a change request instead of creating a new change request each time you restart a stage or a pipeline.

An **attemptNumber** parameter is added to the payload which helps us track reruns. Associated test summary, software quality scan results, commits, work items corresponding to every rerun attempt is also updated in ServiceNow DevOps.

If you are using the [Configuring change control using the Azure Invoke REST API](dev-ops-azure-change-control-api.md) you must add the attempt number parameter to your payload body in the specified syntax format for build and release pipelines. If you do not specify the attempt number parameter, the default attempt number is set to 1.

Example attempt number parameter in build pipeline payload:

```
"attemptNumber": "$(system.jobAttempt)"​
```

Example attempt number parameter in the release pipeline payload:

```
"attemptNumber": "$(Release.AttemptNumber)"
```

**Note:** Do not use the existing started and completed notifications for the stage jobs. If your jobs consider the started and completed notifications the rerun functionality does not work.

## Reusing Change Requests

If a change enabled job is rerun, and a change request exists for the previous run/attempt, you can choose to reuse the previous change request or create a new change request, using the base system ‘DevOps Change Request Reusability Decision Subflow’. The default implementation of this subflow, allows you to reuse a change request from the previous attempt if the change request is in implement, or post-implement states. If the Change request is in any other state, by default, a new change request is created when you rerun the job. Per existing behavior, all associated details such as test summaries, and scans, are newly generated while commits and work items are retained unchanged for new change requests.

For example, when a pipeline fails at a specific stage after the change request is approved, and you rerun that stage. The change request is reused, the associated test summary and software quality scans, and the commits and work items associated to the artifact are associated with the same change request which you approved.

To apply a custom logic for reusability, you can copy the existing subflow, make the changes, publish it, and update the new subflow name under **DevOps Properties** &gt; **DevOps Change Request Reusability Decision Subflow**.

In the regular base system flow when a change is created, ‘ [Customizing DevOps flows](using-dev-ops-model-change-flow.md)’ is used to update the  **State**  field of step execution record after a decision is taken on the change request. However, when you reuse a change, the first trigger condition of a change request being created is not met. A base system subflow ‘DevOps Change Request Reusability Model Subflow’ is triggered instead, whenever a change request is reused when a job is a rerun. The default implementation of this subflow is similar to the DevOps Model Change Request flow. You can create a custom subflow and update the subflow name at **DevOps Properties** &gt; **DevOps Change Request Reusability Model Subflow**.

## Pipeline UI changes

ServiceNow DevOps synchronizes all the changes that are caused when you restart or rerun a stage or a job, and displays them in the DevOps pipeline UI.

-   Click a card to view the latest attempt of that stage.
-   Click the **View all attempts** link to see all the step executions and related information associated to the step or stage that is run more than once.
-   The View change link displays the change request associated with the latest attempt.

In previous releases, failed jobs were either ignored or a new pipeline execution job was created for reruns and processed accordingly. For more information, see [DevOps Pipeline UI](dev-ops-pipeline-ui.md).

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](azure-devops-integration-dev-ops.md)


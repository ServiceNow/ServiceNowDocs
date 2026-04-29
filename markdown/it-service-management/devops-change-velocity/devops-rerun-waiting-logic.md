---
title: Execution sequence and waiting logic for rerun jobs
description: Processing sequence and waiting logic for rerun jobs are different when you reuse or create a change request as part of a rerun job.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Restarting failed build or release pipeline jobs and stages, Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Execution sequence and waiting logic for rerun jobs

Processing sequence and waiting logic for rerun jobs are different when you reuse or create a change request as part of a rerun job.

## Existing Considerations

-   A change request should not exist in a stage which contains parallel jobs.
-   If more than one stage is running in parallel, change request should not be the first job in both the stages.

**Note:** Parallel stages in release pipelines are processed and displayed in the pipeline UI as they occur in the Azure DevOps pipeline. Parallel stages in build pipelines are still processed in parallel but appear in a serial order in the pipeline UI.

## Upgrade Considerations

There is no change in the functionality or execution when you run the first pipeline attempt. All stages are processed sequentially and associated tests, software quality scans and change requests are executed and created as modeled.

**Note:**

-   Run a new pipeline after you upgrade if you have rerun stages and pipelines before upgrading. Rerun attempts and failed events prior to the upgrade are ignored by ServiceNow DevOps for reattempts.
-   If you have only run the pipeline once before upgrade, you can rerun the stage or the pipeline. The rerun functionality applies as designed and is saved in ServiceNow DevOps.

## Execution Sequence and processing logic

-   If the same artifact version registration call is received in reattempt, the registration call is ignored.
-   Package registration calls with same package name are not ignored. A new package associated to artifact versions and pipeline execution is created during reattempt. The artifacts that are associated to the latest package, will be shown on the change request.

From the Azure DevOps GUI, if you rerun a stage in a build pipeline the subsequent stages reruns are also triggered in it's specified sequence. If you reattempt processing a pipeline before all the stages of the previous attempt are not complete. The subsequent attempt waits until all the events in the previous attempt are processed.

For release pipelines, the stages are run in the specified sequence only during the first run. For subsequent rerun attempts manually run each stage. In release pipelines even if stages are running in parallel in Azure DevOps, from the second attempt onwards the events are processed in the specified sequence.

-   When a new change request is created for a reattempt stage job, and the stage that you are reattempting includes a test and a software quality scan only the latest Test Summary and Software Quality scan results display on the change request related list.
-   When a change request is reused for a rerun stage job, the Test Summary and Software Quality scan results for each attempt displays in the change request related list.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)


---
title: Parallel stages in Azure DevOps release pipelines
description: Parallel stages in a release pipeline are now processed concurrently and displayed in the DevOps pipeline UI in real time. Base system pre-deployment conditions and release gates enable you to create change requests that include details from parallel stages.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Parallel stages in Azure DevOps release pipelines

Parallel stages in a release pipeline are now processed concurrently and displayed in the DevOps pipeline UI in real time. Base system pre-deployment conditions and release gates enable you to create change requests that include details from parallel stages.

## Base system parallel stage support for Azure DevOps

Organizations use parallel stages to automate and speed up release processes for tasks that can be performed in parallel. For example, a release pipeline has integrated multiple test and software quality tools and has jobs configured to run in parallel. Not running each job sequentially significantly speeds up the release pipeline execution.

ServiceNow DevOps supports processing parallel stages in release pipelines and displays the stages in a parallel view in the DevOps pipeline UI. Effectively, the DevOps pipeline UI replicates the Azure DevOps GUI in real time.

You can also see the details of the processed stages in the pipeline UI.

**Important:** Support for parallel stages is restricted to Release pipelines. Build pipelines continue to appear in a sequential or serial manner in the DevOps pipeline UI, even if parallel stages are configured for build pipelines in Azure DevOps.

![ADO pipeline with parallel stages](../image/ado-parallel-stage-pipeline-ui.png "ADO pipeline with parallel stages")

Sample ADO pipeline with parallel stages

```
pipeline {
    agent any

    stages {
        stage('Build') {
            steps { 
                echo 'Building...'
                // Your build steps here
            }
        }

        stage('Test') {
            parallel {
                stage('Unit Tests') {
                    steps {
                        echo 'Running unit tests...'
                        // Your unit test steps here
                    }
                }
                stage('Integration Tests') {
                    steps {
                        echo 'Running integration tests...'
                        // Your integration test steps here
                    }
                }
                stage('Additional Tests') {
                    steps {
                        script {
                            parallel(
                                'Nested Stage 1': {
                                    echo 'Running nested parallel stage 1...'
                                    // Your nested parallel stage 1 steps here
                                },
                                'Nested Stage 2': {
                                    echo 'Running nested parallel stage 2...'
                                    // Your nested parallel stage 2 steps here
                                }
                            )
                        }
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                snDevOpsChange changeRequestDetails: '{ "attributes": {"chg_model": "e55d0bfec343101035ae3f52c1d3ae49","standard_change_template"="563504cc47410200e90d87e8dee490e2"},"autoCloseChange": false}',changeStepTimeOut: 18000, pollingInterval: 60
                // Your deploy steps here
            }
        }
    }
}

```

## ServiceNow® DevOps release gate in pre-deployment conditions to create Change requests

A base-system ServiceNow DevOps Release Gate is added along with pre-deployment conditions. Enable base system deployment gates that are configured to call the ServiceNow AI Platform instance, to create a change request before the deploy to production stage. Change requests are now created after all previous \(upstream\) stages complete processing. The change request captures relevant details from all upstream stages and displays them in the following corresponding related lists.

-   Commits
-   Work Items
-   Test Summaries
-   Software Quality Summary
-   Artifact Versions

After the pipeline execution completes processing the parallel stages preceding the production deployment stage, a change request is automatically created and mapped to the deploy to production stage in the Pipeline Executions view. The production stage completes processing once the change request is approved.

From the **Pipeline Execution** view of the relevant pipeline, click the **Pipeline UI** related link to view the real-time state of the pipeline as it appears in Azure DevOps. The associated artifact details which are sourced from the build pipeline, Test Results, Software Quality Summary Results display on the pipeline UI.

## Change creation sequence for parallel jobs

Job information from Azure is received in ServiceNow during the following times:

1.  Upon the completion of a stage.
2.  When the register-change step executes.

Azure provides job information sequentially based on job queue time, despite jobs potentially running in parallel. Consequently, if the register-change step executes while a parallel job queued earlier remains unfinished, the system assumes the parallel job is an upstream task, causing the change creation process to wait for its completion. However, stage completion notifications are not received until all jobs, including the register-change job, have finished.

This creates a deadlock scenario where the change process in ServiceNow waits for the parallel job to complete, while the parallel job waits for the stage completion notification, which in turn waits for the register-change job to finish.

Due to this deadlock, by the time the change is created, the Azure pipeline job has already failed, leading to the 500 error in the event API. Rerunning the job resolves the issue as the previously queued parallel jobs are marked as completed.

## Upgrade Considerations

Ensure that you review the following considerations before upgrading.

**Important:** A change request should not exist in a stage which contains parallel jobs.

-   The **Upstream execution** column in the Task Executions table is not displayed for fresh installations. Any customizations that you have made using the **Upstream execution** column prior to the upgrade are unaffected.
-   If stages are running in parallel, a change request should not be the first job in any stage.
-   After upgrading, new release pipeline executions process parallel stages concurrently and display parallel stages and associated details in the pipeline UI. Azure DevOps release pipelines that are already executed and stored in ServiceNow DevOps prior to the upgrade remain unaffected and continue to display parallel stages \(that are already executed and persisted\) in ServiceNow DevOps serially.
-   If the pre-deployment ServiceNow DevOps release gate is enabled in more than one start stage in a release pipeline with multiple start stages, it might result in multiple pipeline executions.

**Note:** A package is created for each start stage but any one package is associated per pipeline execution.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](azure-devops-integration-dev-ops.md)


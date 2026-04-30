---
title: Nested and parallel stages in Jenkins pipelines
description: Use nested and parallel stages in scripted Jenkins pipelines to speed up your pipeline execution. Change requests are created for nested and parallel stages and not just for the parent stage.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Nested and parallel stages in Jenkins pipelines

Use nested and parallel stages in scripted Jenkins pipelines to speed up your pipeline execution. Change requests are created for nested and parallel stages and not just for the parent stage.

## Support for nested and parallel stages in Jenkins pipelines

You can use nested and parallel stages in scripted Jenkins pipelines to automate and speed up tasks that can be run in parallel. For example, you have a scripted Jenkins pipeline with nested and parallel stages for various test cases such as different quality checks for different operating systems and browsers.

ServiceNow DevOps supports processing parallel and nested stages in Jenkins pipelines and displays the pipeline, in the DevOps pipeline UI. In effect, the ServiceNow DevOps pipeline UI renders or replicates the Jenkins pipeline UI in real time. From the **Pipeline Execution** view of the relevant pipeline, click the **Pipeline UI** related link to view the real-time state of the pipeline as it appears in Jenkins. The associated artifact details that are sourced from the build pipeline, Test Results, Software Quality Summary Results, and Change request details display on the pipeline UI.

**Important:** Support for parallel and nested stages is restricted to scripted pipelines in Jenkins. Freestyle pipelines continue to appear in a sequential or serial manner in the DevOps pipeline UI, even if parallel and nested stages are part of freestyle pipelines in Jenkins.

![Jenkins pipeline with nested or parallel stages](../image/jenkins-nested-pipeline.png "Jenkins pipeline with nested or parallel stages")

Sample pipeline with nested or parallel stages

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

## Change requests in nested and parallel stages

Change requests are created for all nested and parallel stages, once all upstream events \(prior to the change request\) are received. In previous releases, nested or parallel stages in Jenkins pipelines were not identified nor processed in ServiceNow DevOps. Only parent stages were identified and processed in a linear or sequential manner. If change requests existed as part of any nested and parallel stages, those change requests were ignored and a single change request was processed as part of the parent stage. When you run a new pipeline after upgrading, new steps and steps executions are created for nested stages.

Nested and parallel stages were not processed previously, and approval groups were mapped only to the parent stage. Because nested and parallel stages are identified during processing, you must verify that relevant approval groups are mapped to the appropriate nested or parallel stage. If subsequent steps of the pipeline are dependent on the change request's being approved, the pipeline execution is paused, and resumed when the change request is approved.

## Upgrade Considerations

If you are already using Jenkins with nested and parallel pipelines as your orchestration tool, consider the following while upgrading.

-   Upgrade during off-peak hours.
-   Ensure that you do not have any pipeline executions that are currently in progress by ServiceNow DevOps. If pipeline executions are being processed, step executions might not be created as expected for the in-progress pipeline runs. Rerun the pipeline to create appropriate step executions.


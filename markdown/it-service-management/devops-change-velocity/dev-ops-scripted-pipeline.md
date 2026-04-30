---
title: Using a declarative or scripted pipeline in DevOps
description: When you use a Jenkinsfile, steps are created, mapped, and associated to orchestration tasks automatically instead of manually.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Using a declarative or scripted pipeline in DevOps

When you use a Jenkinsfile, steps are created, mapped, and associated to orchestration tasks automatically instead of manually.

Jenkinsfile is a text file that contains the definition of a Jenkins pipeline and is checked into source control.

Each root-level stage configured in the Jenkinsfile is discovered as a separate orchestration task in DevOps that is mapped to an individual step.

**Note:** The **Track** field for the pipeline must be set to **True** in DevOps to receive job notifications from Jenkins. All active Jenkins configurations will receive job notifications when this field is set to **True**.

## DevOps Jenkinsfile commands

-   `snDevOpsChange(ignoreErrors:{true/false},changeRequestDetails:{setCloseCode:{true/false},attributes:})`

    Where `ignoreErrors` specifies the setting to prevent job failure if there is an error \(true/false\)

    Where `changeRequestDetails` specifies [closure code and change request fields](dev-ops-config-change-details.md) from within the pipeline

    Enables change control for each root-level stage that is mapped to a DevOps step.

-   `snDevOpsArtifact`

    Registers artifacts when configuring [Artifacts and packages](using-dev-ops-release-change.md).

-   `snDevOpsPackage`

    Creates a package for artifacts when configuring [Artifacts and packages](using-dev-ops-release-change.md).

-   `snDevOpsGetChangeNumber`

    Retrieves the change request number in a Jenkins pipeline based on specific change details.

-   `snDevOpsUpdateChangeInfo`

    Updates the change request details associated with a Jenkins pipeline.

-   `snDevOpsSecurityResult`

    Configures security scans on any stage of the pipeline and the scan details are retrieved from the corresponding stage to DevOps Change Velocity.


You can specify the Jenkins server configuration in any of these steps by passing the `configurationName` attribute in your pipeline. If the configuration name is not specified in any step, the default configuration will be used in that step. Passing an incorrect configuration name will result in the step to fail unless the **Ignore ServiceNow DevOps errors** option is selected while configuring the Jenkins plugin.

**Note:** Stage mapping is only supported for stages at the root level, not nested or parallel stages.

## Jenkins snippet generator for DevOps

You can use the Jenkins Snippet Generator utility to generate a template code for the orchestration tasks for scripted pipelines. You can use the snippet generator utility to create template for the following orchestration tasks.

-   SnDevOpsArtifact
-   SnDevOpsChange
-   SnDevOpsPackage
-   snDevOpsGetChangeNumber
-   snDevOpsUpdateChangeInfo
-   snDevOpsSecurityResult

To generate a step snippet, navigate to the Pipeline Syntax from a configured pipeline, select the step from the **Sample Step** list, and update the values for different variables in the step. Select the **ignore error** option to prevent job failure if there is an error. Select **Generate Pipeline Script** to create a snippet. You can copy and paste the snippet into a pipeline.

Example of a pipeline script for the SnDevOpsChange task:

```
snDevOpsChange changeCreationTimeOut: 3600, changeRequestDetails: '{ "attributes": { "short_description": "Test description", "priority": "1", "start_date": "2021-02-05 08:00:00", "end_date": "2022-04-05 08:00:00", "justification": "test justification", "description": "test description", "cab_required": true, "comments": "This update for work notes is from jenkins file", "work_notes": "test work notes", "assignment_group": "a715cd759f2002002920bde8132e7018" }, "setCloseCode": false, "autoCloseChange": true }', changeStepTimeOut: 18000, configurationName: 'Jenkins1', pollingInterval: 60
```

## Parallel and sub-stage support

When a stage \(or set of parallel stages\) is nested within a pipeline stage, these rules apply:

-   Any action from the nested stage is processed as part of the parent root-level stage
-   Only one change request is created \(at the parent root level\) even if multiple stages nested under the parent root-level stage trigger a change
-   Orchestration tasks created are always associated with the parent root-level stage \(not the nested stage\)

## Sub stage

In this sub-stage example, if a change request gets created from the sub stage \(deploy PROD\), the details of the parent root-level stage \(deploy\) are used in the change request, and orchestration tasks are also associated with the parent root-level stage \(deploy\).

```

stage("deploy") {
         stages{
             stage('deploy UAT') {
                when{
                   branch 'dev'
                }
            stage('deploy PROD') {
               when {
                  branch 'master'
               }
                steps{
                  
                  snDevOpsChange()              
                }
            }
        }
```

## Parallel stage

In this parallel stage example, if a change request is created from a sub stage \(UAT test-1 and/or UAT static code test\), only the first change request is created \(using the details of the parent root-level stage, UAT test\) regardless of whether both sub stages \(UAT test-1 and UAT static code test\) get triggered.

There is no indication of which parallel stage generated the change, and orchestration tasks are associated with the parent root-level stage \(UAT test\).

```

stage('UAT test') {
      parallel {
          stage('UAT test-1') {
              steps {
                  snDevOpsChange()
                  // 'UAT test-1' tasks
              }
                post {
                  success {
                    // post success tasks. E.g.: junit '**/target/surefire-reports/*.xml'
                  }
              }
          }
          stage('UAT static code test') {
              steps {
                  snDevOpsChange()
                  // 'UAT static code test' tasks
              }
          }
      }
 }

```


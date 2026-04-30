---
title: Additional information - Jenkins
description: Additional information on Jenkins.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Additional information - Jenkins

Additional information on Jenkins.

-   **[Connect to Jenkins using API token authentication](../task/authenticate-jenkins-using-api-token.md)**  
Connect to Jenkins using API token authentication instead of user name and password.
-   **[Reduce calls from Jenkins to ServiceNow DevOps to fetch pipeline information](reduce-pipeline-info-calls-jenkins.md)**  
Enable the Force Tracking Check field in the Jenkins configuration form to create a pipeline tracking file in Jenkins. ServiceNow DevOps makes a REST call to Jenkins to update the tracking file when the Track field in a pipeline is modified.
-   **[Using a declarative or scripted pipeline in DevOps](dev-ops-scripted-pipeline.md)**  
When you use a Jenkinsfile, steps are created, mapped, and associated to orchestration tasks automatically instead of manually.
-   **[Configure SonarQube scans on Jenkins pipelines](../task/config-sonarqube-jenkins-devops.md)**  
Configure SonarQube scans on Jenkins pipelines.
-   **[Notify change request rejection or cancellation reason to Jenkins pipeline](../task/update-jenkins-change-reject-reason.md)**  
Send change request rejection or cancellation reason along with approver name and the change request number to Jenkins pipeline logs.
-   **[Notify ServiceNow DevOps change request number to Jenkins pipelines](devops-change-number-notify-jenkins.md)**  
Send change request numbers to the Jenkins pipeline steps or logs when a change request is created in ServiceNow DevOps.
-   **[Get change request number in Jenkins pipeline](../task/get-change-request-number-in-jenkins-pipeline.md)**  
Retrieve the change request number in a Jenkins pipeline based on specific change details by running the snDevOpsGetChangeNumber script.
-   **[Update change request details in Jenkins pipeline](../task/update-change-request-details-in-jenkins-pipeline.md)**  
Update the change request details associated with a Jenkins pipeline by running the snDevOpsUpdateChangeInfo script in the pipeline.
-   **[Nested and parallel stages in Jenkins pipelines](nested-parallel-stage-support-jenkins.md)**  
Use nested and parallel stages in scripted Jenkins pipelines to speed up your pipeline execution. Change requests are created for nested and parallel stages and not just for the parent stage.
-   **[Jenkins log levels and Log Recorders](../reference/devops-jenkins-log-recorders.md)**  
Set log levels in the Jenkins plugin for ServiceNow DevOps based on the extent of log detail you need for debugging.

**Parent Topic:**[Jenkins integration with DevOps Change Velocity](jenkins-integration-dev-ops.md)


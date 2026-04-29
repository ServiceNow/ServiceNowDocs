---
title: Configure SonarQube scans on Jenkins pipelines
description: Configure SonarQube scans on Jenkins pipelines.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure SonarQube scans on Jenkins pipelines

Configure SonarQube scans on Jenkins pipelines.

## Before you begin

Ensure that you meet the following pre-requisites before configuring your Jenkins pipelines for SonarQube scans

-   SonarCloud or SonarQube version 8.6.1 community edition
-   SonarQube Scanner for Jenkins 2.4 or higher is installed on your Jenkins instance/environment.
-   ServiceNow DevOps plugin version 1.27 or later for Jenkins.
-   Ensure that SonarQube scans are configured and exist on your Jenkins pipelines using the SonarQube Scanner plugin for Jenkins. For more information, see
    -   [SonarQube Scanner for Jenkins](https://www.jenkins.io/doc/pipeline/steps/sonar/)
    -   [SonarScanner for Jenkins](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-jenkins/)
-   A SonarQube tool is created and is connected to the SonarQube server. For more information, see [SonarQube integration with DevOps Change Velocity](../concept/sonarqube-devops-integration-devops.md).

Role required: sn\_devops.admin

## About this task

When you run a pipeline which has SonarQube scan executions, the details are fetched into ServiceNow DevOps from the Jenkins pipeline. Using the Jenkins plugin, we check if the scan execution is configured in the Jenkins pipeline and check for SonarQube scans on every orchestration stage, using the `withSonarQubeEnv` tag. If a SonarQube analysis has happened on any stage of the pipeline’s execution, as part of our end notification we add a model with the `scanID` and `url` details for every scan that occurs in a particular stage. These scan analytics or details are correlated and displayed in the Software Quality Summary related list from Change requests and Task executions.

## Procedure

1.  In Jenkins, navigate to **Manage Jenkins** &gt; **Configure System**, select the **Enable injection of SonarQube server configuration as build environment variables** check box in the **SonarQube Servers** section, and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name for the configuration/project.|
    |Server URL|URL or IP address of the SonarQube server.|
    |Server authentication|Select the relevant authentication token type for the configuration.|

    **Note:** Use these same SonarQube server details or values while creating the SonarQube tools in ServiceNow DevOps as well as in the Jenkins pipeline.

2.  Click **Test Connection**.

    Verify that the connection successful message is shown.

3.  Click **Apply** and **Save**.

4.  Run the pipeline.


## Result

Based on the scan results on various stages of pipeline's execution, the results are shown in the corresponding step of the pipeline. Inbound events are created for notifications and subflows are triggered based on the notification type and capability.

## What to do next

**Note:**

Navigate to the pipeline UI to view the scan details under the **Quality** &gt; **Software Quality Results**.

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



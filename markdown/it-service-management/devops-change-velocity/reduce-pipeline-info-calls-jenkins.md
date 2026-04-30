---
title: Reduce calls from Jenkins to ServiceNow DevOps to fetch pipeline information
description: Enable the Force Tracking Check field in the Jenkins configuration form to create a pipeline tracking file in Jenkins. ServiceNow DevOps makes a REST call to Jenkins to update the tracking file when the Track field in a pipeline is modified.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Reduce calls from Jenkins to ServiceNow DevOps to fetch pipeline information

Enable the Force Tracking Check field in the Jenkins configuration form to create a pipeline tracking file in Jenkins. ServiceNow DevOps makes a REST call to Jenkins to update the tracking file when the Track field in a pipeline is modified.

## Force Tracking Check

The ServiceNow DevOps configuration section in Jenkins includes a **Force Tracking Check** check box to reduce the number of calls made from Jenkins to DevOps to fetch pipeline information such as pipelines being tracked. Base-system flows:

-   DevOps Jenkins File Update- Track flow
-   DevOps Jenkins File Update- Test Info flow

## How it works

In previous versions, a REST call fetched the pipeline information for every Jenkins build triggered. If you had multiple pipelines in your Jenkins environment and were tracking only a few of them, this meant that a call was made to fetch the tracking information for each pipeline even if you were tracking a few of them.

The first time you trigger a Jenkins build or pipeline execution, Jenkins makes a pipeline information API call and creates *snPipelineInfo.json* file in `/{JENKINS_HOME}/jobs/{jobName}` directory. For each subsequent pipeline execution Jenkins checks the information available in the *snPipelineInfo.json* file before making a pipeline info API call.

If you disable the **Force Track Check** check box:

-   The DevOps Jenkins File Update- Track flow triggers when you update the **Track** field on the pipeline form. The **Track** field info is updated in the *snPipelineInfo.json* file.
-   DevOps Jenkins File Update- Test Info flow triggers when you update Test type mapping for Jenkins tool integration and verify that Test info is updated in *snPipelineInfo.json* file.

If you enable the **Force Track Check** check box, Jenkins makes pipeline info API calls to DevOps even if track/test information exists in the *snPipelineInfo.json* file.


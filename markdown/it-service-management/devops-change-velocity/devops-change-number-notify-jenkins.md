---
title: Notify ServiceNow DevOps change request number to Jenkins pipelines
description: Send change request numbers to the Jenkins pipeline steps or logs when a change request is created in ServiceNow DevOps.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Notify ServiceNow DevOps change request number to Jenkins pipelines

Send change request numbers to the Jenkins pipeline steps or logs when a change request is created in ServiceNow DevOps.

## Sending ServiceNow DevOps change request to Jenkins pipeline

Change requests that are created as part of Jenkins pipeline executions for both scripted and free-style pipelines are notified to the Jenkins pipeline console.

When you trigger a scripted Jenkins pipeline and a change request is created as part of the pipeline execution stage in ServiceNow DevOps, the change request number is notified to Jenkins. The change request number displays in the Jenkins pipeline job logs for scripted pipelines.

![Change request number in Jenkins logs for scripted pipelines](../image/change-number-scripted-jenkins.png)

Upon triggering a free-style Jenkins pipeline, the change request that is created as part of the ServiceNow DevOps pipeline execution stage waits for the approval action to be performed on the change. The change request number and details display against the relevant build in the Jenkins console's **Build History** section.

![Change request number in Jenkins Build History for free-style pipelines](../image/devops-change-freestyle-jenkins.png)

**Note:** After an approval or rejection action is performed on the change request in ServiceNow DevOps, the change request displays in the Jenkins pipeline build logs, similar to scripted pipelines.


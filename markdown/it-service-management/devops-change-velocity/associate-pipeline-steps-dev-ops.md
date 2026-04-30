---
title: Associate Azure pipeline steps in DevOps
description: For manually created DevOps steps, associate each orchestration task in the Orchestration Tasks related list with a DevOps pipeline step to track the activity of each stage in your Azure pipeline.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Associate Azure pipeline steps in DevOps

For manually created DevOps steps, associate each orchestration task in the Orchestration Tasks related list with a DevOps pipeline step to track the activity of each stage in your Azure pipeline.

## Before you begin

Role required: sn\_devops.admin

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Tools** &gt; **Orchestration Tools**, and open the Azure DevOps tool record.

2.  In the Orchestration Tasks related list, enter the corresponding DevOps pipeline step in the **Step** field of each orchestration task.

    **Note:** The **Track** field is set to **True** by default when you discover orchestration tasks and pipelines. Tracking is required to receive job notifications from Azure DevOps.

    Azure pipeline job run notifications are sent to the DevOps application. Each task execution notification corresponds to an orchestration task and, because orchestration tasks are mapped to a certain step in your DevOps pipeline, you can track the activity in each stage of your pipeline.


## Example

![AssociateSteps](../image/dev-ops-azure-associate-steps.png "DevOps associate steps")

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)


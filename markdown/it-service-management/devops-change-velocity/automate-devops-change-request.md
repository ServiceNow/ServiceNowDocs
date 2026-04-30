---
title: Automate DevOps change request creation
description: Modify your pipeline to automatically create a DevOps change request.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Automate DevOps change request creation

Modify your pipeline to automatically create a DevOps change request.

## About this task

The step 5 in this topic requires you to specify the attributes for the change request. Change attributes can be specified in multiple areas. They can be specified in the pipeline step of DevOps Change Velocity, in the Default Change Handler subflow, in an approval flow, in a template, or passed in the pipeline. If a change model is used, they can also be specified in model presets. For more information, see [DevOps change request attributes](../concept/apis-for-change-actions-in-devops.md).

If you have used business rules, then you must set the **sn\_devops.change\_request.apply\_attributes\_on\_creation** property to true, so that the change attributes passed in the pipeline are set when the change request is created instead of the attributes being passed after the change request is created. For more information, see [DevOps Change Velocity properties](../concept/dev-ops-administration.md).

## Before you begin

Role required: sn\_devops.admin, sn\_devops.tool\_owner, or sn\_devops.app\_owner

## Procedure

1.  From the DevOps Change Workspace, select **Automate change creation**.

2.  In the **Application** field, select the application that you want to associate with the pipeline for which you want to automate change request creation, and select **Next**.

    ![Select your application.](../image/change-01.png)

3.  Select the pipeline that has the step \(stage\) from where you want to trigger the automated creation of change requests.

    **Note:** If you don’t see the pipeline, make sure that it’s associated to the application selected in the previous step.

    ![Select a pipeline.](../image/change-02.png)

    You can see the connection state of the tool associated with the pipeline in the **Overall status** column. An alert will also be displayed based on the connection state of the tool before proceeding to the next step.

4.  Select the step in the pipeline from where you want to trigger the automated creation of a change request.

    **Note:** You can skip this activity if you want to manage and specify change attributes in the pipeline instead as specified in the **Enable change** step.

    ![Select a step.](../image/change-03.png)

5.  Specify the change attributes in the change fields and enable change receipt by selecting the Change receipt option.

    **Note:** You can skip the activity of specifying change attributes if you want to manage and specify these attributes in the pipeline instead. However, change receipt can be enabled only from ServiceNow DevOps Change Velocity.

    For more information on configuring change settings, see [Create a Change](../../change-management/task/t_CreateAChange.md).

    You must enable change receipt if you don’t want the pipeline to pause when the change request is created. You can disable the sn\_devops.enable\_change\_receipt\_state\_transition property if you don’t want the state to transition automatically.

    ![Specify change attributes.](../image/change-04.png)

6.  Modify your pipeline and use the corresponding code snippet to enable change control and specify change attributes.

    Depending on your orchestration tool, the steps to enable change control are displayed. Follow the instructions given on the page and modify your pipeline accordingly.

    The following image displays the steps for Azure DevOps.

    ![Change control script for Azure DevOps.](../image/change-05.png)

7.  Select **Done**.


**Parent Topic:**[Accelerating your DevOps change process](../concept/dev-ops-change-acceleration.md)


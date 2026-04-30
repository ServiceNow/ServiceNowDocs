---
title: Customizing DevOps flows
description: Customize or recreate the DevOps Change Request Manual Approval, DevOps Change Request Minimal Automation Approval, and DevOps Change Request Advanced Automation Approval flows based on your requirements using a flow or a script.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Customizing DevOps flows

Customize or recreate the DevOps Change Request Manual Approval, DevOps Change Request Minimal Automation Approval, and DevOps Change Request Advanced Automation Approval flows based on your requirements using a flow or a script.

You can clone the DevOps flows and then customize them according to your requirements. To clone a flow, navigate to the flow you want to clone from the Base system DevOps flows sections or from the Flow Designer landing page \(**All &gt; Process Automation &gt; Flow Designer**\). On the top-right corner of the Flow page, select **More Actions &gt; Copy flow**. In the Create a copy of this flow dialog box, enter the new name for the flow, and select DevOps Data Model as the application. Select the **Copy** button to create the new flow. The new flow will open in Flow Designer. Make any changes to customize it to your business requirements. You can run the flow to make sure it has no errors by selecting the **Test** button on the top-right corner of the screen before activating the flow. Activate the flow when it's ready by selecting the **Activate** button.

## Customize the DevOps Change Request Manual Approval flow

In the DevOps Change Request Manual Approval flow, the state of step execution is changed based on the change approval. However, you can customize or recreate this flow based on your requirements.

After the change request state is moved to approved, canceled, or rejected \(either manually or by using a change policy\), call the **Update state of step execution based on change approval** Workflow Studio action to update the **State** field of the step execution record.

You can use either a flow or a script to call the action.

-   **Calling the Workflow Studio action using a flow**

    Calling the **Update state of step execution based on change approval** Workflow Studio action is required to update the state of the step execution record according to the approval field in the change request record.

    This action serves as a trigger for the **Change Control Callback** flow, which is used to notify the change decision to the orchestration tool.

    ![DevOps Change Request Manual Approval flow](../image/devops-manual-flow.png)

-   **Calling the Workflow Studio action using a script**

    Method to call the Workflow Studio action from a script:

    ```
    sn_fd.FlowAPI.executeAction('sn_devops.update_state_of_step_execution_based_on_change_approval’, inputs);
    ```


## Customize the DevOps Change Request Minimal Automation Approval flow

In the DevOps Change Request Minimal Automation Approval flow, the change is approved and the state of the change moves from the new to the implementation state. After the change request state is moved to approved, call the **DevOps - Update Step Execution and Change Request States** Flow Designer action to update the **State** field of the step execution record.

You can use either a flow or a script to call the action.

-   **Calling the Workflow Studio action using a flow**

    Calling the **DevOps - Update Step Execution and Change Request States** Workflow Studio action is required to update the state of the step execution record.

    This action serves as a trigger for the **Change Control Callback** flow, which is used to notify the change decision to the orchestration tool.

    ![DevOps Change Request Minimal Automation Approval flow](../image/devops-minimal-flow.png)

-   **Calling the Workflow Studio action using a script**

    Method to call the Workflow Studio action from a script:

    ```
    sn_fd.FlowAPI.executeAction('sn_devops.devOps-_update_step_execution_and_change_request’, inputs);
    ```


## Customize the DevOps Change Request Advanced Automation Approval flow

In the DevOps Change Request Advanced Automation Approval flow, the change is approved and the state of the change moves from the new to the implementation state. After the change request state is moved to approved, call the **Update step execution record** action to update the **State** field of the step execution record.

You can use either a flow or a script to call the action.

-   **Calling the Workflow Studio action using a flow**

    Calling the **Update step execution record** Workflow Studio action is required to update the state of the step execution record according to the approval field in the change request record.

    This action serves as a trigger for the **Change Control Callback** flow, which is used to notify the change decision to the orchestration tool.

    ![DevOps Change Request Advanced Automation Approval flow](../image/devops-advanced-flow.png)

-   **Calling the Workflow Studio action using a script**

    Method to call the Workflow Studio action from a script:

    ```
    sn_fd.FlowAPI.executeAction('sn_devops.update_step_execution_record’, inputs);
    ```


**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)

**Related topics**  


[Accelerating your DevOps change process](dev-ops-change-acceleration.md)


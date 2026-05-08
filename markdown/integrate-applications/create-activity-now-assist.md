---
title: Create an activity with Now Assist
description: Create activities from text instructions and preview options by using the Now Assist for RPA Hub application. Activities provide modularity to an automation project in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Use, Now Assist for RPA Hub, Workflow Data Fabric]
---

# Create an activity with Now Assist

Create activities from text instructions and preview options by using the Now Assist for RPA Hub application. Activities provide modularity to an automation project in RPA Desktop Design Studio.

## Before you begin

Set up the RPA Desktop Design Studio application and add the ServiceNow instance details. For more information, see [Set up RPA Desktop Design Studio](set-up-rpa-studio.md).

To access the Now Assist for RPA Hub feature in RPA Desktop Design Studio, perform the following steps:

-   Install the Now Assist for RPA Hub application to add the generative AI capability. For more information, see [Configure Now Assist for RPA Hub](configure-now-assist-rpa-hub.md).
-   Turn on the RPA bot generation skill to use the generative AI capability. For more information, see [Turn on the RPA bot generation skill](turn-rpa-bot-generation-skill.md).
-   After activating the RPA bot generation skill, relaunch the RPA Desktop Design Studio application to apply the modified settings.

If you skip these steps, the Now Assist for RPA Hub feature doesn’t appear in RPA Desktop Design Studio.

Familiarize yourself with the RPA bot generation skill concepts. For more information, see [Robotic Process Automation \(RPA\) bot generation](../concept/rpa-bot-generation.md).

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## About this task

Activities are a reusable set of instructions that are designed for an automation on the Design surface of RPA Desktop Design Studio. Activities are used to segregate the entire automation into smaller chunks for easier comprehension of the automation logic.

You can design automation workflows in an activity on the Design surface by using various components.

Each activity contains two components by default: Start and End. These components can't be deleted because they’re the starting and ending points of the activity.

You can reuse each activity multiple times within the same automation project by dragging the activity to the Design surface. You can also import activities in different automation projects.

To create an activity manually, see [Create and use an activity in RPA Desktop Design Studio](configure-activity-rpa-studio.md).

## Procedure

1.  In the Project Explorer pane of RPA Desktop Design Studio, navigate to **Activities**.

    The Activities section lists all the activities that are created in each project. By default, a Main activity is created when a new project is initiated. The automation execution starts from the startup activity, in this case, Main activity, as shown in the following example.

    ![Main activity is displayed in the RPA Desktop Design Studio when a new project is initiated.](../image/example-activity-screen.png "Example: Activity in RPA Desktop Design Studio")

2.  In the Project Explorer pane, right-click **Activities** and select **New activity using Now Assist**.

    ![RPA Desktop Design Studio user interface that shows the New activity using the Now Assist option.](../image/create-activity-now-assist-rpa.png "Create an activity using Now Assist")

3.  In the New activity window, enter the Now Assist instructions.

    The instruction text is used by the RPA bot generation skill to create your automation. Use short, direct, and clear sentences to describe the expected actions. Be specific and provide detailed descriptions of the automation logic. Avoid jargon and abbreviations.

    The following example shows that the Now Assist instructions are provided to build an automation to trigger a flow designer, retrieve the output, and insert it into an existing Microsoft Word document.

    ![New activity window that shows the instructions that are used by Now Assist to generate an automation workflow.](../image/new-activity-directions.png "Example: New activity window")

    **Note:**

    For more information on example instructions and general guidelines for writing Now Assist instructions, see [Robotic Process Automation \(RPA\) bot generation](../concept/rpa-bot-generation.md). For more information about the limitations of the RPA bot generation skill, see [Limitations of Robotic Process Automation \(RPA\) bot generation skill](../reference/limitations-rpa-bot-gen-skill.md).

4.  Select **Generate preview**.

5.  In the New Activity window, regenerate a preview, clear a workflow, cancel an automation, or add an activity.

    **Note:**

    You can't make any changes In the Activity preview screen because it's read-only. You can maximize it and use scroll options to view the entire generated automation workflow.

    If your instruction generates a workflow with components that aren’t compatible with the current project type, those components show up as unknown in the generated workflow. For example, if your workflow includes a GracefulStop component and if the current project is attended automation, the GracefulStop component appears as unknown because it’s not supported in the attended automations.

    ![New activity window displays the options to regenerate a preview, clear a workflow, cancel an automation, or add an activity.](../image/new-activity-options.png "Example: New activity options")

<table id="choicetable_tkm_2nn_4dc"><thead><tr><th align="left" id="d358905e358">

Option

</th><th align="left" id="d358905e361">

Procedure

</th></tr></thead><tbody><tr><td id="d358905e367">

**Regenerate preview**

</td><td>

If the generated automation preview doesn’t meet your needs, you can update the Now Assist instructions, and select **Regenerate preview**.Each time you build or rebuild an automation, the operation counts as an assist tracked by your Now Assist subscription. To track your Now Assist usage, see Monitoring Now Assist usage in Subscription Management.

</td></tr><tr><td id="d358905e394">

**Clear**

</td><td>

If you want to clear the workflow that was created by the Now Assist instructions, select **Clear** and then select **Yes** in the Confirm clear automation window.

</td></tr><tr><td id="d358905e412">

**Cancel**

</td><td>

If you want to stop creating an automation and return to the design surface, select **Cancel**. In the Confirm cancel window, select **Yes** to return to the previous screen.The added content isn’t saved.

</td></tr><tr><td id="d358905e429">

**Add activity**

</td><td>

If the automation preview looks good, select **Add activity**.**Important:** The automation is generated by Now Assist. Be sure to check it for accuracy and make any edits before running.

Close the displayed message for a clearer view.

![Generated automation workflow that is displayed on the design surface.](../image/activity-now-assist-last-screen.png "Example: Automation workflow on the design surface")

</td></tr></tbody>
</table>
## Result

The automation flow is added as a New Activity in Activities.

## What to do next

For more actions on the activity, see [Create and use an activity in RPA Desktop Design Studio](configure-activity-rpa-studio.md).


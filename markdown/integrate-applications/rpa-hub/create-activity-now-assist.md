---
title: Create an activity with AI
description: Create activities from text instructions and preview options by using AI. Activities provide modularity to an automation project in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/create-activity-now-assist.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create an activity with AI

Create activities from text instructions and preview options by using AI. Activities provide modularity to an automation project in RPA Desktop Design Studio.

## Before you begin

Set up the RPA Desktop Design Studio application and add the ServiceNow instance details. For more information, see [Set up RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/set-up-rpa-studio.md).

To access the AI features in RPA Desktop Design Studio, perform the following steps:

-   Install the ServiceNow Otto for RPA Hub application to add the generative AI capability. For more information, see [Install ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-now-assist-rpa-hub.md).
-   Turn on the RPA bot generation skill to use the generative AI capability. For more information, see [Turn on the RPA bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/turn-rpa-bot-generation-skill.md).
-   After activating the RPA bot generation skill, relaunch the RPA Desktop Design Studio application to apply the modified settings.

If you skip these steps, the ServiceNow Otto for RPA Hub feature doesn’t appear in RPA Desktop Design Studio.

Familiarize yourself with the RPA bot generation skill concepts. For more information, see [Robotic Process Automation \(RPA\) bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-bot-generation.md), [Limitations of ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/limitations-rpa-bot-gen-skill.md), and [Example instructions for ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/example-instructions-rpa.md).

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## About this task

Activities are a reusable set of instructions that are designed for an automation on the Design surface of RPA Desktop Design Studio. Activities are used to segregate the entire automation into smaller chunks for easier comprehension of the automation logic.

You can design automation workflows in an activity on the Design surface by using various components.

Each activity contains two components by default: Start and End. These components can't be deleted because they’re the starting and ending points of the activity.

You can reuse each activity multiple times within the same automation project by dragging the activity to the Design surface. You can also import activities in different automation projects.

To create an activity manually, see [Create an activity manually in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-activity-rpa-studio.md).

## Procedure

1.  In the Project Explorer pane of RPA Desktop Design Studio, navigate to **Activities**.

    The Activities section lists all the activities that are created in each project. By default, a Main activity is created when a new project is initiated. The automation execution starts from the startup activity, in this case, Main activity, as shown in the following example.

    \[Omitted image "example-activity-screen.png"\] Alt text: Main activity is displayed in the RPA Desktop Design Studio when a new project is initiated.

2.  In the Project Explorer pane, right-click **Activities** and select **New activity using AI**.

    \[Omitted image "create-activity-now-assist-rpa.png"\] Alt text: RPA Desktop Design Studio user interface that shows the New activity using the Now Assist option.

3.  In the New activity window, enter the AI instructions.

    The instruction text is used by the RPA bot generation skill to create your automation. Use short, direct, and clear sentences to describe the expected actions. Be specific and provide detailed descriptions of the automation logic. Avoid jargon and abbreviations.

    \[Omitted image "new-activity-directions.png"\] Alt text: New activity window that shows the instructions that are used by AI to generate an automation workflow.

    **Note:**

    For more information on example AI instructions and general guidelines, see [Robotic Process Automation \(RPA\) bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-bot-generation.md). For more information about the limitations of the RPA bot generation skill, see [Limitations of ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/limitations-rpa-bot-gen-skill.md).

4.  Select **Generate preview**.

5.  In the New Activity window, regenerate a preview, clear a workflow, cancel an automation, or add an activity.

    **Note:**

    You can't make any changes In the Activity preview screen because it's read-only. You can maximize it and use scroll options to view the entire generated automation workflow.

    If your instruction generates a workflow with components that aren’t compatible with the current project type, those components show up as unknown in the generated workflow. For example, if your workflow includes a GracefulStop component and if the current project is attended automation, the GracefulStop component appears as unknown because it’s not supported in the attended automations.

    \[Omitted image "new-activity-options.png"\] Alt text: New activity window displays the options to regenerate a preview, clear a workflow, cancel an automation, or add an activity.

<table id="choicetable_tkm_2nn_4dc"><thead><tr><th align="left" id="d599023e352">

Option

</th><th align="left" id="d599023e355">

Procedure

</th></tr></thead><tbody><tr><td id="d599023e361">

**Regenerate preview**

</td><td>

If the generated automation preview doesn’t meet your needs, you can update the AI instructions, and select **Regenerate preview**.Each time you build or rebuild an automation, the operation counts as an assist tracked by your AI subscription. To track your AI usage, see [Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md).

</td></tr><tr><td id="d599023e379">

**Clear**

</td><td>

If you want to clear the workflow that was created by the AI instructions, select **Clear** and then select **Yes** in the Confirm clear automation window.

</td></tr><tr><td id="d599023e394">

**Cancel**

</td><td>

If you want to stop creating an automation and return to the design surface, select **Cancel**. In the Confirm cancel window, select **Yes** to return to the previous screen.The added content isn’t saved.

</td></tr><tr><td id="d599023e411">

**Add activity**

</td><td>

If the automation preview looks good, select **Add activity**.**Important:** The automation is generated by AI. Be sure to check it for accuracy and make any edits before running.

Close the displayed message for a clearer view.

\[Omitted image "activity-now-assist-last-screen.png"\] Alt text: Generated automation workflow that is displayed on the design surface.

</td></tr></tbody>
</table>
## Result

The automation flow is added as a New Activity in Activities.

## What to do next

For more actions on the activity, see [Create an activity manually in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-activity-rpa-studio.md).

**Parent Topic:**[Building automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-studio-build.md)


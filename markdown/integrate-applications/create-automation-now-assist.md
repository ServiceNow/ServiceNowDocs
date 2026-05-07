---
title: Create an automation with Now Assist
description: Create an automation from text instructions and preview options by using the Now Assist for RPA Hub application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Use, Now Assist for RPA Hub, Workflow Data Fabric]
---

# Create an automation with Now Assist

Create an automation from text instructions and preview options by using the Now Assist for RPA Hub application.

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

To create an automation project manually, see [Create an automation project manually](create-automation-project.md).

## Procedure

1.  On the RPA Desktop Design Studio home page, select **Create Automation**.

2.  In the Build an automation window, select the **Build with Now Assist** option.

    ![Build an automation window that displays Build with Now Assist and Build manually options to start creating automations. The Build with Now Assist option is selected.](../image/start-build-now-assist-rpa.png "Build with Now Assist")

3.  Select **Next**.

4.  In the Build with Now Assist window, enter the Now Assist instructions.

    The instruction text is used by the RPA bot generation skill to create your automation. Use short, direct, and clear sentences to describe the expected actions. Be specific and provide detailed descriptions of the automation logic. Avoid jargon and abbreviations.

    The following example shows that the Now Assist instructions are provided so that you can build an automation to get PDF files from a location and then merge all PDF documents into a single PDF document.

    ![Build with Now Assist window that shows the instructions that are used by Now Assist to generate an automation workflow.](../image/build-now-assist-example.png "Build with Now Assist window")

    An example instruction is displayed for your reference.

    **Note:**

    For more information on example instructions and general guidelines for writing Now Assist instructions, see [Robotic Process Automation \(RPA\) bot generation](../concept/rpa-bot-generation.md). For more information about the limitations of the RPA bot generation skill, see [Limitations of Robotic Process Automation \(RPA\) bot generation skill](../reference/limitations-rpa-bot-gen-skill.md).

5.  Select **Generate preview**.

6.  In the Build with Now Assist window, regenerate a preview, clear the workflow, stop creating an automation, or select next if you like the automation preview.

    **Note:** You can’t make any changes In the Automation preview screen because it’s read-only. You can maximize it and use the scroll options to view the entire generated automation workflow.

    ![Build with Now Assist window displays options to regenerate a preview, clear the workflow, stop creating an automation, or select next if you like the automation preview.](../image/text-bot-preview-options.png "Build with Now Assist options")

<table id="choicetable_tkm_2nn_4dc"><thead><tr><th align="left" id="d208137e337">

Option

</th><th align="left" id="d208137e340">

Procedure

</th></tr></thead><tbody><tr><td id="d208137e346">

**Regenerate preview**

</td><td>

If the generated automation preview doesn’t meet your needs, you can update the Now Assist instructions, and select **Regenerate preview**.Each time you build or rebuild an automation, the operation counts as an assist tracked by your Now Assist subscription. To track your Now Assist usage, see [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d208137e373">

**Clear**

</td><td>

If you want to clear the workflow that was created by Now Assist and the instruction in Now Assist, select **Clear** and then select **Yes** in the Confirm clear automation window.

</td></tr><tr><td id="d208137e394">

**Cancel**

</td><td>

If you want to stop creating an automation and return to the RPA Desktop Design Studio home page, select **Cancel**. In the Confirm cancel window, select **Yes** to return to the previous screen.The generated automation workflows, if any, aren’t saved.

</td></tr><tr><td id="d208137e414">

**Next**

</td><td>

If the automation preview looks good, select **Next**.

</td></tr></tbody>
</table>7.  In the Create new automation window, fill in the fields.

    ![Create new automation window that displays a form so that you can fill in the automation information for the generated workflow.](../image/create-new-automation-now-assist.png "Create new automation window")

    **Note:**

    If your instruction generates a workflow with components that aren’t compatible with the selected automation type, those components show up as unknown in the generated workflow. For example, if your workflow includes a GracefulStop component and you select **Attended Automation**, the GracefulStop component appears as unknown because it’s not supported in the attended automations.

<table id="table_u1z_r4n_4dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select an automation type

</td><td>

Type of automation. Select either **Unattended Automation** or **Attended Automation**.An unattended automation doesn’t require human supervision and can be used for highly repetitive tasks. For example, an unattended robot can seamlessly perform copy and paste operations into a Microsoft Excel file, streamlining data entry in a Customer Relationship Management \(CRM\) system without any human input.

An attended automation requires human supervision. For example, in a contact center, robots are used as user assistants. They’re installed on an operator’s workstation and are triggered by human operators on demand.

</td></tr><tr><td>

Name

</td><td>

Name of the unattended or attended automation project.

</td></tr><tr><td>

Description

</td><td>

Description of the unattended or attended automation project.

</td></tr><tr><td>

Location

</td><td>

Location of the automation project or the default location.

</td></tr></tbody>
</table>8.  Select **Save and Edit**.

    **Important:** The automation is generated by Now Assist. Be sure to check it for accuracy and make any edits before running.

    Close the displayed message for a clearer view.

    ![Generated automation workflow that is displayed on the design surface.](../image/now-assist-automation-legal-notice.png "Automation workflow on the design surface")


## Result

The automation flow is launched on the design surface and it’s added as a Main activity in Activities.


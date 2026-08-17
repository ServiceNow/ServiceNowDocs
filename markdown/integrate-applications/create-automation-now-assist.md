---
title: Create an automation with AI
description: Create an automation from text instructions and preview options by using the ServiceNow Otto for RPA Hub application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-automation-now-assist.html
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create an automation with AI

Create an automation from text instructions and preview options by using the ServiceNow Otto for RPA Hub application.

## Before you begin

Set up the RPA Desktop Design Studio application and add the ServiceNow instance details. For more information, see [Set up RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-rpa-studio.md).

To access the AI features in RPA Desktop Design Studio, perform the following steps:

-   Install the ServiceNow Otto for RPA Hub application to add the generative AI capability. For more information, see [Install ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-now-assist-rpa-hub.md).
-   Turn on the RPA bot generation skill to use the generative AI capability. For more information, see [Turn on the RPA bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/turn-rpa-bot-generation-skill.md).
-   After activating the RPA bot generation skill, relaunch the RPA Desktop Design Studio application to apply the modified settings.

If you skip these steps, the ServiceNow Otto for RPA Hub feature doesn’t appear in RPA Desktop Design Studio.

Familiarize yourself with the RPA bot generation skill concepts. For more information, see [Robotic Process Automation \(RPA\) bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-bot-generation.md), [Limitations of ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/limitations-rpa-bot-gen-skill.md), and [Example instructions for ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/example-instructions-rpa.md).

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin

## About this task

To create an automation project manually, see [Create an automation project manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-automation-project.md).

## Procedure

1.  On the RPA Desktop Design Studio home page, select **Create Automation**.

2.  In the Build an automation window, select the **Build with AI** option.

    \[Omitted image "build-now-assist-screen-rpa.png"\] Alt text: RPA Desktop Design Studio user interface that shows the \(1\) Create automation option and \(2\) Build with AI option.

3.  Select **Next**.

4.  In the Build with AI window, enter instructions for AI.

    The instruction text is used by the RPA bot generation skill to create your automation. Use short, direct, and clear sentences to describe the expected actions. Be specific and provide detailed descriptions of the automation logic. Avoid jargon and abbreviations.

    The following example shows that the AI instructions are provided so that you can build an automation to get PDF files from a location and then merge all PDF documents into a single PDF document.

    \[Omitted image "build-now-assist-example.png"\] Alt text: Build with AI window that shows the instructions that are used by AI to generate an automation workflow.

    An example instruction is displayed for your reference.

    **Note:**

    For more information on example AI instructions and general guidelines, see [Robotic Process Automation \(RPA\) bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-bot-generation.md). For more information about the limitations of the RPA bot generation skill, see [Limitations of ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/limitations-rpa-bot-gen-skill.md).

5.  Select **Generate preview**.

6.  In the Build with AI window, regenerate a preview, clear the workflow, stop creating an automation, or select next if you like the automation preview.

    **Note:** You can’t make any changes In the Automation preview screen because it’s read-only. You can maximize it and use the scroll options to view the entire generated automation workflow.

    \[Omitted image "text-bot-preview-options.png"\] Alt text: Build with AI window displays options to regenerate a preview, clear the workflow, stop creating an automation, or select next if you like the automation preview.

<table id="choicetable_tkm_2nn_4dc"><thead><tr><th align="left" id="d202550e320">

Option

</th><th align="left" id="d202550e323">

Procedure

</th></tr></thead><tbody><tr><td id="d202550e329">

**Regenerate preview**

</td><td>

If the generated automation preview doesn’t meet your needs, you can update the AI instructions, and select **Regenerate preview**.Each time you build or rebuild an automation, the operation counts as an assist tracked by your AI subscription. To track your AI usage, see [Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md).

</td></tr><tr><td id="d202550e347">

**Clear**

</td><td>

If you want to clear the workflow that was created by AI and the AI instruction, select **Clear** and then select **Yes** in the Confirm clear automation window.

</td></tr><tr><td id="d202550e362">

**Cancel**

</td><td>

If you want to stop creating an automation and return to the RPA Desktop Design Studio home page, select **Cancel**. In the Confirm cancel window, select **Yes** to return to the previous screen.The generated automation workflows, if any, aren’t saved.

</td></tr><tr><td id="d202550e382">

**Next**

</td><td>

If the automation preview looks good, select **Next**.

</td></tr></tbody>
</table>7.  In the Create new automation window, fill in the fields.

    \[Omitted image "create-new-automation-now-assist.png"\] Alt text: Create new automation window that displays a form so that you can fill in the automation information for the generated workflow.

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

    **Important:** The automation is generated by AI. Be sure to check it for accuracy and make any edits before running.

    Close the displayed message for a clearer view.

    \[Omitted image "now-assist-automation-legal-notice.png"\] Alt text: Generated automation workflow that is displayed on the design surface.


## Result

The automation flow is launched on the design surface and it’s added as a Main activity in Activities.

**Parent Topic:**[Building automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-studio-build.md)


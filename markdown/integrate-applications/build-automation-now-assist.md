---
title: Build an automation with Now Assist
description: Enhance the automation logic with text instructions, either in an empty activity or by selecting a component in an existing one by using the Now Assist for RPA Hub application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Use, Now Assist for RPA Hub, Workflow Data Fabric]
---

# Build an automation with Now Assist

Enhance the automation logic with text instructions, either in an empty activity or by selecting a component in an existing one by using the Now Assist for RPA Hub application.

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

The **Build automation** option \(or the in-line prompting feature\) with the AI icon \(![AI icon.](../image/ai-sparkle-rpa-icon.png)\), appears only for those components that contain control output ports. For example, the AI icon doesn’t appear for components such as END or Break.

On the design surface, if you select multiple components and the AI icon \(![AI icon.](../image/ai-sparkle-rpa-icon.png)\), the in-line prompting trigger appears for the first component that you select.

If there are multiple control output ports for a component, the generated automation workflow is attached to the default or first control output port.

## Procedure

1.  In the RPA Desktop Design Studio, extend the automation logic with in-line prompting from the component level or from the design surface.

<table id="choicetable_lsf_npv_ydc"><thead><tr><th align="left" id="d548091e187">

Option

</th><th align="left" id="d548091e190">

Procedure

</th></tr></thead><tbody><tr><td id="d548091e196">

**From component level**

</td><td>

1.  On the design surface, select the required component and hover over the AI icon \(![AI icon.](../image/ai-sparkle-rpa-icon.png)\).
2.  Open the in-line prompting window by selecting the AI icon \(![AI icon.](../image/ai-sparkle-rpa-icon.png)\) and selecting **Build automation**.

You can also use the keyboard shortcut Ctrl+Enter to open the in-line prompting window.

![RPA Desktop Design Studio user interface showing the Build automation option after a component is selected, for example, Start.](../image/comp-level-inline-prompt-example.png "Build an automation logic by selecting a component")

 If you access in-line prompting from the component level, the automation workflow is generated to the default control output port of the component.

</td></tr><tr><td id="d548091e247">

**From design surface**

</td><td>

On the design surface, open the in-line prompting window by selecting and holding \(or right-clicking\) and selecting **Build automation**. You can also use the keyboard shortcut Ctrl+Enter to open the in-line prompting window.

![RPA Desktop Design Studio user interface that shows the Build automation option from an empty activity on the design surface.](../image/canvas-level-inline-prompt.png "Build an automation logic from an empty activity on the design surface")

If you access in-line prompting from the design surface, the generated automation workflow is an orphan flow. You must connect the control output ports.

</td></tr></tbody>
</table>2.  In the Build automation with Now Assist window, enter the Now Assist instructions and select the enter icon \(![Enter icon.](../image/enter-inline-prompt-icon.png)\).

    For example, `Launch www.servicenow.com from location 'C:\Program Files\Google\Chrome\Application\chrome.exe'`.

    The instruction text is used by the RPA bot generation skill to create your automation. Use short, direct, and clear sentences to describe the expected actions. Be specific and provide detailed descriptions of the automation logic. Avoid jargon and abbreviations.

    The following example shows that the Now Assist instructions are provided to build an automation to launch the ServiceNow website with Google Chrome.

    ![Build automation with Now Assist window that shows the instructions that are used by Now Assist to generate an automation workflow.](../image/inline-prompt-example.png "Build with Now Assist window")

    **Note:**

    For more information on example instructions and general guidelines for writing Now Assist instructions, see [Robotic Process Automation \(RPA\) bot generation](../concept/rpa-bot-generation.md). For more information about the limitations of the RPA bot generation skill, see [Limitations of Robotic Process Automation \(RPA\) bot generation skill](../reference/limitations-rpa-bot-gen-skill.md).

3.  In the Build with Now Assist window, close the window, cancel the workflow generation, reject an automation, or accept the automation preview.

<table id="choicetable_tkm_2nn_4dc"><thead><tr><th align="left" id="d548091e377">

Option

</th><th align="left" id="d548091e380">

Procedure

</th></tr></thead><tbody><tr><td id="d548091e386">

**Close**

</td><td>

If you want to close the Build with Now Assist window, select the close icon \(![Close icon.](../image/close-now-assist-rpa-icon.png)\), and then select **Close Now Assist** in the confirmation window.The generated automation workflow is discarded.

</td></tr><tr><td id="d548091e409">

**Stop generating**

</td><td>

If you want to cancel the workflow generation or update the instruction, select **Stop generating**. You can update the Now Assist instructions and select the enter icon \(![Enter icon.](../image/enter-inline-prompt-icon.png)\).

</td></tr><tr><td id="d548091e430">

**Reject**

</td><td>

If you aren’t satisfied with the automation preview, select **Reject**. Each time you build or rebuild an automation, the operation counts as an assist tracked by your Now Assist subscription. To track your Now Assist usage, see [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d548091e452">

**Accept**

</td><td>

If the automation preview looks good, select **Accept**.

</td></tr></tbody>
</table>    ![Build automation with Now Assist window that shows the Close and Stop generation options.](../image/inline-prompt-close-stop-screen.png "Close and Stop generation options")

    ![Build automation with Now Assist window that shows the Accept and Reject options.](../image/inline-prompt-accept-reject.png "Accept and Reject options")


## Result

The automation workflow that is generated by Now Assist is displayed on the design surface.

![Design surface displays the automation workflow that is generated by Now Assist.](../image/inline-prompt-accepted-screen.png "Generated automation workflow on the design surface")


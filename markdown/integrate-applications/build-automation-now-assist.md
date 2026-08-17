---
title: Build an automation with AI
description: Enhance the automation logic with AI text instructions, either in an empty activity or by selecting a component in an existing one by using the ServiceNow Otto for RPA Hub application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/build-automation-now-assist.html
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Build an automation with AI

Enhance the automation logic with AI text instructions, either in an empty activity or by selecting a component in an existing one by using the ServiceNow Otto for RPA Hub application.

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

The **Build automation** option \(or the in-line prompting feature\) with the AI icon \[Omitted image "ai-sparkle-rpa-icon.png"\] Alt text:, appears only for those components that contain control output ports. For example, the AI icon doesn’t appear for components such as END or Break.

On the design surface, if you select multiple components and the AI icon \[Omitted image "ai-sparkle-rpa-icon.png"\] Alt text:, the in-line prompting trigger appears for the first component that you select.

If there are multiple control output ports for a component, the generated automation workflow is attached to the default or first control output port.

## Procedure

1.  In the RPA Desktop Design Studio, extend the automation logic with in-line prompting from the component level or from the design surface.

<table id="choicetable_lsf_npv_ydc"><thead><tr><th align="left" id="d626213e201">

Option

</th><th align="left" id="d626213e204">

Procedure

</th></tr></thead><tbody><tr><td id="d626213e210">

**From component level**

</td><td>

1.  On the design surface, select the required component and hover over the AI icon \[Omitted image "ai-sparkle-rpa-icon.png"\] Alt text:.
2.  Open the in-line prompting window by selecting the AI icon \[Omitted image "ai-sparkle-rpa-icon.png"\] Alt text: and selecting **Build automation**.

You can also use the keyboard shortcut Ctrl+Enter to open the in-line prompting window.

\[Omitted image "comp-level-inline-prompt-example.png"\] Alt text: RPA Desktop Design Studio user interface showing the Build automation option after a component is selected, for example, Start.

 If you access in-line prompting from the component level, the automation workflow is generated to the default control output port of the component.

</td></tr><tr><td id="d626213e259">

**From design surface**

</td><td>

On the design surface, open the in-line prompting window by selecting and holding \(or right-clicking\) and selecting **Build automation**. You can also use the keyboard shortcut Ctrl+Enter to open the in-line prompting window.

\[Omitted image "canvas-level-inline-prompt.png"\] Alt text: RPA Desktop Design Studio user interface that shows the Build automation option from an empty activity on the design surface.

If you access in-line prompting from the design surface, the generated automation workflow is an orphan flow. You must connect the control output ports.

</td></tr></tbody>
</table>2.  In the Build automation with AI window, enter the AI instructions and select the enter icon \[Omitted image "enter-inline-prompt-icon.png"\] Alt text:.

    For example, `Launch www.servicenow.com from location 'C:\Program Files\Google\Chrome\Application\chrome.exe'`.

    The instruction text is used by the RPA bot generation skill to create your automation. Use short, direct, and clear sentences to describe the expected actions. Be specific and provide detailed descriptions of the automation logic. Avoid jargon and abbreviations.

    The following example shows that the AI instructions are provided to build an automation to launch the ServiceNow website with Google Chrome.

    \[Omitted image "inline-prompt-example.png"\] Alt text: Build automation with AI window that shows the instructions that are used by AI to generate an automation workflow.

    **Note:**

    For more information on example AI instructions and general guidelines, see [Robotic Process Automation \(RPA\) bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-bot-generation.md). For more information about the limitations of the RPA bot generation skill, see [Limitations of ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/limitations-rpa-bot-gen-skill.md).

3.  In the Build with AI window, close the window, cancel the workflow generation, reject an automation, or accept the automation preview.

<table id="choicetable_tkm_2nn_4dc"><thead><tr><th align="left" id="d626213e364">

Option

</th><th align="left" id="d626213e367">

Procedure

</th></tr></thead><tbody><tr><td id="d626213e373">

**Close**

</td><td>

If you want to close the Build with AI window, select the close icon \[Omitted image "close-now-assist-rpa-icon.png"\] Alt text:, and then select **Close AI** in the confirmation window.The generated automation workflow is discarded.

</td></tr><tr><td id="d626213e392">

**Stop generating**

</td><td>

If you want to cancel the workflow generation or update the instruction, select **Stop generating**. You can update the AI instructions and select the enter icon \[Omitted image "enter-inline-prompt-icon.png"\] Alt text:.

</td></tr><tr><td id="d626213e409">

**Reject**

</td><td>

If you aren’t satisfied with the automation preview, select **Reject**. Each time you build or rebuild an automation, the operation counts as an assist tracked by your AI subscription. To track your AI usage, see [Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md).

</td></tr><tr><td id="d626213e425">

**Accept**

</td><td>

If the automation preview looks good, select **Accept**.

</td></tr></tbody>
</table>    \[Omitted image "inline-prompt-close-stop-screen.png"\] Alt text: Build automation with AI window that shows the Close and Stop generation options.

    \[Omitted image "inline-prompt-accept-reject.png"\] Alt text: Build automation with AI window that shows the Accept and Reject options.


## Result

The automation workflow that is generated by AI is displayed on the design surface.

\[Omitted image "inline-prompt-accepted-screen.png"\] Alt text: Design surface displays the automation workflow that is generated by AI.

**Parent Topic:**[Building automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-studio-build.md)


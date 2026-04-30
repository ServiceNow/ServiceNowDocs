---
title: Example: Use AI agents to process badge-related requests automatically
description: As an HR representative, automatically process various badge requests by triggering AI agents that use desktop action tools from the Now Assist panel.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 4
breadcrumb: [Execute desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Example: Use AI agents to process badge-related requests automatically

As an HR representative, automatically process various badge requests by triggering AI agents that use desktop action tools from the Now Assist panel.

## Before you begin

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Remote Desktop must be enabled on your machine and your account must be granted Remote Desktop access permissions before you start using the AI Desktop Actions Execution workspace.
-   Theme must match between the systems used for recording and execution.

**Note:** Screen resolution and scaling must be the same between the systems used for recording and execution of desktop actions that are created prior to AI Desktop Actions v1.0.1.

Familiarize yourself with the AI Desktop Actions Execution workspace. For more information, see [AI Desktop Actions Execution workspace](../concept/agentic-desktop-excution-workspace.md).

Role required: now\_assist\_panel\_user

## About this task

AI agents use desktop actions that are designed in the AI Desktop Actions Design workspace as tools. When an AI agent is triggered from the Now Assist panel, it determines which desktop actions it can use to perform the automation. Once triggered, the automation is executed in the desktop-in-desktop mode within the AI Desktop Actions Execution workspace.

**Note:**

To avoid conflicts, do not run the AI Desktop Actions Execution workspace and RPA Attended Desktop mode at the same time.

## Procedure

1.  Navigate to **All** &gt; **Requests** &gt; **Assigned to you** and select all the pending requests that you would like to resolve.

2.  Open the Now Assist panel by using the Now Assist ![Now Assist icon.](../../../administer/now-assist-platform/images/wwna-icon.png) icon.

3.  On the Now Assist panel, enter `Use the badge management tool and process the selected requests`.

4.  Monitor the automation execution.

    ![AI Desktop Actions Execution workspace displaying "Listening for instructions" message for desktop session activation.](../image/execution-workspace-ready-ad.png "Execution workspace waiting for instruction from AI Agent Studio")

<table id="table_rhj_4vm_jhc"><thead><tr><th>

On Now Assist panel

</th><th>

On AI Desktop Actions Execution workspace

</th></tr></thead><tbody><tr><td>

An AI agent is triggered from the Now Assist panel to complete your request in the Execution workspace.

</td><td>

The Execution workspace is launched.

</td></tr><tr><td>

The AI agent prepares a plan and shows which desktop actions it uses for the execution.

</td><td>

AI agent logs in to the AI Desktop Actions Execution workspace.If it’s the first time you launch the Execution workspace using AI agents, you must enter the Windows Security credentials before proceeding.

The Execution workspace waits for instructions from AI Agent Studio.

</td></tr><tr><td>

The AI agent shows the steps as it executes them in the panel.The outcome of execution is shown in the Now Assist panel.

</td><td>

Once the plan is received, the AI agent starts executing the automation in the Execution workspace. The AI agent performs the tasks same as a human would.The Execution workspace shows the status of the execution. For more information, see [Execution statuses](../concept/agentic-desktop-excution-workspace.md#ad-execution-status).

</td></tr></tbody>
</table>5.  Interact with the automation when your inputs are required.

    -   **Step in**: take control whenever human inputs are required
    -   **Step out**: give the control back to the AI agent.
    **Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

6.  Use the smart sizing options to enable your desktop executions automatically adapt to your display.

<table id="choicetable_tbg_qwv_23c"><thead><tr><th align="left" id="d57558e382">

Option

</th><th align="left" id="d57558e385">

Description

</th></tr></thead><tbody><tr><td id="d57558e391">

**Fit to window**

</td><td>

Scales the execution screen to fit within the display area of the Execution workspace. The entire screen is visible without scrolling.Shortcut: `ctrl+shift+w`

</td></tr><tr><td id="d57558e404">

**Original resolution**

</td><td>

Displays the execution screen at its original resolution. Scroll bars appear if the screen is larger than the display area of the Execution workspace.Shortcut: `ctrl+shift+d`

</td></tr></tbody>
</table>
If the desktop session isn't sized correctly and mouse actions aren't working as expected after you enter the session, use the following keyboard shortcuts to resize the session:

`Ctrl + Shift + W`: Resize to window view.

`Ctrl + Shift + D`: Resize to actual desktop view.

**Parent Topic:**[Examples of executing desktop actions using AI agents](../concept/use-agentic-desktop.md)


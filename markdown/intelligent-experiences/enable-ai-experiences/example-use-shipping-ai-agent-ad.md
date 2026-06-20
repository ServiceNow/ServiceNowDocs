---
title: Example: Use AI agents to automatically enter data into the shipping management app
description: As a shipping coordinator, enter shipping details automatically from Excel to the Shipping Management app by triggering AI agents that use desktop action tools from the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/example-use-shipping-ai-agent-ad.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 5
breadcrumb: [Execute desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Example: Use AI agents to automatically enter data into the shipping management app

As a shipping coordinator, enter shipping details automatically from Excel to the Shipping Management app by triggering AI agents that use desktop action tools from the Now Assist panel.

## Before you begin

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Remote Desktop must be enabled on your machine and your account must be granted Remote Desktop access permissions before you start using the AI Desktop Actions Execution workspace.
-   Theme must match between the systems used for recording and execution.
-   Confirm that your firewall allows bidirectional traffic between the AI Desktop Actions application and your ServiceNow instance on the port 80 for HTTP and port 443 for HTTPs.

    If your organization uses non-standard ports for HTTP or HTTPS, confirm the correct ports with your IT administrator before proceeding.

    You must have full permissions to create and use system I/O communication pipes.

-   If applicable, confirm that the `snada://` custom URI protocol is registered to launch the AI Desktop Actions application in the browser.

**Note:** Screen resolution and scaling must be the same between the systems used for recording and execution of desktop actions that are created prior to AI Desktop Actions v1.0.1.

Familiarize yourself with the AI Desktop Actions Execution workspace. For more information, see [AI Desktop Actions Execution workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/agentic-desktop-excution-workspace.md).

Role required: now\_assist\_panel\_user

## About this task

AI agents use desktop actions that are designed in the AI Desktop Actions Design workspace as tools. When an AI agent is triggered from the Now Assist panel, it determines which desktop actions it can use to perform the automation. Once triggered, the automation is executed in the desktop-in-desktop mode within the AI Desktop Actions Execution workspace.

\[Omitted image "execution-workspace-ready-ad.png"\] Alt text: AI Desktop Actions Execution workspace displaying "Listening for instructions" message for desktop session activation.

**Note:**

To avoid conflicts, do not run the AI Desktop Actions Execution workspace and RPA Attended Desktop mode at the same time.

## Procedure

1.  Navigate to **All** &gt; **Incidents** &gt; **Assigned to you** and open an incident that you would like to resolve.

    When you open an incident, the Now Assist application checks if a plan is available by using AI agents and displays the `Now Assist has a plan for solving INCXXXXXXX. Open Now Assist Panel to view the plan.` message in a banner.

    **Note:** You can select the banner and directly go to the conversation on the Now Assist panel to complete the task.

2.  Open the Now Assist panel by using the Now Assist \[Omitted image "wwna-icon.png"\] Alt text: Now Assist icon. icon.

    Now Assist provides the resolution steps for the incident.

3.  On the Now Assist panel, enter `Read the shipping order details from the Excel spreadsheet located at: "C:\temp\Shipping orders.xlsx\". First, launch the Shipping Management application and login. Then, iterate through each order row in the spreadsheet and enter the data into the Shipping Management application.`.

4.  Monitor the automation execution.

<table id="table_rhj_4vm_jhc"><thead><tr><th>

On Now Assist panel

</th><th>

On AI Desktop Actions Execution workspace

</th></tr></thead><tbody><tr><td>

The AI agent is triggered and starts preparing a plan.

</td><td>

The Execution workspace launches. The AI agent logs in. If this is the first time you launch the Execution workspace using AI agents, enter your Windows Security credentials when prompted.

</td></tr><tr><td>

The agent shows which desktop actions it uses for the execution.

</td><td>

The Execution workspace waits for instructions from AI Agent Studio.

</td></tr><tr><td>

The AI agent shows each step as it executes them.

</td><td>

The AI agent performs the tasks in the Execution workspace that shows the execution status. For more information, see [Execution statuses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/agentic-desktop-excution-workspace.md).

</td></tr><tr><td>

The outcome of the execution is shown in the Now Assist panel.

</td><td>

The Execution workspace returns to the ready state.

</td></tr></tbody>
</table>    **Note:** If a pop-up window blocks the automation, select **Step in** to clear it, then select **Step out** to return control to the agent.

    During execution, the agent uses the values configured for each input. Values can come from two sources: static values set during design time, or mapped parameter records. If you also specify values for inputs configured for parameters in the agent instructions or in the Now Assist panel, the mapped parameter values override them.

5.  Interact with the automation when your inputs are required.

    -   **Step in**: take control whenever human inputs are required
    -   **Step out**: give the control back to the AI agent.
    **Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

6.  Use the smart sizing options to enable your desktop executions automatically adapt to your display.

<table id="choicetable_tbg_qwv_23c"><thead><tr><th align="left" id="d111677e432">

Option

</th><th align="left" id="d111677e435">

Description

</th></tr></thead><tbody><tr><td id="d111677e441">

**Fit to window**

</td><td>

Scales the execution screen to fit within the display area of the Execution workspace. The entire screen is visible without scrolling.Shortcut: `ctrl+shift+w`

</td></tr><tr><td id="d111677e454">

**Original resolution**

</td><td>

Displays the execution screen at its original resolution. Scroll bars appear if the screen is larger than the display area of the Execution workspace.Shortcut: `ctrl+shift+d`

</td></tr></tbody>
</table>
If the desktop session isn't sized correctly and mouse actions aren't working as expected after you enter the session, use the following keyboard shortcuts to resize the session:

`Ctrl + Shift + W`: Resize to window view.

`Ctrl + Shift + D`: Resize to actual desktop view.

**Parent Topic:**[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/use-agentic-desktop.md)


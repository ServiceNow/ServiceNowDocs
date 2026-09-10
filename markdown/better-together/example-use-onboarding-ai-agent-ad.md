---
title: Example: Execute employee onboarding automatically
description: As an HR coordinator, automatically onboard new employees by triggering an AI agent that executes the complete employee provisioning workflow from the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/better-together/example-use-onboarding-ai-agent-ad.html
release: australia
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 6
keywords: [employee onboarding, AI agent execution, desktop actions, HR automation, workflow automation]
breadcrumb: [Building desktop automations from Task Mining data, Solutions]
---

# Example: Execute employee onboarding automatically

As an HR coordinator, automatically onboard new employees by triggering an AI agent that executes the complete employee provisioning workflow from the ServiceNow Otto panel.

## Before you begin

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer for defined desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Theme must match between the systems used for recording and execution.
-   Remote Desktop must be enabled on your machine and your account must be granted Remote Desktop access permissions before you start using the AI Desktop Actions Execution workspace.
-   Add the end users who interact with the Execution workspace of AI Desktop Actions to the Remote Desktop Users group on the target machine and provide Remote Desktop access permissions for seamless automation execution.

    If your organization uses Group Policy, add the end users to a Microsoft Active Directory group that is permitted to use Remote Desktop through Group Policy on each target machine where desktop actions run.

    -   Local changes to the Remote Desktop Users group are temporary unless they align with Microsoft Active Directory entitlements.
    -   If the user is not entitled, Group Policy refresh automatically removes them from the group.
-   Confirm that your firewall allows bidirectional traffic between the AI Desktop Actions application and your ServiceNow instance on the port 80 for HTTP and port 443 for HTTPs.

    If your organization uses non-standard ports for HTTP or HTTPS, confirm the correct ports with your IT administrator before proceeding.

    You must have full permissions to create and use system I/O communication pipes.

-   If applicable, confirm that the `snada://` custom URI protocol is registered to launch the AI Desktop Actions application in the browser.
-   The employee onboarding AI agent is deployed and active in your instance.
-   The HR system \(containing the employee form\) and Microsoft 365 admin portal are accessible from the Windows machine.
-   New hire data is available in the designated Excel spreadsheet with columns for: Employee Name, Employee ID, Department, Manager, and Email Address.
-   The service account running the agent has credentials configured for HR system access and Microsoft 365 admin portal access.

**Note:** Screen resolution and scaling must be the same between the systems used for recording the agent's desktop actions and the execution environment.

Familiarize yourself with the AI Desktop Actions Execution workspace. For more information, see [AI Desktop Actions Execution workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-excution-workspace.md).

Role required: now\_assist\_panel\_user

## About this task

The employee onboarding AI agent automates the complete workflow of onboarding new hires. When you invoke the agent, it executes a series of desktop actions.

-   **Background task: Read Excel data**

    The agent opens the Excel file at the specified path and reads each row containing new hire information. This task runs silently without displaying the spreadsheet.

-   **On-screen task: Create an HR record**

    The agent opens the HR system, navigates to the employee creation form, and fills each field with data from Excel \(name, ID, department, manager\). The agent validates required fields and submits the form. You see the agent interacting with the form on the Windows desktop.

-   **On-screen task: Provision email account**

    The agent navigates to the Microsoft 365 admin portal, creates a new user account with the employee's email address, and assigns the appropriate licenses. This step makes the email account immediately available.

-   **On-screen task: Add to distribution list**

    The agent opens Microsoft Outlook, locates the team distribution list, and adds the new employee's email address as a member. This allows the employee to receive all team communications immediately upon activation.


Each action is orchestrated by the AI agent, which monitors completion and handles data transitions between steps. The entire workflow completes without manual intervention.

**Important:** The AI agent executes desktop actions on a Windows machine. Do not interact with the desktop or keyboard during agent execution. The agent requires exclusive access to the Windows desktop to perform its tasks accurately.

## Procedure

1.  Prepare the new hire data in the designated Excel spreadsheet.

    Verify that all required fields are populated: Employee Name, Employee ID, Department, Manager, and Email Address.

2.  In ServiceNow, navigate to your HR requests or onboarding queue to confirm all new hire records are ready for processing.

3.  Open the ServiceNow Otto panel by clicking the ServiceNow Otto \[Omitted image "icon-otto-outline-24.svg"\] icon in the ServiceNow interface.

4.  In the ServiceNow Otto panel, type: `Onboard new employees` or `Execute employee onboarding workflow`.

    The AI agent recognizes your request and displays a prompt asking for:

    -   **Excel file path**: Location of the spreadsheet containing new hire data
    -   **HR system URL** \(optional\): Pre-configured if the agent already has access
    -   **Distribution list name**: The team or department distribution list to add employees to
5.  Enter the required information and initiate execution.

6.  Monitor the automation execution.

<table id="table_rhj_4vm_jhc"><thead><tr><th>

On ServiceNow Otto panel

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

The AI agent performs the tasks in the Execution workspace that shows the execution status. For more information, see [AI Desktop Actions Execution workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-excution-workspace.md#ad-execution-status).

</td></tr><tr><td>

The outcome of the execution is shown in the ServiceNow Otto panel.

</td><td>

The Execution workspace returns to the ready state.

</td></tr></tbody>
</table>    **Note:** If a pop-up window blocks the automation, select **Step in** to clear it, then select **Step out** to return control to the agent.

    During execution, the agent uses the values configured for each input. Values can come from two sources: static values set during design time, or mapped parameter records. If you also specify values for inputs configured for parameters in the agent instructions or in the ServiceNow Otto panel, the mapped parameter values override them.

7.  After the agent completes execution, verify successful onboarding by checking:

    -   **HR system**

        New employee records display in the employee list with all fields populated correctly.

    -   **Microsoft 365 Admin Portal**

        New employee accounts appear in the user list with assigned licenses and active status

    -   **Microsoft Outlook distribution list**

        New employees appear as members of the team distribution list

    -   **Exchange online**

        New employee mailboxes are provisioned and ready for use

    -   **Execution report in ServiceNow**

        The agent execution record shows all steps completed successfully with timestamps

8.  If the agent encounters errors with specific employees, review the error details and resolve any data issues in the Excel spreadsheet or the target systems.

    Common issues include:

    -   Missing data in Excel fields \(all fields are required\)
    -   Duplicate employee IDs in the HR system
    -   Invalid email format in the email field
    -   Distribution list name spelled incorrectly or list not accessible
9.  For records that failed, resolve the issues and re-run the agent with corrected data.

    The agent will process only the failed records or you can re-run the complete batch.

10. Interact with the automation when your inputs are required.

    -   **Step in**: take control whenever human inputs are required
    -   **Step out**: give the control back to the AI agent.
    **Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

11. Use the smart sizing options to enable your desktop executions automatically adapt to your display.

<table id="choicetable_tbg_qwv_23c"><thead><tr><th align="left" id="d24024e583">

Option

</th><th align="left" id="d24024e586">

Description

</th></tr></thead><tbody><tr><td id="d24024e592">

**Fit to window**

</td><td>

Scales the execution screen to fit within the display area of the Execution workspace. The entire screen is visible without scrolling.Shortcut: `ctrl+shift+w`

</td></tr><tr><td id="d24024e605">

**Original resolution**

</td><td>

Displays the execution screen at its original resolution. Scroll bars appear if the screen is larger than the display area of the Execution workspace.Shortcut: `ctrl+shift+d`

</td></tr></tbody>
</table>

---
title: Install the Task Mining agent for Windows
description: Install the Task Mining desktop agent on Windows workstations using the installation wizard. Convert the agent installer to .intunewin format and deploy it to managed Windows devices through the Microsoft Intune admin center.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 3
breadcrumb: [Install the Task Mining agent, Configure, Task Mining, Platform Analytics]
---

# Install the Task Mining agent for Windows

Install the Task Mining desktop agent on Windows workstations using the installation wizard. Convert the agent installer to `.intunewin` format and deploy it to managed Windows devices through the Microsoft Intune admin center.

## Before you begin

Role required: Task Mining Agent Install

**Note:** You must be a part of the Task Mining Agent Install group with roles itil, sn\_tm\_core.service\_user, and agent\_client\_collector\_admin to install the Task Mining agent. If the group doesn't exist, create a group with that name and those roles manually. For more information, see Assign a role to a group.

You have access to the Microsoft Intune admin center.

## About this task

The Task Mining agent for Windows can be installed interactively using the installation wizard or silently from the command line. Both methods require a **Registration key** and **Instance URL** obtained from the Agent Installation page.

Deploying the Task Mining agent using Microsoft Intune involves converting the installer to `.intunewin` format using the Win32 Content Prep Tool, then configuring and deploying the application through the Intune admin center.

## Procedure

1.  Obtain the **Instance URL** and **Registration key**.

    The instance URL and registration key values are the same for Windows and macOS agents.

    1.  Navigate to **All** &gt; **Task Mining** &gt; **Agent Installation**.

    2.  Select an existing key or create one.

        ![Screenshot of registration key selection.](../image/tm-agent-3.png)

    3.  Copy the **Instance URL** and **Registration key** on the Agent Installation page.

    ![Screenshot of instance URL and registration key.](../image/tm-agent-4.png)

2.  Install the Windows agent by running the script.

    1.  Select the **Windows** tab on the **Agent Installation** page.

    2.  Select **Copy** next to **Download and Install** to collect the one-line installation script.

        ![Screenshot of Windows command line.](../image/tm-agent-6.png)

    3.  Open Windows **PowerShell** as an administrator.

    4.  Paste the script and press **Enter**.

    5.  Verify the instance URL, registration key, and installation destination, and select **Install**.

    The script downloads the installer, runs it with the instance URL and registration key, and reports whether installation succeeded or failed.

    The installer performs the following actions:

    -   Extracts application files to `C:\Program Files\ServiceNow\tm-agent` \(default\).
    -   Creates the **Task Mining Agent** \(`TaskMiningAgent`\) system service.
    -   Creates a folder for global configuration and logs at `C:\ProgramData\ServiceNow\tm-agent`.
    -   Creates a folder for gathered data and user-level logs at `C:\Users\%Username%\AppData\Local\ServiceNow\tm-agent`.
    -   Writes to the Windows Registry at:
        -   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\Task Mining Agent x.x.x.x`
        -   `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\TaskMiningAgent`
    **Note:** For a manual install, download the .exe by selecting **Download**, then install it manually either by running the .exe to start the installation wizard, or by using this command line: `tm-agent-setup-3.0.0.x.exe /S /INSTANCEURL="enter-instance-url" /REGKEY="enter-registration-key"`

3.  Download `IntuneWinAppUtil.exe` from the Microsoft Win32 Content Prep Tool GitHub repository and save it to a known location.

4.  Convert the agent installer to `.intunewin` format.

    1.  Open Command Prompt and navigate to the folder containing `IntuneWinAppUtil.exe`.

    2.  Run `IntuneWinAppUtil.exe`.

    3.  Enter the following values:

        -   **Source folder**: the folder containing the agent package \(for example, `C:\Temp\Task Mining Agent\Package`\).
        -   **Setup file**: `Deploy-Application.exe`.
        -   **Output folder**: the destination for the `.intunewin` file \(for example, `C:\Temp\Task Mining Agent\Intune File`\).
        -   **Catalog folder**: `N` \(No\).
    When conversion reaches 100%, `Deploy-Application.intunewin` is created in the output folder.

5.  In the Intune admin center, navigate to **Apps** &gt; **All Apps** &gt; **Create**.

6.  Select **Windows app \(Win32\)** as the app type.

7.  Upload the package file.

    1.  Select **Select app package file**.

    2.  Upload `Deploy-Application.intunewin` and select **OK**.

    3.  Update the **Name**, **Version**, **Publisher**, and **Description** fields.

    4.  Select **Select image** to add a logo and browse to the logo file.

8.  Configure the program settings, then select **Next**.

    -   **Install command**: `Deploy-Application.exe -DeploymentType "Install"`
    -   **Uninstall command**: `Deploy-Application.exe -DeploymentType "Uninstall"`
    -   **Device restart behavior**: **No specific action**
9.  Specify the device requirements, then select **Next**.

    -   **Operating system architecture**: 64-bit
    -   **Minimum OS version**: Windows 10 21H1 \(or as per your organizational policy\)
10. Configure the detection rules.

    1.  From the **Rules format** list, select **Manually configure detection rules** and select **+ Add**.

    2.  From the **Rule type** list, select **Registry**.

    3.  Enter the following values:

        -   **Key path**: `HKEY_LOCAL_MACHINE\SOFTWARE\CSE\Packages\Servicenow_TaskMiningAgent_2024.1.99`
        -   **Value name**: `Installed`
        -   **Detection method**: String Comparison
        -   **Operator**: Equals
        -   **Value**: `True`
    4.  Select **OK**, then select **Next**.

11. Configure dependencies, supersedence rules, or scope tags, or select **Next** through these pages.

12. Choose the deployment method, then select **Next**.

    -   **Available for enrolled devices**: users install the app from the Company Portal.
    -   **Required**: the app installs automatically on targeted devices or for specific user groups.
    **Important:** Test the deployment with a pilot group before rolling it out to a larger organization.

13. Review all settings, then select **Create**.


## Result

Check the Notifications section for upload progress. Once the package is uploaded, the application is ready for deployment.

## What to do next

Verify the deployment by opening the company portal on a target device, search for Task Mining Agent, and check the installation status.


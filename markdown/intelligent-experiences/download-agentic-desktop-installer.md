---
title: Download AI Desktop Actions installer
description: Download the AI Desktop Actions installer so that you can install AI Desktop Actions on your Windows machine for designing and running desktop actions.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-02"
reading_time_minutes: 2
breadcrumb: [Defined desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Download AI Desktop Actions installer

Download the AI Desktop Actions installer so that you can install AI Desktop Actions on your Windows machine for designing and running desktop actions.

## Before you begin

-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   Ensure that you install the AI Desktop Actions installer using Windows administrator privileges.
-   Ensure that the Desktop-in-Desktop settings are configured correctly.
-   Add the end users who interact with the Execution workspace of AI Desktop Actions to the Remote Desktop Users group on the target machine and provide Remote Desktop access permissions for seamless automation execution.

    If your organization uses Group Policy, add the end users to a Microsoft Active Directory group that is permitted to use Remote Desktop through Group Policy on each target machine where desktop actions run.

    -   Local changes to the Remote Desktop Users group are temporary unless they align with Microsoft Active Directory entitlements.
    -   If the user is not entitled, Group Policy refresh automatically removes them from the group.

Role required: Windows administrator

## Procedure

1.  Navigate to **All** &gt; **AI Desktop Actions** &gt; **Downloads**.

2.  In the AI Desktop Actions Downloads page, do any of the following actions to download the required application for Windows:

    -   Select the download icon \(![](../../rpa-hub/image/rpa-hub-download-icon.png)\).
    -   Select the copy link \(![](../../rpa-hub/image/rpa-hub-copyurl-icon.png)\). In a browser, right-click and select the **paste and go** option.
    ![Downloads page for downloading AI Desktop Actions installer.](../image/agentic-desktop-download-msi.png)

    The system might prompt you to save or open the file.

    **Note:** Depending on your browser setting, the browser might automatically save the file to your Downloads folder.

3.  Execute the application installation file \(.msi file\).

4.  Follow the on-screen instructions to install the application.

    AI Desktop Actions is installed in a per-machine folder by default, making it available to all users. You can change the folder location during setup.

5.  Keep the option **Enable Remote Desktop access for the logged-in user** selected to automatically add the logged-in user to the Remote Desktop Users group.

    ![AI Desktop Actions Setup welcome screen.](../image/ad-set-up-remote-user.png)

6.  If not already installed, download and install the .Net Desktop Runtime framework.

    The installer validates if required .NET Desktop Runtime is installed or not on the user machine. If not installed, the installer provides a link to instructions for downloading and installing the same. For more information, see [Download and install .Net Desktop Runtime for AI Desktop Actions](install-dot-network-framework-ad.md).

    ![NET Desktop Runtime required screen.](../image/ad-set-up-dot-net-installation.png)


If AI Desktop Actions is not installed using Windows administrator privileges, you may encounter issues with the desktop session in the Execution workspace. To fix the issue, perform the following steps.

1.  Navigate to the **SessionRegistry** folder of the AI Desktop Actions installation directory.
2.  Right-click **SN.AGENTICDESKTOP.SESSION.REGISTER.exe** and select **Run as administrator**.
3.  Restart your system.

## What to do next

Use AI Desktop Actions to design desktop actions. For more information, see [Defined path desktop actions in AI Desktop Actions](../concept/desktop-actions-designer-workspace-ad.md).

**Parent Topic:**[Configuring AI Desktop Actions for defined path desktop actions](../concept/ad-defined-path-da.md)


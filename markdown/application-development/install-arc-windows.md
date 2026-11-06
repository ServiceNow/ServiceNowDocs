---
title: Download and install Arc on Windows
description: Install ServiceNow Arc on your Windows computer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/install-arc-windows.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [install on Windows, Windows Hypervisor Platform, virtualization, MSI, agent sandbox]
breadcrumb: [Configure, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Download and install Arc on Windows

Install ServiceNow Arc on your Windows computer.

## Before you begin

Your computer must meet these system requirements:

-   Windows 11, x64
-   Administrator privileges on the computer, to install the MSI and turn on the Windows Hypervisor Platform feature
-   At least 8 GB of RAM, with 16 GB recommended
-   About 50 GB of free disk space

Role required: sn\_app\_arc.admin or sn\_app\_arc.user

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Arc** &gt; **Downloads**.

2.  Download the Windows installer.

3.  In your **Downloads** folder, double-click the ServiceNow Arc MSI installer file.

    Windows Installer prepares the installation, and the setup wizard opens.

4.  Restart your computer.

5.  On the welcome screen and the **Destination Folder** screen, select **Next**.

6.  Select **Install**, and approve the administrator prompt.

    The setup wizard installs ServiceNow Arc. If the Windows Hypervisor Platform isn't on yet, the installer shows **Enabling Windows Hypervisor Platform**, which can take a few minutes, and asks you to restart the computer when it finishes.

7.  On the completed screen, select **Finish**.

    To open Arc right away, leave the launch check box selected.

8.  To open Arc later, double-click its desktop icon, or select **Start**, search for `Arc`, and select the app.

9.  Sign in with your ServiceNow credentials.

    The first time you sign in, Arc downloads the sandbox image and sets up the sandbox, and the sidebar shows **Provisioning sandbox**. This happens once, and later launches are faster. To follow the progress, select **Provisioning sandbox**.


## Result

When **Sandbox image ready**, **Hyper-V runtime prepared**, and **MicroVM sandbox ready** are all complete, the sidebar shows **Sandbox Provisioned**, and you can start a chat.

## What to do next

To finish setting up Arc, see [Set up ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/set-up-cowork.md).

For more information about resolving common issues, see [Troubleshoot Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/troubleshoot-arc.md).

After you install Arc, it keeps itself up to date. It checks for updates at startup, and when you check for updates from **Settings**.

**Parent Topic:**[Configuring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-configuring.md)


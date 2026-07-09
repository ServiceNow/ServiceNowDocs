---
title: Install MID Server with the command line installer
description: Using the ITOM Infra Services Workspace, MID Servers can be deployed with the command line installer. The command line installer automates many of the processes, especially for first time installations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/mid-server/mid-ipki-install-command.html
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Install MID Server with the command line installer

Using the ITOM Infra Services Workspace, MID Servers can be deployed with the command line installer. The command line installer automates many of the processes, especially for first time installations.

## Before you begin

Role required: admin

<table id="table_skp_xr4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>## Procedure

1.  On the instance, navigate to **ITOM Infra Services Workspace**.

2.  In the **Set up a MID** panel, select **Download a MID Server**.

3.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

4.  To begin the installation process, provide the following information.

    -   **Authentication type:** ServiceNow certificate
    -   **I'm installing the MID Server on:** Select the option corresponding to the host
    -   **I want to install using a:** Command Line Installer
5.  To proceed, select **Next: Configuration**.

6.  Provide the name of the MID Server.

    You can provide a note about the MID Server in the MID Server purpose field. This note does not affect anything about the MID Server's roles or performance.

    In addition, you can reveal the **Advanced configuration settings** to **Manually set MID Server user**, provide the IP address and port number for **Proxy configuration**, or **Manually set service name**.

7.  To proceed, select **Next**.

8.  Create a dedicated non-admin \(for Windows hosts\) or non-root \(for Linux hosts\) service account for the MID Server.

    This account must have the **Log in as a Service** right and **Read, Write, Execute** permissions for the MID Server installation folder. For more information, see [Configure Windows MID Server service credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md) and [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

9.  Open PowerShell in the intended MID Server installation directory and run the command provided by the installer.

    This command downloads the MID Server package from ServiceNow and connects it to your instance. This command token expires in 24 hours. If it has expired, use the refresh button on the installer to generate a new one.

10. Verify that the MID Server is running.

    The MID Server record appears in the installer step once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `agent\logs` to identify the issue.

11. Set up your MID Server applications and capabilities by selecting the MID Server record and navigating to the related lists.

    By default, the MID Server is not be able to run any applications or capabilities.


## What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.

**Parent Topic:**[Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-installation-landing.md)


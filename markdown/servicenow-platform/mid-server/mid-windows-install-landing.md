---
title: Installing MID Server on Windows
description: Using the ITOM Infra Services Workspace, MID Servers can be deployed to Windows with a variety of authentication and installation methods. For authentication, choose between private key JWT, basic authentication, or mutual authentication.Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file.Using the ITOM Infra Services Workspace, MID Servers can be deployed with the Windows installer \(MSI\). Basic authentication is less secure than other authentication types.Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file. Basic authentication is less secure than other authentication types.Using the ITOM Infra Services Workspace, MID Servers can be deployed for mutual authentication. Mutually authentication must be authorized and prepared on the instance by ServiceNow support.Using the ITOM Infra Services Workspace, MID Servers can be deployed using ZIP for mutual authentication. Mutually authentication must be authorized and prepared on the instance by ServiceNow support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/mid-server/mid-windows-install-landing.html
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 23
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Installing MID Server on Windows

Using the ITOM Infra Services Workspace, MID Servers can be deployed to Windows with a variety of authentication and installation methods. For authentication, choose between private key JWT, basic authentication, or mutual authentication.

<table id="table_skp_xr4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>-   Verify that the host computer satisfies the [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).
-   The MID Server requires the minimum PowerShell version 3.0 and supports versions up to PowerShell 5.1.
-   Ensure that the Microsoft Application Experience Lookup Service is enabled on the MID Server host. If this service is disabled, the MID Server auto-upgrade might fail, causing the MID Server to go down. For information on managing issues with the Application Experience service, see [KB0597552](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0597552).

Java 17.0.12 is bundled with the MID Server installer package and is installed on the host for all new MID Servers. The installer automatically configures Java 17.0.12 to run in your environment. No additional configuration is required. This version supports both 64-bit Windows MID Servers and 64-bit Linux MID Servers. The MID Server requires a minimum JRE version 17.0.10, and recommended version 17.0.12. If you are using a lower version than 17.0.10, you may see encryption related issues.

**Note:** ServiceNow no longer supports new installations of 32-bit MID Servers or upgrades to version Rome. New MID Server installation are blocked through RPM and MSI installer on the following operating systems:

-   CentOS 7
-   Windows server 2008
-   Windows server 2008 R2
-   Windows 8
-   Windows 10

MID Servers can be manually installed to any operating system with the ZIP file, however Windows 10 is unsupported. Unsupported MID Servers auto-upgrading to Rome create an issue record in MID Server Issues \(ecc\_agent\_issue\). For more information, see [Supported platform changes for MID Server \[KB0863694\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863694).

Testing showed that the MID Server works as expected with Oracle Java 11 version 17.0.10. If you need to upgrade the JRE to a different version, then coordinate with the appropriate account representative for support.

Upgraded MID Servers might use different Java versions depending on their operating system versions.

-   MID Servers upgraded from earlier versions use the OpenJDK provided with the MID Server installer. This version of the OpenJDK was tested and certified for use with these MID Servers.
-   MID Servers upgraded on any other operating system versions also automatically upgrade the JRE to the version provided with the installation package.

**Parent Topic:**[Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-installation-landing.md)

## Install MID Server on Windows with private key JWT using ZIP

Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file.

### Before you begin

Role required: admin

### Procedure

1.  On the instance, navigate to **ITOM Infra Services Workspace**.

2.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

3.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

4.  To begin the installation process, provide the following information.

    -   **Authentication type:** ServiceNow certificate
    -   **I'm installing the MID Server on:** Windows
    -   **I want to install using a:** Manual configuration via zip file
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

5.  To proceed, select **Next: Configuration**.

6.  Provide the name of the MID Server.

    You can provide a note about the MID Server in the MID Server purpose field. This note does not affect anything about the MID Server's roles or performance.

    In addition, you can reveal the **Advanced configuration settings** to **Manually set MID Server user**, provide the IP address and port number for **Proxy configuration**, or **Manually set service name**.

7.  To configure a Service Account, create a dedicated non-admin service account for the MID Server.

    This account must have the **Log in as a Service** right and **Read, Write, Execute** permissions for the MID Server installation folder. For more information, see [Configure Windows MID Server service credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md).

8.  Download the Windows ZIP file from the installation plan.

9.  On the Windows host machine, extract the ZIP file into the intended install directory for the MID Server.

10. Go to the installation plan and generate a token to register your ServiceNow-provided certificate.

    This token allows a new MID Server to authenticate to this instance for the first time. It is single-use and expires in 24 hours. You can regenerate this key if needed.

11. Paste the code block into the `config.xml` file.

    **Note:** This token is generated with a default MID Server user. If you want to use a specific MID Server user, select **Specify MID Server user** to generate the token.

12. To configure your MID Server, navigate to the agent folder and configure the following properties in `config.xml` with a text editor:

<table id="table_hqp_4lj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

url

</td><td>

Set to your instance URL \(https://YOUR\_INSTANCE.service-now.com/\)

</td></tr><tr><td>

name

</td><td>

Set to your MID Server name. This name must be unique and cannot contain spaces or special characters. \(mid-uswest-01\)

</td></tr></tbody>
</table>    If your MID Server connects to the instance through a proxy, uncomment and configure the following properties as well:

<table id="table_jqp_4lj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

mid.proxy.use\_proxy

</td><td>

Set to true

</td></tr><tr><td>

mid.proxy.host

</td><td>

Set to your proxy value \(proxy.example.com\)

</td></tr><tr><td>

mid.proxy.port

</td><td>

Set to your proxy port \(defaults to 8080\)

</td></tr><tr><td>

mid.proxy.password

</td><td>

Optional, set to your proxy password

</td></tr></tbody>
</table>13. Navigate to `\conf\wrapper-override.conf` and edit the following:

<table id="table_nc3_llj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

wrapper.ntservice.account

</td><td>

Set to service account name \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

wrapper.ntservice.password.prompt

</td><td>

Uncomment the parameter to enable it, but do not change it.

</td></tr><tr><td>

wrapper.ntservice.permissions.1.account

</td><td>

Set to service account name \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

wrapper.ntservice.permissions.1.allow

</td><td>

Uncomment the parameter to enable it, but do not change it.

</td></tr><tr><td>

wrapper.name

</td><td>

Set a name for this MID Server. This name must be unique on the host. \(mid-uswest-01\)

</td></tr></tbody>
</table>14. Start your MID Server by opening a command prompt, navigating to the agent folder, and running `start.bat`.

    If a service account was configured, enter the password when prompted. The MID Server then starts and connects to the instance.

15. Set up your MID Server applications and capabilities by selecting the MID Server record and navigating to the related lists.

    By default, the MID Server is not be able to run any applications or capabilities.


### What to do next

To optimize your MID Server, consider configuring it to be part of a cluster or set IP ranges. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md).

## Install MID Server on Windows with basic authentication

Using the ITOM Infra Services Workspace, MID Servers can be deployed with the Windows installer \(MSI\). Basic authentication is less secure than other authentication types.

### Before you begin

Role required: admin

### Procedure

1.  On the instance, navigate to **ITOM Infra Services Workspace**.

2.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

3.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

4.  To begin the installation process, provide the following information.

    -   **Authentication type:** Basic authentication
    -   **I'm installing the MID Server on:** Windows
    -   **I want to install using a:** Windows installer \(MSI\)
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

5.  To proceed, select **Next: Download and Install**.

6.  Create a ServiceNow user for this MID Server and grant it **mid\_server** role.

    For more information on creating users, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

    **Note:** This user should be unique for each MID Server using basic authentication.

7.  Download the installer `.msi` to the desired MID Server host.

8.  Open the installer with Administrator level privileges.

    For more details, see [Install a MID Server on Windows with guided installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md).

9.  Create a dedicated non-admin service account for the MID Server.

    This account must have the **Log in as a Service** right and **Read, Write, Execute** permissions for the MID Server installation folder. For more information, see [Configure Windows MID Server service credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md).

10. Verify that the MID Server is running.

    The MID Server record appears in the installer step once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `agent\logs` to identify the issue.


### What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.

## Install MID Server on Windows with basic authentication using ZIP

Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file. Basic authentication is less secure than other authentication types.

### Before you begin

Role required: admin

### Procedure

1.  On the instance, navigate to **ITOM Infra Services Workspace**.

2.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

3.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

4.  To begin the installation process, provide the following information.

    -   **Authentication type:** Basic authentication
    -   **I'm installing the MID Server on:** Windows
    -   **I want to install using a:** Manual configuration via zip file
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

5.  To proceed, select **Next: Download and Install**.

6.  Download the Windows ZIP file from the installation plan.

7.  On the Windows host machine, extract the ZIP file into the intended install directory for the MID Server.

8.  To configure a Service Account, create a dedicated non-admin service account for the MID Server.

    This account must have the **Log in as a Service** right and **Read, Write, Execute** permissions for the MID Server installation folder. For more information, see [Configure Windows MID Server service credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md).

9.  Navigate to `\conf\wrapper-override.conf` and edit the following:

<table id="table_nc3_llj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

wrapper.ntservice.account

</td><td>

Set to service account name \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

wrapper.ntservice.password.prompt

</td><td>

Uncomment the parameter to enable it, but do not change it.

</td></tr><tr><td>

wrapper.ntservice.permissions.1.account

</td><td>

Set to service account name \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

wrapper.ntservice.permissions.1.allow

</td><td>

Uncomment the parameter to enable it, but do not change it.

</td></tr><tr><td>

wrapper.name

</td><td>

Set a name for this MID Server. This name must be unique on the host. \(mid-uswest-01\)

</td></tr></tbody>
</table>10. To configure your MID Server, navigate to the agent folder and configure the following properties in `config.xml` with a text editor:

<table id="table_sxr_lxx_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

url

</td><td>

Set to your instance URL \(https://YOUR\_INSTANCE.service-now.com/\)

</td></tr><tr><td>

mid.instance.username

</td><td>

Enter the name of the MID Server user that you already created. The MID Server user must have the mid\_server role.

</td></tr><tr><td>

mid.instance.password

</td><td>

Enter the password for the user in the ServiceNow MID Server username.

</td></tr><tr><td>

name

</td><td>

Set to your MID Server name. This name must be unique and cannot contain spaces or special characters. \(mid-uswest-01\)

</td></tr></tbody>
</table>    If your MID Server connects to the instance through a proxy, uncomment and configure the following properties as well:

<table id="table_jqp_4lj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

mid.proxy.use\_proxy

</td><td>

Set to true

</td></tr><tr><td>

mid.proxy.host

</td><td>

Set to your proxy value \(proxy.example.com\)

</td></tr><tr><td>

mid.proxy.port

</td><td>

Set to your proxy port \(defaults to 8080\)

</td></tr><tr><td>

mid.proxy.password

</td><td>

Optional, set to your proxy password

</td></tr></tbody>
</table>11. Start your MID Server by opening a command prompt, navigating to the agent folder, and running `start.bat`.

    If a service account was configured, enter the password when prompted. The MID Server then starts and connects to the instance.

    The MID Server appears in the record table once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `agent\logs` to identify the issue.

12. Set up your MID Server applications and capabilities by selecting the MID Server record and navigating to the related lists.

    By default, the MID Server is not be able to run any applications or capabilities.


### What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.

## Install MID Server on Windows with mutual authentication

Using the ITOM Infra Services Workspace, MID Servers can be deployed for mutual authentication. Mutually authentication must be authorized and prepared on the instance by ServiceNow support.

### Before you begin

Role required: admin

### Procedure

1.  To enable Mutual Authentication, the instance must be authorized and prepared by ServiceNow support.

    For more information, see [Enable MID Server mutual authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/install-mid-mutual-auth.md).

2.  On the instance, navigate to **ITOM Infra Services Workspace**.

3.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

4.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

5.  To begin the installation process, provide the following information.

    -   **Authentication type:** Custom certificate \(mutual TLS\)
    -   **I'm installing the MID Server on:** Windows
    -   **I want to install using a:** Windows installer \(MSI\)
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

6.  To proceed, select **Next: Download and Install**.

7.  Create a ServiceNow user for this MID Server and grant it **mid\_server** role.

    For more information on creating users, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

    **Note:** This user should be unique for each MID Server using basic authentication.

8.  Download the installer `.msi` to the desired MID Server host.

9.  Open the installer with Administrator level privileges.

    For more details, see [Install a MID Server on Windows with guided installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md).

10. To configure a Service Account, create a dedicated non-admin service account for the MID Server.

    This account must have the **Log in as a Service** right and **Read, Write, Execute** permissions for the MID Server installation folder. For more information, see [Configure Windows MID Server service credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md).

11. Verify that the MID Server is running.

    The MID Server record appears in the installer step once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `agent\logs` to identify the issue.


### What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.

## Install MID Server on Windows with mutual authentication using ZIP

Using the ITOM Infra Services Workspace, MID Servers can be deployed using ZIP for mutual authentication. Mutually authentication must be authorized and prepared on the instance by ServiceNow support.

### Before you begin

Role required: admin

### Procedure

1.  To enable Mutual Authentication, the instance must be authorized and prepared by ServiceNow support.

    For more information, see [Enable MID Server mutual authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/install-mid-mutual-auth.md).

2.  On the instance, navigate to **ITOM Infra Services Workspace**.

3.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

4.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

5.  To begin the installation process, provide the following information.

    -   **Authentication type:** Custom certificate \(mutual TLS\)
    -   **I'm installing the MID Server on:** Windows
    -   **I want to install using a:** Manual configuration via zip file
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

6.  To proceed, select **Next: Download and Install**.

7.  Download the Windows ZIP file from the installation plan.

8.  On the Windows host machine, extract the ZIP file into the intended install directory for the MID Server.

9.  To configure a Service Account, create a dedicated non-admin service account for the MID Server.

    This account must have the **Log in as a Service** right and **Read, Write, Execute** permissions for the MID Server installation folder. For more information, see [Configure Windows MID Server service credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-install-prereqs.md).

10. Navigate to `\conf\wrapper-override.conf` and edit the following:

<table id="table_nc3_llj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

wrapper.ntservice.account

</td><td>

Set to service account name \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

wrapper.ntservice.password.prompt

</td><td>

Uncomment the parameter to enable it, but do not change it.

</td></tr><tr><td>

wrapper.ntservice.permissions.1.account

</td><td>

Set to service account name \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

wrapper.ntservice.permissions.1.allow

</td><td>

Uncomment the parameter to enable it, but do not change it.

</td></tr><tr><td>

wrapper.name

</td><td>

Set a name for this MID Server. This name must be unique on the host. \(mid-uswest-01\)

</td></tr></tbody>
</table>11. To configure your MID Server, navigate to the agent folder and configure the following properties in `config.xml` with a text editor:

<table id="table_sxr_lxx_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

url

</td><td>

Set to your instance URL \(https://YOUR\_INSTANCE.service-now.com/\)

</td></tr><tr><td>

mid.instance.username

</td><td>

Enter the name of the MID Server user that you already created. The MID Server user must have the mid\_server role.

</td></tr><tr><td>

mid.instance.password

</td><td>

Enter the password for the user in the ServiceNow MID Server username.

</td></tr><tr><td>

name

</td><td>

Set to your MID Server name. This name must be unique and cannot contain spaces or special characters. \(mid-uswest-01\)

</td></tr></tbody>
</table>    If your MID Server connects to the instance through a proxy, uncomment and configure the following properties as well:

<table id="table_jqp_4lj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

mid.proxy.use\_proxy

</td><td>

Set to true

</td></tr><tr><td>

mid.proxy.host

</td><td>

Set to your proxy value \(proxy.example.com\)

</td></tr><tr><td>

mid.proxy.port

</td><td>

Set to your proxy port \(defaults to 8080\)

</td></tr><tr><td>

mid.proxy.password

</td><td>

Optional, set to your proxy password

</td></tr></tbody>
</table>12. Start your MID Server by opening a command prompt, navigating to the agent folder, and running `start.bat`.

    If a service account was configured, enter the password when prompted. The MID Server then starts and connects to the instance.

    The MID Server appears in the record table once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `\agent\logs` to identify the issue.

13. Set up your MID Server applications and capabilities by selecting the MID Server record and navigating to the related lists.

    By default, the MID Server is not be able to run any applications or capabilities.


### What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.


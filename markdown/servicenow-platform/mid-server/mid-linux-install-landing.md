---
title: Installing MID Server on Linux
description: Using the ITOM Infra Services Workspace, MID Servers can be deployed to Linux with a variety of authentication and installation methods. For authentication, choose between private key JWT, basic authentication, or mutual authentication.Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file.Using the ITOM Infra Services Workspace, MID Servers can be deployed with the Linux installer. Basic authentication is less secure than other authentication types.Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file. Basic authentication is less secure than other authentication types.Using the ITOM Infra Services Workspace, MID Servers can be deployed for mutual authentication. Mutually authentication must be authorized and prepared on the instance by ServiceNow support.Using the ITOM Infra Services Workspace, MID Servers can be deployed using ZIP for mutual authentication. Mutually authentication must be authorized and prepared on the instance by ServiceNow support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/mid-server/mid-linux-install-landing.html
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 22
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Installing MID Server on Linux

Using the ITOM Infra Services Workspace, MID Servers can be deployed to Linux with a variety of authentication and installation methods. For authentication, choose between private key JWT, basic authentication, or mutual authentication.

<table id="table_skp_xr4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>To install Linux on MID Server, the RedHat/CentOS systems require RPM while Debian \(Ubuntu\) systems require DEB. The default installation location is `/opt/servicenow/mid`. Installing DEB in user defined directories is not supported.

To improve security, this procedure installs and run the MID Server service as a non-root user. Root privilege is required to deploy and configure a MID Server on a Linux server. A non-root user can manage a service only if they have the required permissions. For more details, see [PolicyKit issues with Linux MID Servers using non-admin accounts \[KB0815542\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0815542).

**Note:** ServiceNow no longer supports new installations of 32-bit MID Servers or upgrades to version Rome. New MID Server installation are blocked through RPM and MSI installer on the following operating systems:

-   CentOS 7
-   Windows server 2008
-   Windows server 2008 R2
-   Windows 8
-   Windows 10

MID Servers can be manually installed to any operating system with the ZIP file, however Windows 10 is unsupported. Unsupported MID Servers auto-upgrading to Rome create an issue record in MID Server Issues \(ecc\_agent\_issue\). For more information, see [Supported platform changes for MID Server \[KB0863694\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863694).

Java 17.0.12 is bundled with the MID Server installer package and is installed on the host for all new MID Servers. The installer automatically configures Java 17.0.12 to run in your environment. No additional configuration is required. This version supports both 64-bit Windows MID Servers and 64-bit Linux MID Servers. The MID Server requires a minimum JRE version 17.0.10, and recommended version 17.0.12. If you are using a lower version than 17.0.10, you may see encryption related issues.

**Note:** Linux MID Servers require glibC version 2.17. The library must be updated for JRE 11. On 64-bit Linux systems, you must install the 32-bit [GNU C library](http://www.gnu.org/software/libc/) \(glibc\). The installation command for CentOS is: `yum install glibc.i686`

Testing showed that the MID Server works as expected with Oracle Java 11 version 17.0.10. If you need to upgrade the JRE to a different version, then coordinate with the appropriate account representative for support.

**Parent Topic:**[Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-installation-landing.md)

## Install MID Server on Linux with private key JWT using ZIP

Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file.

### Before you begin

Role required: admin

### Procedure

1.  On the instance, navigate to **ITOM Infra Services Workspace**.

2.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

3.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

4.  To begin the installation process, provide the following information.

    -   **Authentication type:** ServiceNow certificate
    -   **I'm installing the MID Server on:** Linux
    -   **I want to install using a:** Manual configuration via zip file
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

5.  To proceed, select **Next: Configuration**.

6.  Configure a Non-Root User by creating a dedicated non-root account for the MID Server.

7.  Download the Linux ZIP file from the installation plan.

8.  On the Linux host machine, extract the ZIP file into the intended install directory for the MID Server.

9.  Go to the installation plan and generate a token to register your ServiceNow-provided certificate.

    This token allows a new MID Server to authenticate to this instance for the first time. It is single-use and expires in 24 hours. You can regenerate this key if needed.

10. Paste the code block into the `config.xml` file.

    **Note:** This token is generated with a default MID Server user. If you want to use a specific MID Server user, select **Specify MID Server user** to generate the token.

11. To configure your MID Server, navigate to the agent folder and configure the following properties in config.xml with a text editor:

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
</table>12. Navigate to `mid.shconf_override` and edit the following:

<table id="table_i3s_kmj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

APP\_NAME

</td><td>

Set to a unique MID Server Name \(mid\_centos\_1\)

</td></tr><tr><td>

APP\_LONG\_NAME

</td><td>

Set to a unique MID Server Name \(ServiceNow MID Server Centos 1\)

</td></tr><tr><td>

RUN\_AS\_USER

</td><td>

Set to non-root username \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

GROUP\_NAME

</td><td>

Optional: Add name of group directory to own MID Server folder

</td></tr><tr><td>

PROMPT\_BEFORE\_OWNERSHIP\_CHANGE

</td><td>

Set to true

</td></tr></tbody>
</table>13. Start your MID Server by opening a command prompt, navigating to the agent folder, and running `start.bat`.

    If a service account was configured, enter the password when prompted. The MID Server then starts and connects to the instance.

14. Set up your MID Server applications and capabilities by selecting the MID Server record and navigating to the related lists.

    By default, the MID Server is not be able to run any applications or capabilities.


### What to do next

To optimize your MID Server, consider configuring it to be part of a cluster or set IP ranges. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md).

## Install MID Server on Linux with basic authentication

Using the ITOM Infra Services Workspace, MID Servers can be deployed with the Linux installer. Basic authentication is less secure than other authentication types.

### Before you begin

Role required: admin

### Procedure

1.  On the instance, navigate to **ITOM Infra Services Workspace**.

2.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

3.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

4.  To begin the installation process, provide the following information.

    -   **Authentication type:** Basic authentication
    -   **I'm installing the MID Server on:** Linux
    -   **I want to install using a:** Linux \(RPM, DBM, or Docker\)
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

5.  To proceed, select **Next: Download and Install**.

6.  Create a ServiceNow user for this MID Server and grant it **mid\_server** role.

    For more information on creating users, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

    **Note:** This user should be unique for each MID Server using basic authentication.

7.  Download either the MID Server installer RPM file for RedHat/CentOS or the DEB file for Debian \(Ubuntu\) systems.

    For more information, see [Install a MID Server on Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md).

8.  Place the installer file on the MID Server host.

9.  Install the package for the appropriate system with the following commands:

    1.  Install the RPM package for RedHat systems with the command: `sudo rpm -ivh --nodeps package_name.rpm.`

    2.  Install the DEB package for Debian systems with the following command: `sudo dpkg -i package_name.deb.`

10. To configure the MID Server service, run the command `./installer.sh` from the agent folder as a user with root privilege, and provide the required inputs.

11. Verify that the MID Server is running.

    The MID Server record appears in the installer step once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `agent\logs` to identify the issue.


### What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.

## Install MID Server on Linux with basic authentication using ZIP

Using the ITOM Infra Services Workspace, MID Servers can be deployed and configured manually with a ZIP file. Basic authentication is less secure than other authentication types.

### Before you begin

Role required: admin

### Procedure

1.  On the instance, navigate to **ITOM Infra Services Workspace**.

2.  From the home page, in the **Set up a MID** panel, select **Download a MID Server**.

3.  In the **Download and set up a MID Server** panel, select **Set up a MID Server**.

4.  To begin the installation process, provide the following information.

    -   **Authentication type:** Basic authentication
    -   **I'm installing the MID Server on:** Linux
    -   **I want to install using a:** Manual configuration via zip file
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

5.  To proceed, select **Next: Download and Install**.

6.  Download the Linux ZIP file from the installation plan.

7.  On the Linux host machine, extract the ZIP file into the intended install directory for the MID Server.

8.  Configure a Non-Root User by creating a dedicated non-root account for the MID Server, then navigate to the `mid.shconf_override` and edit the following:

<table id="table_i3s_kmj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

APP\_NAME

</td><td>

Set to a unique MID Server Name \(mid\_centos\_1\)

</td></tr><tr><td>

APP\_LONG\_NAME

</td><td>

Set to a unique MID Server Name \(ServiceNow MID Server Centos 1\)

</td></tr><tr><td>

RUN\_AS\_USER

</td><td>

Set to non-root username \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

GROUP\_NAME

</td><td>

Optional: Add name of group directory to own MID Server folder

</td></tr><tr><td>

PROMPT\_BEFORE\_OWNERSHIP\_CHANGE

</td><td>

Set to true

</td></tr></tbody>
</table>9.  To configure your MID Server, navigate to the agent folder and configure the following properties in `config.xml` with a text editor:

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
</table>10. Start your MID Server by opening a command prompt, navigating to the agent folder, and running `start.bat`.

    If a service account was configured, enter the password when prompted. The MID Server then starts and connects to the instance.

    The MID Server appears in the record table once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `agent\logs` to identify the issue.

11. Set up your MID Server applications and capabilities by selecting the MID Server record and navigating to the related lists.

    By default, the MID Server is not be able to run any applications or capabilities.


### What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.

## Install MID Server on Linux with mutual authentication

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
    -   **I'm installing the MID Server on:** Linux
    -   **I want to install using a:** Linux \(RPM, DBM, or Docker\)
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

6.  To proceed, select **Next: Download and Install**.

7.  Create a ServiceNow user for this MID Server and grant it **mid\_server** role.

    For more information on creating users, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

    **Note:** This user should be unique for each MID Server using basic authentication.

8.  Download either the MID Server installer RPM file for RedHat/CentOS or the DEB file for Debian \(Ubuntu\) systems.

    For more information, see [Install a MID Server on Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md).

9.  Place the installer file on the MID Server host.

10. Install the package for the appropriate system with the following commands:

    1.  Install the RPM package for RedHat systems with the command: `sudo rpm -ivh --nodeps package_name.rpm.`

    2.  Install the DEB package for Debian systems with the following command: `sudo dpkg -i package_name.deb.`

11. To configure the MID Server service, run the command `./installer.sh` from the agent folder as a user with root privilege, and provide the required inputs.

12. Verify that the MID Server is running.

    The MID Server record appears in the installer step once it is detected. If the MID Server does not appear within 5 minutes of running the installation command, check your logs in `agent\logs` to identify the issue.


### What to do next

Consider selecting the clusters, applications, capabilities, and IP ranges for this MID Server. For more information, see [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md), [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_ConfigureCapabilities.md), [Using MID Server IP range auto-assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-servers-auto-assignment.md) respectively.

## Install MID Server on Linux with mutual authentication using ZIP

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
    -   **I'm installing the MID Server on:** Linux
    -   **I want to install using a:** Linux \(RPM, DBM, or Docker\)
    **Note:** If this is your first time installing a MID Server, use the command line installer instead of installing manually. See [Install MID Server with the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-ipki-install-command.md) for more information.

6.  To proceed, select **Next: Download and Install**.

7.  Create a ServiceNow user for this MID Server and grant it **mid\_server** role.

    For more information on creating users, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

    **Note:** This user should be unique for each MID Server using basic authentication.

8.  Download the Linux ZIP file from the installation plan.

9.  On the Linux host machine, extract the ZIP file into the intended install directory for the MID Server.

10. Configure a Non-Root User by creating a dedicated non-root account for the MID Server, then navigate to the `mid.shconf_override` and edit the following:

<table id="table_i3s_kmj_mjc"><tbody><tr><td>

**Parameter**

</td><td>

**Action**

</td></tr><tr><td>

APP\_NAME

</td><td>

Set to a unique MID Server Name \(mid\_centos\_1\)

</td></tr><tr><td>

APP\_LONG\_NAME

</td><td>

Set to a unique MID Server Name \(ServiceNow MID Server Centos 1\)

</td></tr><tr><td>

RUN\_AS\_USER

</td><td>

Set to non-root username \(DOMAIN\\svc\_mid\_uswest1\)

</td></tr><tr><td>

GROUP\_NAME

</td><td>

Optional: Add name of group directory to own MID Server folder

</td></tr><tr><td>

PROMPT\_BEFORE\_OWNERSHIP\_CHANGE

</td><td>

Set to true

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


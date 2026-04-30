---
title: Install a MID Server on Linux
description: Install MID Servers with the MID Server installer and verify it is active. The package includes an installer that automatically configures JRE to run in the environment. The MID Server can use an existing JRE rather than the provided JRE. Uninstall the MID Server to redeploy it.Silently installing the MID Server uses predefined parameters and requires no user input after it is initiated. You can use silent installation on several machines at once to quickly set up a network and to ensure all MID Servers have the same installation settings.Run MID Servers as non-root user on a Linux machine to improve security. Multiple MID Server can be installed as services so they can start by themselves after system reboots.You can choose to use an existing JRE for your MID Server rather than the OpenJDK provided with the MID Server installer. The MID Server runs as a stand-alone service. You can remove a stand-alone MID Server service to accommodate such tasks as redeploying the MID Server to another host machine or changing the unique name of a MID Server when deploying multiple MID Servers.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 13
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Install a MID Server on Linux

Install MID Servers with the MID Server installer and verify it is active. The package includes an installer that automatically configures JRE to run in the environment. The MID Server can use an existing JRE rather than the provided JRE. Uninstall the MID Server to redeploy it.

## Before you begin

Verify that the host computer satisfies the [MID Server system requirements](../reference/r_MIDServerSystemRequirements.md).

Role required: admin, mid\_server

<table id="table_yt1_bs4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>## About this task

To install Linux on MID Server, the RedHat/CentOS systems require RPM while Debian \(Ubuntu\) systems require DEB. The default installation location is `/opt/servicenow/mid`. Installing DEB in user defined directories is not supported.

To improve security, this procedure installs and run the MID Server service as a non-root user. Root privilege is required to deploy and configure a MID Server on a Linux server. A non-root user can manage a service only if they have the required permissions. For more details, see [PolicyKit issues with Linux MID Servers using non-admin accounts \[KB0815542\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0815542).

**Note:** ServiceNow no longer supports new installations of 32-bit MID Servers or upgrades to version Rome. New MID Server installation are blocked through RPM and MSI installer on the following operating systems:

-   CentOS 7
-   Windows server 2008
-   Windows server 2008 R2
-   Windows 8
-   Windows 10

MID Servers can be manually installed to any operating system with the ZIP file, however Windows 10 is unsupported. Unsupported MID Servers auto-upgrading to Rome create an issue record in MID Server Issues \(ecc\_agent\_issue\). For more information, see [Supported platform changes for MID Server \[KB0863694\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863694).

Java 11.0.17 is bundled with the MID Server installer package and is installed on the host for all new MID Servers. The installer automatically configures Java 11.0.17 to run in your environment. No additional configuration is required. This version supports both 64-bit Windows MID Servers and 64-bit Linux MID Servers. The MID Server requires a minimum JRE version 11.0.8, and recommended version 11.0.17. If you are using a lower version than 11.0.8, you may see encryption related issues.

**Note:** Linux MID Servers require glibC version 2.17. The library must be updated for JRE 11. On 64-bit Linux systems, you must install the 32-bit [GNU C library](http://www.gnu.org/software/libc/) \(glibc\). The installation command for CentOS is: `yum install glibc.i686`

Testing showed that the MID Server works as expected with Oracle Java 11 version 11.0.5. If you need to upgrade the JRE to a different version, then coordinate with the appropriate account representative for support.

## Procedure

1.  On the instance, navigate to **MID Server** &gt; **Downloads** and download either the MID Server installer RPM file for RedHat/CentOS or the DEB file for Debian \(Ubuntu\) systems.

    ![The Linux installer download page.](../image/linux-installer-download-page.png)

    **Note:** Use the copy link button to copy the download link and use the following `wget` command to directly download the installers in Linux machines.

    ```
    wget **&lt;copied link of the installer&gt;**
    ```

2.  Manually verify the authenticity and integrity of the downloaded file.

    1.  Download the signature ZIP files for RPM/DEB.

    2.  Run the following commands for either RPM or DEB.

        **RPM**

        -   Extract the public key, `ServiceNow_Digicert_DGST.pem`, and signature file from the downloaded signature zip file.
        -   Run the following command to verify the signature of the RPM file.

            ```
            openssl dgst -sha256 -verify <Extracted .pem file> -signature <Extracted bin file path> <RPM file path> 
            ```

        **DEB**

        -   Extract the public key, `ServiceNow_Digicert_Public.gpg`, from the downloaded signature zip files.
        -   Import the public key and verify the signature of the DEB file with the following commands.

            ```
            gpg --import <public key> 
            dpkg-sig --verify <DEB file path>
            ```

3.  Use the following commands to install either the RPM or DEB installer:

    **RPM**

    -   Install the RPM package for RedHat systems with the following command:

        ```
        sudo rpm -ivh --nodeps package_name.rpm.
        ```

    -   Install the RPM package for RedHat systems in a user defined location with the following command:

        ```
        sudo rpm -ivh --nodeps package_name.rmp --prefix=/path/to/user/directory.
        ```

    **DEB**

    Install the DEB package for Debian systems with the following command:

    ```
    sudo dpkg -i package_name.deb.
    ```

4.  To configure the MID Server service, run the following command from the agent folder as a user with root privilege and provide the required inputs.

    ```
    ./installer.sh
    ```

    ![The Linux command line with the installer.sh running.](../image/linux-installer-commandline.png)

5.  The **installer.sh** script takes the following inputs.

    -   **Instance URL**

        Enter the full URL of your instance, for example: `https://mycompanyinstace.service-now.com`

    -   **MID-Server Username**

        Enter the user name of [the MID Server user that you already created](t_SetupMIDServerRole.md#). The MID Server user must have the mid\_server role.

    -   **MID-Server Password**

        Set the password for the current MID Server user.

    -   **MID-Server Name**

        Set the name of the MID Server.

    Proxy Server Information \(optional\).

    -   **mid.proxy.use\_proxy**

        Enables the MID Server to use a web proxy to access the ServiceNow instance.

    -   **mid.proxy.host**

        Set this parameter to define the web proxy's host.

    -   **mid.proxy.port**

        Set this parameter to define the web proxy's port.

    -   **mid.proxy.username**

        If the web proxy requires a user name, set this parameter to define that username.

    -   **mid.proxy.password**

        If the web proxy requires a password, set this parameter to define that password.

    The MID Server can bypass proxy servers whose DNS/IP address is listed in the configuration parameter **mid.cloud.discovery.proxy.exclusion.list**. See [MID Server property](../reference/r_MIDServerProperties.md#) for more information.

    To run a MID Server as a daemon service, the following properties are also required.

    -   **app\_name**

        Set a unique name for the current MID Server

    -   **app\_long\_name**

        Set a unique long name for the MID Server.

    -   **run\_as\_user**

        Set the username to run the service as a non-root user.


## Result

Once all the inputs are entered, the MID Server automatically runs as a daemon service and starts the service.

## Linux MID Server silent installation

Silently installing the MID Server uses predefined parameters and requires no user input after it is initiated. You can use silent installation on several machines at once to quickly set up a network and to ensure all MID Servers have the same installation settings.

To perform a silent installation with the Linux installer, run the following command:

```
./installer.sh -silent -INSTANCE_URL https://instance_name.service-now.com -MUTUAL_AUTH N -MID_USERNAME username -MID_PASSWORD password -USE_PROXY N -MID_NAME mid -APP_NAME mid -APP_LONG_NAME ServiceNow_MID_Server_Mid -NON_ROOT_USER nonrootuser 
```

The following fields can be passed through the command line:

-   **INSTANCE\_URL**

    Enter the URL of your instance, for example: `https://mycompanyinstance.service-now.com`

-   **MUTUAL\_AUTH**

    Set this value to Y to use mutual authentication instead of basic authentication. Otherwise, set it to N.

    **Note:** If **MUTUAL\_AUTH** = Y then provide the path to the certificate with **CERTIFICATE\_PATH**.

-   **CERTIFICATE\_PATH**

    If mutual authentication is enabled, provide the path to the certificate.

-   **MID\_USERNAME**

    Enter the user name of [the MID Server user that you already created](t_SetupMIDServerRole.md#). The MID Server user must have the mid\_server role.

-   **MID\_PASSWORD**

    Enter the password for the user.

-   **USE\_PROXY**

    Set this value to Y if your MID Server communicates through a proxy to connect to the instance.

    **Note:** If **USE\_PROXY** = N then skip the other proxy details.

-   **PROXY\_HOST**

    Enter the proxy server host name or IP address. Do not include the protocol in the host name. For example: `proxyserver.domain.com` is correct, but `https://proxyserver.domain.com` is incorrect.

-   **PROXY\_PORT**

    Enter the port the proxy server uses to communicate. If this value is blank, the installer uses the proxy server's default port number.

-   **PROXY\_USERNAME**

    Enter the username that has administrator rights to the proxy server.

-   **PROXY\_PASSWORD**

    Enter the password for the username.

-   **MID\_NAME**

    Enter the MID Server name.

-   **APP\_NAME**

    Provide the service name. It must be unique for the current MID Server.

-   **APP\_LONG\_NAME**

    Provide the service long name.

-   **NON\_ROOT\_USER**

    Provide the username to run the service as a non-root user.


The following is an example command for a MID Server which uses a proxy and mutual authentication:

```
./installer.sh -silent -INSTANCE_URL https://instance_name.service-now.com MUTUAL_AUTH Y –CERTIFICATE_PATH <path-to-certificate> -USE_PROXY Y -PROXY_HOST <ip> -PROXY_PORT <port> -PROXY_USERNAME <username> -PROXY_PASSWORD <password> -MID_NAME proxymid -APP_NAME proxymid -APP_LONG_NAME servicenow_proxy_mid -NON_ROOT_USER nonrootuser 
```

**Note:** To reconfigure the MID Server, run the `installer.sh` command again. Reconfiguring the MID Server deletes the old configuration. ![The Linux command line after using the silent installation command.](../image/linux-silent-install.png)

## Run Linux MID Servers as non-root users

Run MID Servers as non-root user on a Linux machine to improve security. Multiple MID Server can be installed as services so they can start by themselves after system reboots.

### Before you begin

Role required: root

This process is only applicable if you installed the MID Server manually using the ZIP file. If you installed the MID Server with the procedure in [Install a MID Server on Linux](t_InstallAMIDServerOnLinux.md#), then the MID Server is already running as a non-root user.

Supported versions for this procedure are Linux Red Hat 6 or newer, Ubuntu 1404 or newer, and CentOS 6 or newer.

### Procedure

1.  Stop any MID Server running on the host with the command **bin/mid.sh stop**.

2.  Remove any MID Servers on the host with the command **bin/mid.sh remove**.

3.  Edit the file `mid.shconf_override`.

    ![The content in mid.shconf_override.](../image/linux-mid.shconf_override.png)

4.  Add the MID Server's name using the lines **APP\_NAME=** and **APP\_LONG\_NAME=** to run it as a service.

    To prevent errors, the **APP\_NAME** of each MID Server must be unique.

5.  To run multiple MID Servers as services on the same host, add an **APP\_NAME** and **APP\_LONG\_NAME** for each instance.

    ![Multiple MID Servers being named as non-roots.](../image/Linux-multiple-non-admin-mid.png)

6.  Add the name of the non-root user to operate the account using the line **RUN\_AS\_USER=**.

7.  Add the name of the group to own the entire agent directory using the line **GROUP\_NAME=**.

8.  Set the line **PROMPT\_BEFORE\_OWNERSHIP\_CHANGE=** to **true** to prompt the user for confirmation before any changes to file permissions are applied.

    The file permission change is applied to the entire agent folder and everything inside recursively. The changes include blocking other users' the access to the entire agent folder, changing the owner to **$RUN\_AS\_USER** if specified, and changing the group to **$GROUP\_NAME** if specified.

9.  Reinstall the MID Server with the command **bin/mid.sh install**.

    **Note:**

    To prevent errors, make sure to stop and remove any existing MID Server services before starting new ones. During the first installation, a root user is required to call **bin/mid.sh install**. Reinstalling the MID Server applies the changes in `mid.shconf_override`. Then the non-root user specified in `mid.shconf_override` is able to start/stop/restart the service without elevated privileges.


### What to do next

For more information about managing the allow list and file permission enforcement, see [File permission enforcement for Windows MID Servers](../concept/mid-non-admin-permission.md). Running a Linux MID Server with a non-root account may result in issues with PolicyKit in some systems. See [PolicyKit issues with Linux MID Servers using non-root accounts](https://support.servicenow.com/kb_view.do?sysparm_article=KB0815542) for more information.

## Configure a Linux MID Server to use an existing JRE

You can choose to use an existing JRE for your MID Server rather than the OpenJDK provided with the MID Server installer.

### Before you begin

Ensure that your JRE version is supported. See [MID Server system requirements](../reference/r_MIDServerSystemRequirements.md) for details.

Role required: admin

### About this task

By electing to use your own JRE, you are responsible for upgrading it as necessary. For a detailed procedure and cautions regarding changing the JRE, see [KB0778272](https://support.servicenow.com/kb_view.do?sysparm_article=KB0778272).

### Procedure

1.  Navigate to this file in the MID Server installation directory:

    `agent/conf/wrapper-override.conf`

2.  To specify the existing Java executable that you want to use, add this line to the file:

    `wrapper.java.command={your\_java\_executable}`

    For more information, see the Java service wrapper property [documentation](https://wrapper.tanukisoftware.com/doc/english/prop-java-command.html).

3.  Save the file.


## Uninstall a Linux MID Server

The MID Server runs as a stand-alone service. You can remove a stand-alone MID Server service to accommodate such tasks as redeploying the MID Server to another host machine or changing the unique name of a MID Server when deploying multiple MID Servers.

### Before you begin

Role required: admin

### Procedure

1.  Run the **uninstall.sh** script in the agent folder to remove the service and uninstall the RPM/DEB.

    ![The Linux command line after running the uninstall.sh script.](../image/linux-uninstall-commandline.png)


### Result

The MID Server service is uninstalled.

### What to do next

[Validate](t_ValidateAMIDServer.md) the MID Server to prepare it for use.


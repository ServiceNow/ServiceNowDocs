---
title: Install a MID Server on Windows
description: Install MID Servers with the MID Server guided Windows installation package. The package includes an installer that automatically configures OpenJDK to run in the environment. The MID Server can use an existing JRE rather than the provided OpenJDK. Uninstall the MID Server to redeploy it.Install MID Servers with the MID Server guided Windows installation package. The package includes an installer that automatically configures OpenJDK to run in the environment.The MID Server guided native Windows installer also supports guided uninstallation of the MID Server.MID Server service credentials are required to manage the MID Server service on the host machine, including its ability to successfully auto-upgrade.Silently installing the MID Server uses predefined parameters and requires no user input after it is initiated. You can use silent installation on several machines at once to quickly set up a network and to ensure all MID Servers have the same installation settings.Install MID Servers with the ZIP file installation package and verify it is active.The MID Server runs as a stand-alone service. You can remove a stand-alone MID Server service to accommodate such tasks as redeploying the MID Server to another host machine or changing the unique name of a MID Server when deploying multiple MID Servers.You can choose to use an existing JRE for your MID Server rather than the OpenJDK provided with the MID Server installer.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 21
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Install a MID Server on Windows

Install MID Servers with the MID Server guided Windows installation package. The package includes an installer that automatically configures OpenJDK to run in the environment. The MID Server can use an existing JRE rather than the provided OpenJDK. Uninstall the MID Server to redeploy it.

<table id="table_jvn_ds4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>-   Verify that the host computer satisfies the [MID Server system requirements](../reference/r_MIDServerSystemRequirements.md).
-   The MID Server requires the minimum PowerShell version 3.0 and supports versions up to PowerShell 5.1.
-   Ensure that the Microsoft Application Experience Lookup Service is enabled on the MID Server host. If this service is disabled, the MID Server auto-upgrade might fail, causing the MID Server to go down. For information on managing issues with the Application Experience service, see [KB0597552](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0597552).

Java 21.0.7 is bundled with the MID Server installer package and is installed on the host for all new MID Servers. The installer automatically configures Java 21.0.7 to run in your environment. No additional configuration is required. This version supports both 64-bit Windows MID Servers and 64-bit Linux MID Servers. The MID Server requires a minimum JRE version 17.0.10, and recommended version 21.0.7. If you are using a lower version than 17.0.10, you may see encryption related issues.

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

## Install a MID Server on Windows with guided installation

Install MID Servers with the MID Server guided Windows installation package. The package includes an installer that automatically configures OpenJDK to run in the environment.

### Before you begin

Role required: admin or mid\_server

### About this task

The MID Server guided native Windows installer will configure the MID Server with provided settings. The installer creates the MID Server Service and assigns it to the provided user. The installer sets the file permissions on the MID Server Install folder. The installer allows for the configuration of proxy settings. Optionally, the installer can start the MID Server automatically.

### Procedure

1.  On the instance, download the MID Server installation .msi file from **MID Server** &gt; **Download**.

2.  Log in to the Windows host machine where you want to install the MID Server.

3.  Place the installer .msi on the desired MID Server host.

4.  Open the installer with Administrator level privileges.

5.  Use the installer to enter the following information.

    ![An example MID Server installation.](../image/mid-installer.png)

<table id="table_ohg_3xm_wcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authentication Type

</td><td>

-   **Basic**

Username and password based authentication.

-   **Mutual**

Client certificate based authentication. See [MID Server unified key store](mid-unified-keystore.md#) for more information on mutual authentication.

 **Note:** Selecting mutual authentication disables the MID Server username and password fields. The disabled fields are not written to **config.xml**.

</td></tr><tr><td>

ServiceNow instance URL

</td><td>

Enter the full URL of your instance, for example: `https://mycompanyinstace.service-now.com`

</td></tr><tr><td>

ServiceNow MID Server username

</td><td>

Enter the name of the [MID Server user](../task/t_SetupMIDServerRole.md#) that you already created. The MID Server user must have the mid\_server role.

</td></tr><tr><td>

ServiceNow MID Server password

</td><td>

Enter the password for the user in the **ServiceNow MID Server username**.

</td></tr><tr><td>

Certificate Revocation

</td><td>

This check box is selected by default to enable certificate revocation policies to improve security. For more information on certificate revocation, see [MID Server certificate check policies](mid-security-checks.md).

 When testing a connection with certificate revocation enabled, the installer checks if OCSP port 80 is open and the entrust page is accessible.

 If the connection test fails due to the certificate revocation check, the error must either be corrected and re-tested or the certificate revocation check must be disabled. The certificate revocation check is not required for successful installation.

</td></tr><tr><td>

Use proxy

</td><td>

Select this check box if your MID Server communicates through a proxy to connect to the instance.**Note:** Your proxy server must use Basic Authentication for the MID server to connect to the instance.

The MID Server can bypass proxy servers whose DNS/IP address is listed in the configuration parameter **mid.cloud.discovery.proxy.exclusion.list**. See [MID Server property](../reference/r_MIDServerProperties.md#) for more information.

</td></tr><tr><td>

Proxy host

</td><td>

Enter the proxy server host name or IP address. Do not include the protocol in the host name. For example, enter `proxyserver.domain.com`, not `https://proxyserver.domain.com`.

</td></tr><tr><td>

Proxy port

</td><td>

Enter the port through which the proxy server communicates. If you leave this field blank, it should use the proxy server's default port number.

</td></tr><tr><td>

Proxy username

</td><td>

Enter the user name that has administrator rights to the proxy server.

</td></tr><tr><td>

Proxy password

</td><td>

Enter the password for the user name.

</td></tr></tbody>
</table>6.  Click **Test your connection** to validate the credentials and instance information.

    If you encounter any errors, verify the information that you input.

7.  Click **Next**.

8.  Configure the MID Server name and Service Account parameters \(see table\).

    ![MID parameters.](../image/mid-server-name-gui.png)

<table id="table_epz_ngn_wcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID Server name

</td><td>

Enter a MID Server name.**Warning:** MID Server names cannot begin with **mid.server**.

</td></tr><tr><td>

Service Account Name

</td><td>

Username of the service account that will be used to run the MID Server service. For information on creating service accounts, see [Create a Windows service account with "Log on as Service" \[KB0867669\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867669).

 Service Account Name field is an editable drop-down menu. Either select a value from the drop-down or type a new value in the text field. Only the accounts with **log on as service** policy are displayed in the drop-down. Group Managed Service Accounts \(gMSA\) that inherit the **log on as service** policy from their groups are not displayed in the drop-down. However, you can install the MID Server service using those accounts by manually entering the service account name in the editable drop-down. The name can follow three formats.

 1.  If the service account is local to the computer, you can give just the name.

Example: My\_Local\_Service\_Account

2.  If the service account is local to the computer, you can provide “.” as the domain name for the account.

Example: .\\My\_Local\_Service\_Account

3.  Any account can follow the format \{domain\}\\\{username\}.

Example: MY-COMPUTER-DOMAIN\\My\_Domain\_Service\_Account

 Add a new local service account by selecting the **+** button. This button opens the **Configure New Local User** window, which has three fields.

-   **Service Account Name:** Enter the name of the new service account.
-   **Service Account Password:** Enter the password of the new service account.
-   **Re-enter Password:** Confirm the password of the new service account.
 When a group Managed Service Account \(gMSA\) user is selected, the password field is removed because passwords for gMSA users are managed by the Active Directory.

 **Note:**

The provided service account credentials must meet the following requirements in addition to being a valid account.

-   The user cannot be a local system or an administrator level account \(local admin, domain admin, etc.\)
-   The service account provided has the **log on as service** right, which is required for an account to be used as the **log on user** for a service.


</td></tr><tr><td>

Service Account Password

</td><td>

Password of the service account that will be used to run the MID Server service.

</td></tr><tr><td>

Set Service Name Manually

</td><td>

Select this check box if you want to manual set the service name and display name for your MID Server.

 Note: Your proxy server must use Basic Authentication for the MID server to connect to the instance.

</td></tr><tr><td>

MID Service wrapper name

</td><td>

Modify this field if necessary. It is populated automatically by prefixing `snc_mid_` to the MID Server name. In most cases, you do not need to modify this.

</td></tr><tr><td>

MID Server wrapper display name

</td><td>

Modify this field if necessary. It is populated automatically by prefixing `ServiceNow MID Server_` to the MID Server name. In most cases, you do not need to modify this.

</td></tr></tbody>
</table>9.  Click **Next** and select a destination folder for the installation.

    Users can manually enter an existing, valid file path, or use the “Change” button to open up a browsing page where they can choose the install location.

10. Click **Next** to view the summary.

    ![Starting the MID Server.](../image/MIDServerInstallerStartMIDServer.png)

    Select **Start MID Server after installation** if you want to start the MID Server immediately after installation. If you wish to make additional configuration changes, before starting the MID server, leave this box unchecked. If mutual authentication was selected, the MID Server username and password fields are removed.

    **Note:** If the MID Server fails to start, the cause might be a duplicate name or multiple services that point to the same executable path. This can happen when you have MID servers previously not installed through the installer. See [MID Server fails to start](../reference/mid-startup-fails.md) for details.

11. Click **Mid Servers List Page**.

    The installer opens the MID Server list from your instance.

12. Select the MID Server name from the list.

    **Note:** It may take a few seconds for the MID Server time to establish a connection with your instance.

    The system displays the MID Server record.

13. From **Related Links**, click **Validate**.

    The MID Server **Validated** changes to **Yes**.


### What to do next

To upgrade the MID Server, see [MID Server upgrades](c_UpgradeAndTestMIDServer.md) for procedures and requirements.

## Uninstall a Windows MID Server with the guided installer

The MID Server guided native Windows installer also supports guided uninstallation of the MID Server.

### Before you begin

Role required: admin

There are three ways to uninstall a MID Server after installing it with the guided native Windows installer.

### Procedure

1.  On the MID Server host, navigate to the **Control Panel** &gt; **Programs** &gt; **Programs and Features** &gt; **Uninstall a program**.

    1.  Uninstall the program with the MID Server's name.

2.  Alternatively, navigate to **Settings** &gt; **Apps**

    1.  Uninstall the program with the MID Server's name.

3.  The MID Server can also be uninstalled with the silent uninstall script.

    This is useful for uninstalling multiple MID Servers. For more information, see [Windows MID Server silent installation and uninstallation](mid-server-install-prereqs.md#)


## Configure Windows MID Server service credentials

MID Server service credentials are required to manage the MID Server service on the host machine, including its ability to successfully auto-upgrade.

### Before you begin

Role required: admin

### About this task

If you installed the MID Server using the native installer, you will not need to complete this procedure. However, to change the service user after the installation for any reason, use this procedure.

Windows service credentials control the level of privilege on the device. The user should not be a local system or an administrator level account \(local admin, domain admin, etc.\) The service account provided should have the **log on as service** right, which is a requirement for an account to be used as the **log on user** for a service.

**Note:**

Windows service credentials are not the same as the MID Server user credentials, which allow communication between the MID Server and the instance. You must configure both of these credentials separately. See [Create the MID Server user and grant the role](../task/t_SetupMIDServerRole.md#) for instructions on MID Server user credentials.

### Procedure

1.  Open the Windows Services console.

2.  Double-click the `ServiceNow` `<MID Server name>` service for each MID Server.

3.  Select the **Log On** tab.

4.  Choose a non-admin user and provide the password for that user.

5.  In the **General** tab, set the **Startup type**.

    The field is set to **Automatic** by default.

6.  Click **OK**.

7.  Restart the ServiceNow &lt;MID Server name&gt; service, and make sure that ServiceNow\\&lt;MID Server name&gt;\\agent\\logs\\agent0.log does not have error messages.

    If the MID Server does not start, see the ServiceNow knowledge article Review the agent log for MID Server errors \(article [KB0535148](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0535148)\).

8.  On the instance to which this MID Server is connected, navigate to **MID Server** &gt; **Servers**.

    If Discovery is installed, alternately navigate to **Discovery** &gt; **MID Servers**. All MID Servers connected to this instance are listed.

9.  Make sure that the Status of the MID Server that you just installed is **Up**.


## Windows MID Server silent installation and uninstallation

Silently installing the MID Server uses predefined parameters and requires no user input after it is initiated. You can use silent installation on several machines at once to quickly set up a network and to ensure all MID Servers have the same installation settings.

### MID Server silent installation

**Note:** All silent install/uninstall commands must be run with administrator level privileges.

To silently install the MID Server on a Windows system, download the script attached to the Knowledge Base article [Windows MID Server silent installation and uninstallation](https://support.servicenow.com/kb_view.do?sysparm_article=KB0854442). Place the file on the target MID Server host machine and run the following command from the command prompt. You can also run the script directly from powershell.

```
powershell -command “.\SilentInstall.ps1 -<parameter_name1> ‘<value for parameter1>’ -<parameter_name2> ‘<value for parameter2>’ etc…”
```

The script checks the following mandatory parameters:

-   **MSI\_FILE\_NAME**: the name of the MSI file used for the installation.
-   **INSTALL\_LOCATION**: the location to install the MID Server.
-   **INSTANCE\_URL**: the target ServiceNow instance the MID Server will connect to.
-   **MID\_USERNAME**: the instance account name.
-   **MID\_PASSWORD**: the instance account password.
-   **MID\_NAME**: the name of the MID Server.
-   **SERVICE\_ACCOUNT\_NAME**: the name of the service account.
-   **SERVICE\_ACCOUNT\_PASSWORD**: the password of the service account.

The following parameters are optional:

-   **LOG\_NAME**: enables logging and puts logs into the file named by this parameter.
-   **START\_MID**: sets the MID Server to start automatically after the installation finishes.
-   **USE\_PROXY**: enables the use of a proxy. If you choose this command, the following parameters become mandatory.
    -   **PROXY\_HOST**: the name of the proxy host.
    -   **PROXY\_PORT**: the port number of the proxy.
    -   **PROXY\_USERNAME**: the proxy username. If there is no username, input **‘’**.
    -   **PROXY\_PASSWORD**: the proxy password. If there is no password, input **‘’**.
-   **MANUAL\_SERVICE\_NAME**: the service name. If you choose this command, the following parameters become mandatory:
    -   **SERVICE\_NAME**: the service name.
    -   **SERVICE\_DISPLAY\_NAME**: the service display name.
-   **MUTUAL\_AUTH**: enables mutual authentication. If this switch is enabled, **MID\_USERNAME** and **MID\_PASSWORD** are not required. See [MID Server unified key store](mid-unified-keystore.md#) for more information.

**Note:** The parameters **START\_MID**, **USE\_PROXY**, **MUTUAL\_AUTH**, and **MANUAL\_SERVICE\_NAME** are switches. They use the format **-&lt;switch\_param\_name&gt;** and are not followed by a value.

After the script runs, verify the MID Server files, service, and entry in Programs and Features are installed. If you enabled logging, verify the log info in the file specified by the **LOG\_NAME** parameter.

An example MID Server silent installation command:

```
powershell -command ".\SilentInstall.ps1 -MSI_FILE_NAME 'MID-Installer.msi' -INSTALL_LOCATION 'C:\Users\Administrator' -INSTANCE_URL 'https://my-instance-name.service-now.com' -MID_USERNAME 'mid_server' -MID_PASSWORD 'mid_password' -MID_NAME 'Silent_Install_MID' -SERVICE_ACCOUNT_NAME 'DOMAIN\My_Service_Account' -SERVICE_ACCOUNT_PASSWORD 'Service_Account_Password' -LOG_NAME 'Silent_Install_Log.txt'"
```

An example command using the **START\_MID** switch:

```
powershell -command ".\SilentInstall.ps1 -MSI_FILE_NAME 'MID-Installer-Wix.msi' -INSTALL_LOCATION 'C:\Users\Administrator' -INSTANCE_URL 'https://my-instance-name.service-now.com' -MID_USERNAME 'DOMAIN\My_Service_Account' -MID_PASSWORD 'mid_password' -MID_NAME 'Silent_Install_MID' -SERVICE_ACCOUNT_NAME 'DOMAIN\My_Service_Account’ -SERVICE_ACCOUNT_PASSWORD 'Service_Account_Password' -LOG_NAME 'Silent_Install_Log.txt' -START_MID"
```

### MID Server silent uninstallation

To silently uninstall the MID Server on a Windows system, download the script attached to the Knowledge Base article [Windows MID Server silent installation and uninstallation](https://support.servicenow.com/kb_view.do?sysparm_article=KB0854442). Then run the script using the command prompt. It can also be run directly from powershell.

```
powershell -command “.\SilentUninstall.ps1 -MID_NAME ‘<value for MID_NAME>’ -LOG_NAME ‘<value for LOG_NAME>’”
```

The script requires the mandatory parameter **MID\_NAME**, which is the name of the MID Server you want to uninstall.

The optional parameter **LOG\_NAME** enables logging of the uninstallation and puts logs into the file named by this parameter.

After the script runs, verify the MID Server files, service, and entry in Programs and Features are uninstalled. If you enabled logging, verify the log info in the file specified by the **LOG\_NAME** parameter.

An example MID Server silent uninstall command:

```
powershell -command ".\SilentUninstall.ps1 -MID_NAME 'silent_install_cmd' -LOG_NAME
      'uninstall.txt'"
```

## Manually install a MID Server on Windows

Install MID Servers with the ZIP file installation package and verify it is active.

### Before you begin

Role required: admin or mid\_server

### About this task

Click this link to view the installation video:Installing the MID Server on Linux

MID Servers can be configured to run using non-administrative accounts. Using non-admin accounts in conjunction with file permission enforcement can improve security by restricting access to MID Server files. sIf you choose to run a MID Server with a non-admin account, there are limitations that change the behavior of other applications. The following behavior changes can occur:

-   The MID Server account needs appropriate credentials to run a Discovery schedule. If the credentials are insufficient, the MID Server falls back to the user account's privileges. A non-admin user account may not have the necessary privileges to access the Discovery target.
-   Enhanced Application Dependency Mapping \(ADME\) and File Based Discovery \(FBD\) may not work by default. To correct this issue, non-admin users need to be given permission to read/write to the Admin Share folder.

### Procedure

1.  Log in to the Windows host machine where you want to install the MID Server.

2.  Create a folder for the MID Server on the top level of the drive such as `ServiceNow\MID Server1`.

3.  Download the MID archive file into the new folder.

4.  Right-click the archive and select **Extract All**.

5.  Navigate to the `service-now\<mid server name>\agent` folder that was created when the file was extracted.

6.  To configure the MID Server manually, edit the `config.xml` file with a text editor such as WordPad:

    1.  Find the element **&lt;parameter name="url" value="https://YOUR\_INSTANCE.service-now.com" /&gt;** element and change the value to the URL of your instance.

    2.  Enter the MID user credentials in the `mid.instance.username` and `mid.instance.password` parameters.

        By default, the MID Server, uses basic authentication for SOAP messages. The password value is also encrypted authentication.

    3.  Find the **&lt;parameter name="name" value="YOUR\_MIDSERVER\_NAME\_GOES\_HERE" /&gt;** element and change the value for the MID Server name.

    4.  Enter connection information for the proxy server.

        Remove the appropriate comment tags from the proxy configuration information.

        For example, you can configure these parameters:

        -   **mid.proxy.use\_proxy**
        -   **mid.proxy.host**
        -   **mid.proxy.port**
        -   **mid.proxy.username**
        -   **mid.proxy.password**
7.  If you want to install the MID Server as a non-admin user, follow these steps.

    1.  Edit the `.\conf\wrapper-override.conf` file.

    2.  Uncomment the `wrapper.ntservice.account` property and specify the Service Account Name.

    3.  Either uncomment `wrapper.ntservice.password.prompt`, or uncomment `wrapper.ntservice.password` and provide a password.

        Enabling `wrapper.ntservice.password.prompt` prompts for a password when installing the service. Enabling `wrapper.ntservice.password` sets a password immediately but is less secure.

    4.  Uncomment the `wrapper.ntservice.permissions.1.account` and specify the Service Account Name.

    5.  Uncomment `wrapper.ntservice.permissions.1.allow` but do not edit it.

    6.  Uncomment `wrapper.name` and specify the desired service name, and uncomment `wrapper.displayname` and specify the desired display name.

        The `wrapper.name` must be unique on the host and no other service can share the same name.

8.  Run `start.bat` to start the MID Server.

    If `wrapper.ntservice.password.prompt` was set in step 7c, enter the password when prompted. If there is no password, proceed without entering one.

9.  On the instance, in the **Related Links**, select **Validate**.

    The MID Server **Validated** changes to **Yes**.


## Uninstall a Windows MID Server after manual installation

The MID Server runs as a stand-alone service. You can remove a stand-alone MID Server service to accommodate such tasks as redeploying the MID Server to another host machine or changing the unique name of a MID Server when deploying multiple MID Servers.

### Before you begin

Role required: admin

This procedure is only for users who install the MID Server using the ZIP file.

### Procedure

1.  Stop the running MID Server service, using either of these procedures:

    -   **Windows command line**: From the MID Server home \(`agent`\) directory, run `stop.bat`.
    -   **Windows Services console**: From the Windows Services console, right-click the **ServiceNow** *MID Server name* and then select **stop**.
2.  From a command prompt, go to the `\agent\bin` directory in the MID Server installation directory and double-click the `UninstallMID-NT.bat` file.


### What to do next

[Validate](../task/t_ValidateAMIDServer.md) the MID Server to prepare it for use.

## Configure a MID Server on Windows to use an existing JRE

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



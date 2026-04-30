---
title: Install and uninstall Nmap on a MID Server
description: If you decide to use credential-less Discovery in your network, you must install Nmap on each Windows MID Server that you want to use for this purpose. Self-hosted customers whose network security does not permit downloads from install.service-now.com must use a specific manual process to install and configure Nmap.Use this procedure to install Nmap on MID Server host machines in a self-hosted environment that does not allow network access to the ServiceNow install.service-now.com download site.Use this procedure to uninstall Nmap in a self-hosted environment that does not allow network access to the ServiceNow install.service-now.com download site.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Install and uninstall Nmap on a MID Server

If you decide to use credential-less Discovery in your network, you must install Nmap on each Windows MID Server that you want to use for this purpose. Self-hosted customers whose network security does not permit downloads from `install.service-now.com` must use a specific manual process to install and configure Nmap.

## Before you begin

Role required: agent\_admin

<table id="table_tqp_ws4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>-   Assign MID Server IP ranges to all deployed MID Servers. The quickest and most reliable way to do this is with the [Using MID Server IP range auto-assignment](../concept/mid-servers-auto-assignment.md#) feature available in the [Discovery Quick Start](https://www.servicenow.com/docs/access?context=discovery-quick-start&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) wizard. This method ensures that the set of MID Servers configured to access an IP address range is comprehensive.
-   Identify the IP ranges you want to explore with credential-less Discovery. Ensure that these ranges can only be accessed by MID Servers with Nmap installed, running on supported Windows hosts.
-   Use the **All** option for selecting IP ranges and observe these requirements:
    -   Restrict the use of this feature to Windows MID Servers only.
    -   Ensure that Nmap is installed on each of these MID Servers.
    -   Ensure that the MID Servers can access the entire customer network.
-   When you create a Discovery schedule with Nmap enabled, observe these requirements for the MID Server selection options:
    -   **Specific MID Cluster**: Verify that Nmap is installed on all MID Servers in the cluster, where each MID Server in the cluster is configured to access the same set of IP ranges.
    -   **Auto-Select Mid Server**: When running horizontal Discovery, verify that Nmap is installed on at least one of the MID Servers that can access the Discovery schedule’s configured MID Server IP ranges.
    -   **Specific MID Server**: Verify that Nmap is installed on each MID Server that can access the schedule’s configured MID Server IP Ranges.

        **Note:** To use credential-less Discovery for Service Mapping, install Nmap on all MID Servers that can access the Discovery schedule’s configured MID Server IP ranges.


Role required: agent\_admin

## About this task

The Discovery - IP Based \[com.snc.discovery.ip\_based\] plugin provides connection to the installer for Nmap and the programming elements that allow a Windows MID Server to run approved scripts on target CIs for credential-less Discovery. MID Servers on which Nmap is installed can execute an Nmap command configured to perform reverse DNS name resolution, discover MAC addresses, or gather OS information on target CIs without using credentials. The Discovery - IP Based plugin is activated automatically when the Discovery \[com.snc.discovery\] or Event Management and Service Mapping Core \[com.snc.service-watch\] plugins are activated.

-   **Service Mapping and Nmap**

    Service Mapping does not check for the presence of the **Nmap** capability and selects the MID Server based on the IP address only. To ensure that Service Mapping does not select a MID Server without the **Nmap** capability, install Nmap on all MID Servers assigned to the IP address ranges for which you want credential-less Discovery to be available. If Service Mapping selects a MID Server for credential-less Discovery that does not have Nmap capabilities, this error message appears in the map at the site of the CI being discovered: `Nmap is not installed on MID Server. Verify all MIDs configured to handle selected IP Address have Nmap Capability. Nmap root directory path does not exist: <path>`

-   **Amazon Web Service AWS**

    Running Nmap scans to or from any resource within the Amazon Web Service AWS environment is tightly regulated and requires the permission of AWS through the [AWS Vulnerability/Penetration Testing Request](https://aws.amazon.com/security/penetration-testing/) form. AWS only permits testing of EC2 and RDS instances that you own. Tests against any other AWS services or AWS-owned resources are prohibited. In addition, any Nmap scan of a permitted instance must be performed within an approved time window. For these reasons, credential-less Discovery within an AWS environment is not appropriate, and if a violation of their policy occurs, could result in expulsion from the service.

-   **Supported operating systems**

    Nmap is supported on all editions of these operating systems, including virtual machines and 64 bit systems:

    -   Windows 2012
    -   Windows 2016
-   **MID Server requirements**

    Nmap can be installed on MID Servers that meet these requirements:

    -   Status is **Up**.
    -   MID Server is validated.
    -   MID Server does not already have the **Nmap** [capability](../reference/r_MIDServerCapabilities.md).
    -   MID Server must be logged in as a local admin if Nmap is not already installed. Administrative privleges are only necessary for the installation process. Once Nmap is installed, non-admin users can use and run credential-less discovery.

        **Note:** If there are multiple MID Servers installed on the same host machine and one of them has already installed Nmap using an admin user, the other MID Servers can enable credential-less discovery using a non-admin user.

    **Warning:** The MID Server installation path must not contain the following characters:

    -   **\( \)**
    -   **\{ \}**
    -   **\[ \]**
    The Nmap installer replaces these characters with spaces. This prevents the installer from finding the correct path, and the installation fails. An example of a path that will fail is `C:\MIDServers\MID(1)\agent`.


## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Open the desired MID Server record.

3.  Under **Related Links**, select **Enable Credential-less Discovery**.

    A confirmation dialog box appears.

    ![Confirmation dialog box](../image/EnableCredential-lessDiscovery.png)

4.  Click **Yes** to continue with the installation.

    The instance runs the Nmap installer from `https://install.service-now.com`, a site within a ServiceNow datacenter that contains installers for the platform. This progress notice appears during installation:

    ![Nmap installer progress notice](../image/NmapInstallationProgress.png)

    The **Logs** tab in the MID Server record shows the message: `Running system command: installNmap`.

5.  Click **OK** if you want to hide the dialog box while the installer continues to run in the background.

    Installing Nmap also installs Npcap on the host, if it is not already installed. Npcap is Nmap's packet capture library for Windows that allows Nmap to perform port scans quickly and to identify the family of the operating system running on the target. Npcap is installed once on the host and can be used by any other application that requires it, such as Wireshark.

    **Note:** If a more recent version of Npcap is already installed on the Windows MID Server host, Nmap is installed without Npcap. If an older version of Npcap is installed on the host, the Nmap installer upgrades it to the newer version.

    The installation process has either of these outcomes:

    -   **Success**: These conditions indicate a successful installation:
        -   The version of Nmap that is installed appears in the **Nmap version** field in the MID Server record
        -   The **Related Link** changes to **Disable Credential-less Discovery**.
        -   The **Nmap** capability is assigned to the MID Server and appears in the **Capabilities** tab of the MID Server record.
    -   **Failure**: If the installation fails, an error message is logged to the [MID Server Issue \[ecc\_agent\_issue\]](../concept/mid-server-active-issues.md) table. If you run the installer again with success, the issue is marked as **Resolved**.
6.  To uninstall Nmap for a selected MID Server, select **Disable Credential-less Discovery** under **Related Links** in the MID Server record.

    This dialog appears during the uninstallation process:

    ![Credential-less Discovery uninstallation notice](../image/DisableCredential-lessDiscovery.png)

    The **Logs** tab in the MID Server record shows the message: `Running system command: uninstallNmap`.

    **Important:** Because Npcap can be used by other applications, uninstalling Nmap does not automatically uninstall Npcap. You must uninstall Npcap manually, after determining that no other dependencies exist.


**Parent Topic:**[Configuring MID Servers](../concept/c_MIDServerConfiguration.md)

**Related topics**  


[Credential-less Discovery](https://www.servicenow.com/docs/access?context=nmap-credential-less-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)

## Install Nmap on a self-hosted system

Use this procedure to install Nmap on MID Server host machines in a self-hosted environment that does not allow network access to the ServiceNow® `install.service-now.com` download site.

### Before you begin

Role required: admin, maint

### About this task

You must install Nmap manually on each MID Server host and then configure the instance to execute credential-less Discovery.

**Note:** This procedure does not apply to self-hosted customers whose MID Server hosts can access `install.service-now.com` from within their network.

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties** \(MID Server Property \[ecc\_agent\_property\] table\) and open the record for the **mid.nmap.version** property.

    This property contains the version of Nmap that you must install. Record the version number.

2.  Download the correct installer executable from one of these URLs:

    -   [https://nmap.org/dist/](https://nmap.org/dist/): If the Nmap version in the property is 7.94, the executable you need is `https://nmap.org/dist/nmap-7.94-setup.exe`.
    -   `https://install.service-now.com/glide/distribution/builds/package/thirdparty/nmap/nmap-setup-xxx-windows.exe`. If the Nmap version in the property is 7.94, the executable you need is `https://install.service-now.com/glide/distribution/builds/package/thirdparty/nmap/nmap-setup-7.94-windows.exe`
3.  Create a folder called `nmap` in the MID Server `agent` folder of every MID Server you want to use for credential-less Discovery.

    ![Nmap installer folder on MID Server](../image/NmapInstallFolder.png)

4.  Copy the Nmap installer file that you downloaded to the `nmap` folder and rename it to `nmapInstaller.exe`.

    ![Rename Nmap installer file](../image/RenameNmapInstaller.png)

5.  Run the `agent\scripts\PowerShell\NmapInstallation.ps1` script and pass it the following parameters in the order in which they appear.

    This script runs the `nmapInstaller.exe` file.

    ![Nmap installer script location](../image/NmapInstallerScript.png)

    1.  **$operation**: Task that `NmapInstallations.ps1` will process. To install Nmap, the task is **install**.
    2.  **$nmap\_root\_path**: Complete path for the `nmap` folder that you create in step 4.
    3.  **$nmap\_self\_installer**: Complete path for `nmapInstaller.exe` file that you copied in step 5.
    4.  **$nmap\_command**: Complete path for the Nmap install command. The`NmapInstallations.ps1` script installs Nmap in the `nmap` folder created in step 4. This parameter is **$nmap\_root\_path\\nmap.exe**.
    5.  **$nmap\_uninstall\_command**: Complete path for the Nmap uninstall command. This command is **$nmap\_root\_path\\Uninstall.exe**.
    6.  **$nmap\_npcap\_version**: The Npcap version installed with Nmap. This value must be the same as the value of the **mid.nmap.npcap.version** property in the MID Server Property \[ecc\_agent\_property\] table.
    7.  **$nmap\_safe\_scripts**: List of safe scripts that Nmap uses. You can retrieve this list from the**mid.nmap.safe.scripts** property in the MID Server Property \[ecc\_agent\_property\] table.
6.  Set up the parameters in the `NmapInstallation.ps1` script in this order:

    **./NmapInstallations.ps1 $operation $nmap\_root\_path $nmap\_self\_installer $nmap\_command $nmap\_uninstall\_command $nmap\_npcap\_version $nmap\_safe\_scripts**

    For example, the script might look like this:

    ```
    PS C:\MidServers\mid1\agent\scripts\PowerShell> .\NmapInstallation.ps1 "install"
    "C:\MidServers\mid1\agent\nmap" "C:\MidServers\mid1\agent\nmap\nmapInstaller.exe"
    "C:\MidServers\mid1\agent\nmap\nmap.exe"
    "C:\MidServers\mid1\agent\nmap\Uninstall.exe" "0.91" 
    "allseeingeye-info.nse,amqp-info.nse,db2-das-info.nse,drda-info.nse,freelancer-info.nse,
    ike-version.nse,mcafee-epo-agent.nse,mqtt-subscribe.nse,openlookup-info.nse,oracle-tns-version.nse,
    quake1-info.nse,quake3-info.nse,rfc868-time.nse,rpcinfo.nse,snmp-info.nse,ventrilo-info.nse,
    weblogic-t3-info.nse,xmpp-info.nse"
    ```

7.  After installation is complete, add the **Nmap** capability to each MID Server you want to use for credential-less Discovery.

    **Important:** Only a **maint** user can add the **Nmap** capability to a MID Server. Contact Customer Service and Support to request temporary **maint** access to your instance.

    1.  On the instance, open the MID Server record.

    2.  Select the **Capabilities** related list.

    3.  Click **Edit**.

    4.  Select **Nmap** from the list of available capabilities and click **Save**.

        ![Add the Nmap capability to the MID Server](../image/AddNmapCapability.png)


## Uninstall Nmap on a self-hosted system

Use this procedure to uninstall Nmap in a self-hosted environment that does not allow network access to the ServiceNow `install.service-now.com` download site.

### Before you begin

Role required: admin, maint

### About this task

Nmap must be manually uninstalled from each MID Server host machine and then disabled on the ServiceNow instance.

### Procedure

1.  Run **Uninstall.exe** in the `nmap` folder on each MID Server host configured for credential-less Discovery.

2.  After uninstallation is complete, delete the `nmap` folder from the `agent` folder.

3.  Remove the **Nmap** capability from each MID Server record.

    **Warning:** Only a **maint** user can remove the **Nmap** capability from a MID Server. Contact Customer Service and Support to request temporary **maint** access to your instance.

    1.  On the instance, open the MID Server record.

    2.  Select the **Capabilities** related list.

    3.  Click **Edit**.

    4.  Remove **Nmap** from the active capabilities list and click **Save**.



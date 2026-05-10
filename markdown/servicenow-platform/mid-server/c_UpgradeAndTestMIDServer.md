---
title: MID Server upgrades
description: Upgrade MID Servers manually, or automatically through the instance. MID Server automatic upgrade is triggered when the instance upgrades and the MID Server no longer has the same version. The new MID Server package is downloaded from install.service-now.com, replaces the old one, and the MID Server starts with the new version.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server upgrades

Upgrade MID Servers manually, or automatically through the instance. MID Server automatic upgrade is triggered when the instance upgrades and the MID Server no longer has the same version. The new MID Server package is downloaded from install.service-now.com, replaces the old one, and the MID Server starts with the new version.

**Warning:** The MID Server can't auto-upgrade on a Windows host if the Windows Application Experience service is turned off. For information on the error that is displayed and instructions for re-enabling this service, see [KB0597552](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597552#appex).

## MID Server upgrade requirements

-   **Access to the MID Server download site**

    The MID Server host computer must have access to the ServiceNow download site at `install.service-now.com` to upgrade automatically. If you have a self-hosted ServiceNow environment that blocks access to the download site, you must import the MID Server installer package into your MID Server hosts manually. For instructions, see [KB0760123](https://support.servicenow.com/kb_view.do?sysparm_article=KB0760123) in the Self-Hosted knowledge base.

-   **MID Server access to OCSP blocked**

    Firewalls and proxy configurations may block calls to the OCSP Entrust and DigiCert servers, which prevents the MID Server from working. You may need to change your firewall permissions so that the OCSP traffic goes through. For more information and resolutions, see the HI Knowledge Base article [\[KB1216223\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1216223).

-   **MID Server operating system compatibility**

    Upgrading Windows or Linux MID Servers with 32-bit operating systems is not supported. For supported operating systems and other host requirements, see [MID Server system requirements](../reference/r_MIDServerSystemRequirements.md).


The MID Server can't upgrade on a Windows host if the Windows Application Experience service is turned off. For information on the error that is displayed and instructions for re-enabling this service, see [KB0597552](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597552#appex&_ga=2.137899701.402632408.1615226320-1555493315.1610383440).

The MID Server upgrade is blocked by some antiviruses running on Windows hosts. For information on the errors and list of these antiviruses, see [KB0870329](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0870329).

Any Linux MID Server upgrade that's service is installed under system in Madrid or lower needs to re-install the service after upgrade. If you didn’t manually reinstall the service in previous upgrades and your MID Server service is still installed on Madrid or lower versions, during upgrade the MID Server automatically re-installs the service. To re-install the service MID Server needs to run as an admin user. If your MID Server upgrade needs to re-install the service, make sure that the MID Server user is admin, or you can manually re-install the service before upgrade. For information about manually re-install the service, see [KB0821436](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0821436).

## When does the MID Server need to upgrade

Any MID Server with a version different from the instance version needs to upgrade. The following two system properties control the version of all MID Servers:

-   **mid.buildstamp**: Identifies the MID Server version with an identifier based on the date of the build. This property uses the format of **mm-dd-yyyy-hhmm**. The MID Server checks for version information hourly. If no override version is configured, the MID Server looks at the **mid.buildstamp** property for the version to use. This property resets itself to the default version \(the version that matches your instance version\) when the instance is restarted or upgraded, so any user changes are lost at that time. The system appends the release name and patch information to the date and time format.

    **Warning:** This property is not visible by default and should not be configured.

-   **mid.version.override**: Sets an override condition for the current version for all MID Servers in your environment. This action pins the MID Servers to a single version and disables the automatic upgrade feature. This property is not visible in the base system and must be added to the System Property \[sys\_properties\] table when it is set. For details, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

When the MID Servers check the version each hour, they look at the **mid.version.override** property first. If this property is empty, the MID Servers get their version information from the **mid.buildstamp** property. If an override version is configured, the MID Servers use this value and ignore the version information in the **mid.buildstamp** property. This override value remains when the instance is restarted and is passed to the MID Servers. The value in the **mid.version.override** property is cleared during an upgrade, which forces the MID Server to reset itself to the version in the **mid.buildstamp** property.

In addition to **mid.version.override**, the MID Server version can also be controlled with the configuration parameter **mid.pinned.version** which pins the MID Server to a specific version.To pin a MID Servers, set the **mid.pinned.version** parameter with the name of that version in the **config.xml** file of each MID Server. Use the format **&lt;version&gt;-mm-dd-yyyy**. This setting overrides the property setting for the pinned MID Server version. For instructions, see [Add a MID Server parameter](../reference/mid-server-parameters.md#). The value set in this parameter is not affected by an upgrade.

**Warning:** Using **mid.version.override** and **mid.pinned.version** is not recommended. The different versions on the MID Server and instance can cause outage issues on the MID Server.

## Upgrade methods

-   **Automatic**

    Automatic upgrade can be triggered by the instance or the MID Server itself. This functionality is available by default. Automatic upgrade occurs:

    -   When the instance is upgraded and the MID Server for that version is different than the version currently on the MID Server. The instance sends **autoUpgrade**system command to the connected MID servers.
    -   Every hour, the MID Server checks with the instance to see if there is a different version available for upgrade. You cannot modify this time period.
-   **Manual**

    Manually start the upgrade by clicking a related link on the MID Server record. Use this method when you do not want to wait until the next hourly automatic update or if your upgrade failed and you want to force an upgrade. See [Upgrade the MID Server manually](../task/t_UpgradeTheMIDServerManually.md) for instructions.


## Upgrade process

1.  **Pre-upgrade Check:**Before starting the actual MID Server upgrade process, the MID Server runs a set of tests to make sure that the host machine meets the minimum requirements. Any errors encountered during this automatic test prevent the upgrade from occurring until the issues are resolved. The pre-upgrade test is enabled by default but can be disabled by adding and setting a system property. See [MID Server pre-upgrade check](../reference/mid-server-pre-upgrade-check.md) for more information.
2.  **Download the packages:**The MID Server downloads upgrade packages from install.service-now.com. These packages are in zip format and are downloaded to the agent folder in the **package/incoming** folder.
3.  **Digital Signature Verification**

    After downloading every package, MID Server verifies the digital signature of the package. It throws an exception if the verification fails. The error will be recorded in the agent log and the MID Server issue table.

    If the packages are downloaded and replaced manually you can verify the signature manually. To manually verify the signature of an installation or upgrade package, use the jarsigner tool which is available for free with JDK. The following is the jarsigner command to initiate the verification: `Jarsigner -verify -verbose -certs -strict <zip-file>`

    The output should be similar to the following example:

    ```
    - Signed by "CN=ServiceNow Inc., O=ServiceNow Inc., L=Santa Clara, ST=California, C=US"
    Digest algorithm: SHA-256
    Signature algorithm: SHA256withRSA, 2048-bit key
    Timestamped by "CN=Symantec SHA256 TimeStamping Signer - G3, OU=Symantec Trust Network, O=Symantec Corporation, C=US" on Tue Nov 05 19:55:37 UTC 2019
    Timestamp digest algorithm: SHA-256
    Timestamp signature algorithm: SHA256withRSA, 2048-bit key
     
    jar verified.
     
    The signer certificate will expire on 2021-08-09.
    The timestamp will expire on 2029-03-22.
    
    ```

4.  **Extracting Zip Files:**After downloading all required packages, the MID Server extracts the zip files.

    -   **Before Rome**: The zip files are extracted in a folder under the operating system defined temporary folder. The folder name is a randomly generated number. The operating system temporary folder is specified by system property **java.io.tmpdir**. On a UNIX host, the value for this property is typically is `/tmp` or `/var/tmp`.
    -   **From Rome onward**: The MID Server avoids using operating system defined temporary folders during MID Server upgrade. The zip files are extracted in a folder in the **work/upgrade\_temp** folder under the agent folder. The folder name format is a randomly generated number. If you want to switch to the previous behavior and use an operating system defined temporary folder you can add **mid.upgrade.use\_os\_temp\_folder**to MID Server’s **config.xml** file and set it to true. To switch the behavior for all MID Servers, you can add it to the MID Server property \[ecc\_agent\_property\] with MID Server field blank.
    **Note:** If you are using [KB0747569](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0747569) to change the**java.io.tmpdir**and you want to keep it for future upgrades from Rome, set **mid.upgrade.use\_os\_temp\_folder**to true after upgrading to Rome. If **mid.upgrade.use\_os\_temp\_folder** is not set to true then **java.io.tmpdir** isn’t applied during the MID Server upgrade and the folder under`agent\work\upgrade_temp` will be used.

5.  **Replace old packages with the upgraded packages:**After downloading and extracting the upgrade packages, the MID Server replaces old files with the new files and starts with the new version. To replace the packages, the MID Server starts a process named **ServiceNow AI Platform Distribution Upgrade** and shuts down. ServiceNow AI Platform Distribution Upgrade waits for the MID Server to shut down properly, then replaces the required files as follows:

    -   **Before Rome:**The process deletes all files and folders in the bin, lib and jre folders and copies the new files into those folders.
    -   **From Rome onward:** The process replaces the files in the bin, lib and jre only if the new version of the file is different from the old version. **ServiceNow Platform Distribution Upgrade** does not clean the upgrade files and the unchanged files are kept.
    If the reinstalling service was required as a part of MID Server upgrade, ServiceNow Platform Distribution Upgrade reinstalls the service before starting the MID Server. For more information refer to [KB0821436](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0821436).

    **Note:**

    If the MID Server upgrade fails in this step the MID Server stays Down. Some anti-viruses block the file replacement in this step. For more information refer to [KB0870329](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0870329).

6.  **Start the MID Server:**After replacing all required files with the new version, the ServiceNow AI Platform Distribution Upgrade starts the MID Server. When the MID Server comes Up with the new version, it cleans up all temporary folders used to extract the upgrade files.

## Upgrade log messages

The MID Server log messages are available in the following log files:

-   Pre-upgrade check log messages are available in agent.log file under agent/logs folder. The message **Performing pre-upgrade validation tests.** indicates that the pre-upgrade check has started. If all mandatory tests are passed, the message **Pre-upgrade validation tests successful. Continuing with upgrade process.** indicates the end of the pre-upgrade check.

-   Log messages for downloading missing files are also available in agent.log. Every package download starts with **Downloading package to PACKAGENAME.ZIP from https://install.service-now.com/ PACKAGEINFO** message. The download progress and the size of downloaded file is monitored in the log. After downloading every package, **Package was successfully downloaded from https://install.service-now.com/ PACKAGEINFO** indicates the successful download.

-   Extracting the zip files is the last step available in the **agent.log**. The message **Upgrading MID server** indicates the start of this step, and the message **Extracting package PACKAGE.ZIP to EXTRACT\_TMP\_FOLDER** is shown for every package extraction. When all required zip files are successfully extracted, the MID Server starts the ServiceNow AI Platform Distribution Upgrade process and the message **Stopping MID server. Bootstrapping upgrade** shows the end of this step before MID Server goes Down.

ServiceNow AI Platform Distribution Upgrade logs include log messages for the process start up and for replacing files during the MID Server upgrade. The upgrade log messages are placed between the messages **\*\*\*\*\*\*\*\*\*\*\*UPGRADE MAIN LOGIN START\*\*\*\*\*\*\*\*\*\*\*** and **\*\*\*\*\*\*\*\*\*\*\*UPGRADE MAIN LOGIN END\*\*\*\*\*\*\*\*\*\*\***. ServiceNow AI Platform Distribution Upgrade log messages can be found in the following log files:

-   In the **glide-dist-upgrade.log** file under temp extract folder. This file is available in upgrade-wrapper/logs folder under temp extract folder. This log file includes process log messages and upgrade log messages.
-   In the **dist-upgrade.log** file in `agent\logs` folder. This file only includes the upgrade portion of log messages. If there was some issue with the process startup you need to look at **glide-dist-upgrade.log.**
-   In **wrapper.log**under `agent\logs` folder. After replacing files, ServiceNow AI Platform Distribution Upgrade appends **glide-dist-upgrade.log** to the wrapper.log file.

## Update the wrapper configuration with upgrade-wrapper-override.conf

The wrapper configuration for `glide-dist-upgrade` can be updated using a `upgrade-wrapper-override.conf` file. Create a file named `upgrade-wrapper-override.conf` in the `agent/conf` folder. Any configurations in the `upgrade-wrapper-override.conf` are used during the upgrade process.

By modifying the configuration with `upgrade-wrapper-override.conf`, debug logs can be enabled at the `dist-upgrade` wrapper level and changes can be tested.

For example, the default timeout may not be long enough for certain JVM level commands. The timeout can be increased with `upgrade-wrapper-override.conf` for the `dist-upgrade` wrapper configuration.

## MID Server states

-   **Upgrading**

    The MID Server status is changed to Upgrading while the upgrade is running. The Upgrading state is similar to the [**Paused**](../task/t_PauseTheMIDServer.md#) state. This is avoids potential miscommunication between the new version of the instance and the previous version of the MID Server during upgrade. While in the Upgrading state, you cannot resume or restart the MID Server. However, you can perform the same actions that you can when the MID Server is in the Paused state.

    **Note:** If you are using an Istanbul instance but you are upgrading a pre-Istanbul MID Server to Istanbul, these upgrade states are not available. They are only available for MID Servers that are already on Istanbul.

-   **Upgrade Failed**

    If the upgrade failed in pre-upgrade check step or download/extract packages step, failed upgrades are handled differently based on the version you are upgrading.

    -   Upgrade to another major release \(such as Istanbul to the next full release\): the status changes to **Upgrade Failed**.
    -   Upgrade from a minor version within a release \(such as Jakarta patch 1 to patch 2\): the MID Server continues using the version it is currently running. It does not perform the upgrade and the status eventually changes to **Up**, assuming the MID Server was already functioning properly.
    -   If the upgrade failed in last step, replacing old version of packages with the new version of packages, the MID Server stays **Down**.

## MID Server upgrade history

Use the MID Server Upgrade History module for troubleshooting problems with MID Server upgrades. The module contains a record of each instance upgrade. Those records provide step-by-step status details for each MID Server's upgrade process. If an error occurs, it is noted in the step and a message is dynamically generated with further details. The table cleanup job automatically deletes issues that haven't been detected for 30 days, regardless of their state. For further information, see [MID Server Upgrade History](mid-server-upgrade-history.md).

## JRE TrustStore certificate migration during JRE updates

For JRE updates after upgrading to Quebec, the MID Server migrates existing self-signed certificates in the JRE TrustStore to the new JRE version's TrustStore. When these certificates are migrated, their aliases are prepended with the string "snc\_".

In order for a certificate to be migrated it must be:

-   an X509 certificate
-   certificate standard v3
-   have the basic constraint extension set to false \(i.e. it is not CA issued\)

The MID Server identifies when a JRE upgrade is about to take place and begins the migration process. Before the migration, the MID Server creates a backup of the original TrustStore as a fall-back in the event of failure. If there is a failure, the backup TrustStore can be manually restored.

-   **[MID Server pre-upgrade check](../reference/mid-server-pre-upgrade-check.md)**  
Prior to an upgrade, the MID Server runs tests to identify issues that could cause the upgrade process to fail or result in a MID Server outage.
-   **[Pinning a MID Server to a specific version](../reference/mid-server-version-selection.md)**  
You can pin all the MID Servers in your environment to a specific version by setting a system property, or you can configure specific versions for individual MID Servers.
-   **[Upgrade the MID Server manually](../task/t_UpgradeTheMIDServerManually.md)**  
You can manually upgrade MID Servers at any time if you do not want to wait for the automatic upgrade.

**Parent Topic:**[MID Server reference](mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](../reference/r_MIDServerSystemRequirements.md)

[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)

[MID Server dashboard](c_MIDServerDashboard.md)

[MID Server properties](../reference/r_MIDServerProperties.md#)

[MID Server parameters](../reference/mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](../reference/mid-config-param-priority.md)

[MID Server File Cleaner](mid_file_cleaner.md)

[MID Server protected records and reserved characters](../reference/mid-server-reserved-characters.md)

[MID Server privileged commands](c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](../reference/r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](../reference/r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)


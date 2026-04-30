---
title: MID Server pre-upgrade check
description: Prior to an upgrade, the MID Server runs tests to identify issues that could cause the upgrade process to fail or result in a MID Server outage.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [MID Server upgrades, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server pre-upgrade check

Prior to an upgrade, the MID Server runs tests to identify issues that could cause the upgrade process to fail or result in a MID Server outage.

Each MID Server contains an AutoUpgrade monitor that compares the MID Server version with that of the instance to determine if the MID Server needs to upgrade. If the AutoUpgrade monitor discovers that the MID Server version is out of date, the monitor runs pre-upgrade validation tests for that MID Server. If an issue is detected, a message is logged to the MID Server Issue \[ecc\_agent\_issue\] table, and the upgrade is blocked. The AutoUpgrade monitor continues to run every hour, until all the tests pass. If there are no blocking issues, the MID Server downloads the appropriate upgrade package and begins the upgrade process. The MID Server pre-upgrade check also runs for the upgrades triggered by the instance when the instance was upgraded, as well as for manual upgrades.

## Pre-upgrade tests

The pre-upgrade runs two sets of tests: **Mandatory tests**and **Alert tests**. Every mandatory test is required to pass to start MID Server upgrade. If a mandatory test was not passed, the test is recorded in the agent log and a [MID Server active issue](../concept/mid-server-active-issues.md) is created in the MID Server issue \[ecc\_agent\_issue\] table. These errors are published before the actual MID Server upgrade occurs and must be resolved before the upgrade can continue. MID Server stops the Upgrade process and changes the status based on [MID Server states](../concept/c_UpgradeAndTestMIDServer.md#section_t1p_jc4_1qb). If any alert test was not passed, a message is added in the agent log and MID Server issue table, but the pre-upgrade check continues and MID Upgrade doesn’t stop.

Pre-upgrade validation tests check the following mandatory tests:

-   At least 1 GB of free disk space
-   Access to the download site at install.service-now.com
-   Verify the digital signature of a sample downloaded file
-   Permission to execute, which involves the following:
    -   Extract a Zip archiver to a temp folder
    -   Copy file from temp folder to the agent folder
    -   Read a text file and validate the content
    -   Delete the pre-upgrade check contents
-   MID Server host machine is not a 32 bit system
-   On Linux MID Servers, the glibC version is at least 2.17

On Windows MID Servers, the pre-upgrade validation runs the following alert tests:

-   Any MID Server Upgrade blocker services is running on the host machine
-   Status of Application Experience on the host machine
-   The MID Server must run as a non-administrator user. If the current **Log On As user** account for the MID Server is **LocalSystem** or is a user that is part of the Administrators group, then the upgrade fails and generates an error log.

## Errors that block the upgrade

These messages describe failing a mandatory test and are published to the MID Server Issue \[ecc\_agent\_issue\] table. Failure of any of these tests blocks the upgrade.

-   **Not enough free disk space. The system reports &lt;n&gt; bytes free**

    This message is displayed when less than 1 GB of free disk space is detected on the MID Server host. This error is also written to the MID Server agent log.

-   **Unable to download updates from the install server**

    This message indicates that either the MID Server host does not have permission to download the installation package from install.service-now.com, or network problems prevent connection. This error is also written to the MID Server agent log.

-   **Signature verification failed:&lt;message&gt;**

    This message indicates that a Verification Exception has occurred when pre-upgrade check tries to verify the digital signature of the downloaded check file.

-   **Unable to verify digital signature:&lt;message&gt;**

    This message indicates that the verification signature process was interrupted by an exception.

-   **Unable to extract contents of pre upgrade check zip**

    This message indicates that the service account on the MID Server host does not have permission to extract the pre-upgrade ZIP archive to the temporary folder.

-   **Unable to create folder &lt;upgrade check file path&gt;**

    This message indicates that the MID Server service account does not have permission to create the upgradeCheck folder for the pre-upgrade checking files in the agent/package path.

-   **Unable to verify file permissions: &lt;message&gt;**

    This message indicates an exception has occurred when checking file permissions, such as a file that does not exist or access failure.

-   **MID Server Windows Service is not running as LocalSystem or a local Administrator**

    This message warns that the Windows service is not running with the desired permissions.

-   **Upgrade Failure: The host machine does not meet the minimum system requirements to upgrade the MID server.**

    MID upgrade is not supported on 32-bit host. Please refer to [KB0863694](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0863694) for more information.

-   **Upgrade Failure: Host does not meet the minimum system requirements to upgrade the MID server. Please refer to MID Server product documentation on GlibC library for more information**

    This error can only occur for Linux MID Servers. Refer to [Java version support](r_MIDServerSystemRequirements.md) for more information.


## Non-blocking warnings

These warnings are displayed in the MID Server Issue \[ecc\_agent\_issue\] table and do not prevent a Windows MID Server from upgrading:

-   **Unable to parse $logOnAsUser**

    This message warns that the Log On As User value for the Windows service is not in either of these expected formats:

    -   user@domain.company.com
    -   domain\\user
-   **Unable to look up Log On As user's groups**

    When the instance attempts to look up the logged on user's group memberships, it executes the **net user &lt;username&gt;** command. The instance expects a certain output structure by the Windows service from this command and issues this warning if the expected output does not match the actual output.

    These PowerShell warnings are written only to the MID Server agent log. Because PowerShell is not required to use a MID Server, these configuration issues do not prevent a Windows MID Server from upgrading. However, these warnings might indicate issues in your environment that require attention.

-   **Skipping PowerShell upgrade checks since PowerShell is not usable**

    PowerShell 3.0 \(at a minimum\) is not installed or powershell.exe is not available to the MID Server service user.

-   **Skipping Powershell test: Target folder has not been initialized**
-   **Skipping Powershell test: Unable to detect the service name**
-   **Service CiscoAMP running on the MID Server host machine is identified as a MID Server upgrade blocker**

    For more information, refer to [KB0870329](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0870329).

-   **The Application Experience is disabled on the MID Server host, which can cause the auto-upgrade process to fail and the MID Server to go down. Enable the service on the host to ensure successful auto-upgrade**

    For more information, refer to [KB0597552](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597552#appex&_ga=2.137899701.402632408.1615226320-1555493315.1610383440).

-   **__Continuing with upgrade, but the following issue was encountered during upgradeCheck: &lt;exception message&gt;__**

    This message indicates that there was an issue running the PowerShell portion of the pre-upgrade tests.


## Disabling the pre-upgrade check

A MID Server configuration parameter called **mid.upgrade.run\_precheck** is set to **true** by default, which allows the automatic pre-upgrade test to run. To disable these tests for a single MID Server, add this parameter to that MID Server's config.xml file and set it to **false**. To disable these tests for all MID Servers, add a new record to the MID Server Property \[ecc\_agent\_property\] table called **mid.upgrade.run\_precheck**. Set the value of this property to **false** and leave the **MID Server** field blank.

**Parent Topic:**[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)


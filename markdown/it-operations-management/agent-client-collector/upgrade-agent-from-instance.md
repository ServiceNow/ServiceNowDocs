---
title: Upgrade an agent in an instance
description: Perform selective self-upgrade instead of bulk upgrade for enhanced efficiency when working with agents that are difficult to access, such as agents deployed in the cloud. You can perform selective upgrade on up to 20 agents at a time.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector installation, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Upgrade an agent in an instance

Perform selective self-upgrade instead of bulk upgrade for enhanced efficiency when working with agents that are difficult to access, such as agents deployed in the cloud. You can perform selective upgrade on up to 20 agents at a time.

## Before you begin

**Note:** Selective upgrade is available for the agents version 2.7.0 and above.

Supported Operating Systems: Windows and Linux.

**Note:**

When working in a Linux environment, ensure that you have sudo permissions and that the following configurations are set:

<table id="id_gcj_ftm_cyb"><thead><tr><th>

OS

</th><th>

OS version

</th><th>

Commands

</th><th>

Agent version

</th></tr></thead><tbody><tr><td>

CentOS,Red Hat

</td><td>

7, 8

</td><td>

-   `/usr/bin/systemctl start acc`
-   `/usr/bin/systemctl stop acc`
-   `<systemctl location> daemon-reload` \(default location is `/usr/bin`\)
-   `/usr/bin/rpm -Uv <cache dir location>/upgrade/agent-client-collector-upgrade.rpm`

 Default cache directory location: `/var/cache/servicenow/agent-client-collector`

 -   `unzip -o`: Unzips the signature file to validate the installation.
-   `openssl dgst -sha256 -verify`: Verifies use of a signature from a servicenow installation file.

</td><td>

2.7

</td></tr><tr><td>

Debian, Ubuntu

</td><td>

 

</td><td>

-   `/usr/bin/systemctl start acc`
-   `/usr/bin/systemctl stop acc`
-   `<systemctl location> daemon-reload` \(default location is `/usr/bin`\)
-   `/usr/bin/dpkg --install --refuse-downgrade --skip-same-version <cache dir location>/upgrade/agent-client-collector-upgrade.deb`

 Default cache directory location: `/var/cache/servicenow/agent-client-collector`

 -   `unzip -o: Unzips the signature file to validate the installation`
-   `gpg -import && gpg --verify: Verifies use of a signature from a servicenow installation file.`

</td><td>

2.7

</td></tr></tbody>
</table>ACC installs will need to access this URL: https://install.service-now.com/.

Role required:

-   Linux: sudo rpm/dpkg
-   Windows: Local SYSTEM account \(Agent Client Collector service running as **Local System**\)

## About this task

Agent Client Collector supports selective self-upgrade in the following operating systems:

-   Windows: Due to Windows UAC restrictions, the agent must run as a local SYSTEM account to perform the upgrade via **msiexec**.
-   Linux: RPM and DEB

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select the agent that you want to upgrade.

3.  In the **Related Links** section, select **Upgrade agent**.

4.  In the confirmation dialog box, select **Upgrade**.

    The **Agent Upgrade Histories** page appears, where you can monitor the upgrade progress in the **State** column, which displays either **Success** or **Failed**.

5.  View the log for the agent upgrade in the **Message** column.

    For a failed upgrade on a Linux machine, navigate to the `<cache directory location>/upgrade/agent-client-collector-upgrade.rpm` file and ensure that the configurations are set for the relevant OS, according to the Linux Operating Systems table, above.

    For a failed upgrade on a Windows machine, check the relevant log file, located at `<user folder>\AppData\Local\Temp\ACC_Logs`:

    -   ACC logs: `ACC_Upgrade.log`
    -   MSI logs: `MSI_ACC_Upgrade.log`


---
title: Upgrade an agent in an instance
description: Perform selective self-upgrade instead of bulk upgrade for enhanced efficiency when working with agents that are difficult to access, such as agents deployed in the cloud. You can perform selective upgrade on up to 20 agents at a time.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [ACC installation, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Upgrade an agent in an instance

Perform selective self-upgrade instead of bulk upgrade for enhanced efficiency when working with agents that are difficult to access, such as agents deployed in the cloud. You can perform selective upgrade on up to 20 agents at a time.

## Before you begin

**Note:** Selective upgrade is available for the agents version 2.7.0 and above.

Supported Operating Systems: Windows and Linux.

Ensure that data files are up to date by restarting the MID Server and collecting host data. For details on collecting host data, see [Run host data collection on demand](acc-run-discovery.md).

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

 **Note:** If you installed the Linux agent using the `--relocate` flag \(for example,

```
rpm -i --relocate /var/cache=/opt/cache
      agent-client-collector-<version_number>-x86_64.rpm
```

\), you must have permission to execute the following commands:

-   `sudo /usr/bin/rpm -q --queryformat '[%{PREFIXES}\\n]' agent-client-collector`
-   `sudo /usr/bin/rpm -q --queryformat '[%{INSTPREFIXES}\\n]' agent-client-collector`

These commands are used by the upgrade script to detect the original relocations and generate the correct upgrade command. Upgrading without the relocation commands might cause installation to fail.

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
</table>When connecting via a MID Server, ACC installs need to access one of the following URLs:

-   `https://<MID-WEBSERVER-URI:PORT>/static/acc_installers/agent-client-collector`
-   `https://install.service-now.com/`

When upgrading MID-less agents, upgrade is performed at the URL set in the **agent-upgrade-url-path** property of the acc.yml file. If no URL is set at this property, upgrade is performed by downloading the installer script from the following Content Delivery Network \(CDN\) URL: `https://cdn-install.sncapps.service-now.com/glide/distribution/builds/package`

**Note:** When using a CDN, send your download request through a proxy server, for added security. For details, see [Configure proxies when performing MID-less upgrade using a Content Delivery Network \(CDN\)](cdn-upgrade-proxies.md).

Select the version to which you want to upgrade your agent.

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
2.  Select **New**.
3.  Assign the following values:
    -   Name = **sn\_agent.agent\_upgrade\_version**
    -   Type = **string**
    -   Value = The version number to be upgraded to, in the format &lt;major\_version.minor\_version.patch\_version&gt;. For example: **4.3.2**
4.  Select **Submit**.

If you do not select a version, the agent automatically upgrades to the current Agent Client Collector Framework scoped app version.

Role required:

-   Windows: Local SYSTEM account \(Agent Client Collector service running as **Local System**\)
-   Linux: sudo rpm/dpkg
-   macOS: sudo pkg

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


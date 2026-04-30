---
title: Install Agent Client Collector on a Linux system
description: Install Agent Client Collector using a package distribution tool. Prior to installing, you can manually install the Agent Client Collector on a few machines to ensure that your agents contain the correct policies and checks before installing a large number of agents.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [ACC installation on a Linux system, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Install Agent Client Collector on a Linux system

Install Agent Client Collector using a package distribution tool. Prior to installing, you can manually install the Agent Client Collector on a few machines to ensure that your agents contain the correct policies and checks before installing a large number of agents.

## Before you begin

-   Ensure that the Agent Client Collector Listener is configured on your MID Servers, and the service is available from your target hosts.
-   Verify that your server's OS and version is supported. For a list of supported OS's and versions, see [Agent Client Collector installation](../concept/acc-installation.md).
-   Verify whether there are restrictions or requirements to be aware of during deployment, such as specifying an account other than the default servicenow account. For more information about embedding the agent into your own automated system, see [ITOM Agent Client Collector documentation material \[KB1122613\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1122613).
-   Ensure that the MID Server and its MID Web Server and ACC Websocket Endpoint extensions are up and running.
-   Retrieve the MID Server ACC Listener information to be specified in the agent's **backend-url** parameter.
    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **MID Servers**.
    2.  Select a MID Server.
    3.  Select the **ACC Websocket Endpoints** tab.
    4.  Select a websocket endpoint.
    5.  Copy the value in the **Endpoint URL** field.
-   Retrieve the MID Server API key specified in the agent's **api-key** parameter.
    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **MID Web Server API Key**.
    2.  Select the API key you want to use.
    3.  In the **Related Links** section, select **View API key**.
    4.  Copy the API key value and close the pop-up window.

Role required: agent\_client\_collector\_admin

## About this task

During Linux installation \(and upgrade\), the agent executable file is enabled with Linux capabilities \(CAP\_SETFCAP, CAP\_SETPCAP\) by default. Store apps such as Agent Client Collector Log Analytics \(ACC-L\) can use this to grant capabilities to read the entire file system \(CAP\_DAC\_READ\_SEARCH\). The system undergoes various security measures, such as double verification of the content origination, leveraging the plugin verification process and more, to ensure that granting capabilities does not pose a security risk. This procedure assumes that you are familiar with commands for Linux capabilities.

To opt out of these enhanced capabilities, run the following commands, based on your Linux OS/packaging system:

<table id="table_zgx_pfw_vcc"><thead><tr><th>

OS/Packaging System

</th><th>

Commands

</th></tr></thead><tbody><tr><td>

RPM

</td><td>

`ACC_SKIP_CAPS=true yum / dnf localinstall`

 `ACC_SKIP_CAPS=true rpm -vi agent-client-collector-<version number>-x86_64.rpm`

</td></tr><tr><td>

Debian

</td><td>

`ACC_SKIP_CAPS=true apt-get install`

 `ACC_SKIP_CAPS=true dpkg -i agent-client-collector-<version number>-<distro>_amd64.deb`

</td></tr><tr><td>

SLES

</td><td>

`ACC_SKIP_CAPS=true zypper install`

</td></tr></tbody>
</table>## Procedure

1.  Download the relevant installation packages.

    -   For manual installation:
        1.  Navigate to **** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads**.
        2.  Download the relevant .rpm or .deb installation file.
        3.  Download the relevant signature files to validate the installation files.
    -   For command-line installation, run the following commands to download both the signature and installation files to your local machine:

        ```
        curl -LO https://install.service-now.com/glide/distribution/builds/package/app-signed/agent-client-collector-<version_number>-x86_64.rpm
        curl -LO https://install.service-now.com/glide/distribution/builds/package/app-signed/agent-client-collector-<version_number>-x86_64-rpm-rpm.zip
        
        ```

        **Note:** Each curl command must appear on a single line.

2.  Verify the package signature.

    1.  Extract the installation file \(if it is compressed\) by running the following command:

        `unzip agent_client-collector-<version_number>-x86_64-rpm-rpm.zip`

    2.  Validate the installation file signature by running the indicated commands.

        -   On an RPM-based system:

            ```
            openssl dgst -sha256 -verify {<ServiceNow DGST pem key>} -signature {<signature file>} agent-client-collector-<version number>-x86_64.rpm
            ```

            Where `<ServiceNow DGST pem key>` is the `.pem` file extracted from the `.zip` file, and `<signature file>` is the `.bin` file extracted from the `.zip` file.

            For example:

            ```
            $ curl -sLO https://install.service-now.com/glide/distribution/builds/package/app-signed/agent-client-collector-3.0.0-x86_64.rpm
            $ curl -sLO https://install.service-now.com/glide/distribution/builds/package/app-signed/agent-client-collector-3.0.0-x86_64-rpm-rpm.zip
            $ unzip agent-client-collector-3.0.0-x86_64-rpm-rpm.zip
            Archive: agent-client-collector-3.0.0-x86_64-rpm-rpm.zip
            inflating: ServiceNow_Digicert_DGST.pem
            extracting: agent-client-collector-3.0.0-x86_64.bin
            $ openssl dgst -sha256 -verify ServiceNow_Digicert_DGST.pem -signature agent-client-collector-3.0.0-x86_64.bin agent-client-collector-3.0.0-x86_64.rpm
            Verified OK
            ```

            **Note:** Each command must appear on a single line.

        -   On a Debian-based system:

            `gpg --import ServiceNow_Digicert_Public.gpg`

            `sudo gpg --verify agent-client-collector-<version number>-<distro>_amd64.deb`

            For example:

            ```
            $ curl -sLO https://install.service-now.com/glide/distribution/builds/package/app-signed/agent-client-collector-3.0.0-debian-9_amd64.deb
            $ curl -sLO https://install.service-now.com/glide/distribution/builds/package/app-signed/agent-client-collector-3.0.0-debian-9_amd64-deb-deb.zip
            $ unzip agent-client-collector-3.0.0-debian-9_amd64-deb-deb.zip
            Archive: agent-client-collector-3.0.0-debian-9_amd64-deb-deb.zip
            extracting: ServiceNow_Digicert_Public.gpg
            $ gpg --import ServiceNow_Digicert_Public.gpg
            gpg: /home/admin/.gnupg/trustdb.gpg: trustdb created
            gpg: key 985DD52C6A0ABB45: public key "ServiceNow, Inc. (Signing) <seceng@servicenow.com>"
            imported
            gpg: Total number processed: 1
            gpg: imported: 1
            $ dpkg-sig --verify agent-client-collector-3.0.0-debian-9_amd64.deb
            Processing agent-client-collector-3.0.0-debian-9_amd64.deb...
            GOODSIG _gpgbuilder 9B928FB49771DF6C047430DD985DD52C6A0ABB45 1665054068
            ```

            **Note:** Each command must appear on a single line.

3.  Install the Agent Client Collector package using the package manager associated with Linux distribution.

    |OS|Command|
    |---|-------|
    |RHEL-based|`yum / dnf localinstall`|
    |SLES|`zypper install`|
    |Debian-based|`apt-get install`|

    Alternatively, if these commands are not configured correctly, you can use the core commands that are configured to run with the package manager commands.

    -   RPM-based system: `# rpm -vi agent-client-collector-<version number>-x86_64.rpm`
    -   Debian-based system: `# dpkg -i agent-client-collector-<version number>-<distro>_amd64.deb`
    Verify that the package commands are configured correctly with your system administrator.

    **Note:** Some file systems may have restrictions enabled; for example, `/var/` may be mounted with a **noexec** flag. Because the agent must execute Agent Client Collector plugins that are normally store in the `/var/cache` directory, you must deploy the application into specific folders by customizing the installation paths using the **--relocate** option as an `.rpm` parameter.

    For example: `rpm -i --relocate /var/cache=/opt/cache agent-client-collector-<version_number>-x86_64.rpm`

    The following paths can be relocated:

    |Path|Notes|
    |----|-----|
    |`/etc`|When updating, you must also update the **allow-list** parameter in the `acc.yml` file with the new path.|
    |`/usr/share`|N/A|
    |`/var/cache`|Updating the `/var` directory retains all `/var` subdirectories, nested under the new directory.|
    |`/var/log`|
    |`/var/run`|
    |`/var`|

    Review the paths in `/usr/lib/systemd/system/acc.service` to ensure that they appear as expected.

4.  When installing a .deb package, configure the agent's `acc.yml` configuration file.

    1.  Copy the sample configuration file by running the following command.

        `# cp -p /etc/servicenow/agent-client-collector/acc.yml.example /etc/servicenow/agent-client-collector/acc.yml`

    2.  Rename the allow list file.

        `# cp -p /etc/servicenow/agent-client-collector/check-allow-list.json.default /etc/servicenow/agent-client-collector/check-allow-list.json`

    **Note:** This step is not relevant for .rpm packages, which come with `acc.yml` and `check-allow-list.json` files included in the base system.

5.  Update the configuration file, adding **check-allow-list.json** to `/etc/servicenow/agent-client-collector` and copying the `backend-url` and `api-key` from the instance.

    For example:

    ```
    ---
    # Agent Client Collector configuration
    backend-url:
     - "wss://YOUR_MID_ENDPOINT_HERE:YOUR_MID_PORT_HERE/ws/events"
    api-key: "YOUR_API_KEY_HERE"
    log-level: "info"
    insecure-skip-tls-verify: false
    allow-list: /etc/servicenow/agent-client-collector/check-allow-list.json
    verify-plugin-signature: true
    max-running-checks: 10
    disable-sockets: true
    disable-api: true
    statsd-disable: true
    enable-auto-mid-selection: false
    agent_cpu_threshold:
     cpu_percentage_limit: 25
     repeated_high_cpu_num: 3 
     monitor_interval_sec: 60
     agent_cpu_threshold_disabled: false
    
    ```

    The **allow-list** feature, indicating the commands permitted to be executed by the agent, is enabled.

6.  Configure sudoers.

    Configuration is typically automated by your Linux sysadmin. To configure manually if you want to ensure correctness before full configuration, run the following.

    ```
    # visudo -f /etc/sudoers.d/01_servicenow
    User_Alias ACC_USERS = servicenow
    Cmnd_Alias ACC_CMD = /usr/sbin/dmidecode -s baseboard-serial-number,/usr/sbin/dmidecode -s chassis-serial-number,/usr/sbin/dmidecode -s system-serial-number,/usr/sbin/dmidecode -s system-uuid,/usr/sbin/ss -tanp
    Cmnd_Alias ACC_CMD_SETENV = /usr/bin/netstat -ltnup,/usr/bin/ls -l /proc/*,/usr/bin/cat /proc/*
    ACC_USERS ALL = (root) NOPASSWD:ACC_CMD
    ACC_USERS ALL = (root) NOPASSWD:SETENV:ACC_CMD_SETENV
    Defaults:ACC_USERS !requiretty
    ```

7.  Configure the agent to run as a service.

    1.  Safeguard resource consumption by adding the indicated values to the `/usr/lib/systemd/system/acc.service` file.

        -   CPUShares=128
        -   CPUQuota=10%
        -   MemoryLimit=192M
        -   BlockIOWeight=10
        -   LimitNICE=15
        For example:

        ```
        # vi /usr/lib/systemd/system/acc.service
        [Unit]
        Description=Agent-Now acc
        After=network-online.target
        [Service]
        Environment=AGENT_ROOT=/usr/share
        Environment=AGENT_CACHE_ROOT=/var/cache
        Environment=AGENT_CONFIG_ROOT=/etc
        Environment=AGENT_LOG_ROOT=/var/log
        Environment=AGENT_RUN_ROOT=/var/run
        Environment=RUBYOPT=-Eutf-8
        User=servicenow
        Group=servicenow
        ExecStart=/usr/share/servicenow/agent-client-collector/bin/acc-service start acc
        KillMode=process
        Restart=on-failure
        RestartSec=1min
        **CPUShares=128**
        **CPUQuota=10%**
        **MemoryLimit=192M**
        **BlockIOWeight=10**
        **LimitNICE=+15**
        [Install]
        WantedBy=network-online.target
        ```

    2.  Run the reload daemon command If you modified the service file after enabling the acc service.

        `# systemctl daemon-reload`

    3.  Enable and start the service by running the following commands.

        `# systemctl enable acc`

        `# systemctl start acc`


**Parent Topic:**[Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md)


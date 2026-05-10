---
title: Install MID-less Agent Client Collector manually in a Linux environment
description: Install MID-less Agent Client Collector manually on a Linux machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Installing MID-less ACC, Configuring MID-less ACC, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Install MID-less Agent Client Collector manually in a Linux environment

Install MID-less Agent Client Collector manually on a Linux machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.

## Before you begin

-   Install the ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\) plugin.
-   Onboard your instance to use ITOM Cloud Services. For details, contact Customer Support.
-   Configure an agent registration key. For details, see [Configure an agent registration key](agent-registration-key-configuration.md).
-   Role required: agent\_client\_collector\_admin

## About this task

For details on sending data through the cloud in a MID-less deployment, see [DEX Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-architecture.md).

## Procedure

1.  Download the relevant installation package.

    1.  Navigate to **** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads**.

    2.  Download the relevant .rpm or .deb installation file.

    3.  Download the relevant signature files to validate the installation files.

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

4.  Run the relevant package upgrade command, based on the cpu your machine runs with:

    -   Intel cpu:

        ```
        sudo installer -pkg agent-client-collector-<version number>-macos_x64.pkg -target /
        ```

    -   Apple silicon cpu:

        ```
        sudo installer -pkg agent-client-collector-<version number>-macos_arm64.pkg -target /
        ```

    This command also backs up and restores the agent-id and configuration files before upgrading.

5.  In the `acc.yml` configuration file:

    1.  Set the following parameters:

        |Parameter|Value|
        |---------|-----|
        |backend-url|"&lt;gateway URL&gt;"|
        |connect-without-mid|true|
        |instance-url|"&lt;instance URL&gt;"|
        |registration-key|"&lt;regsitration-key&gt;"|
        |insecure-skip-tls-verify|false|

    2.  Comment out the **api-key** parameter.

6.  Save the configuration file.

7.  Configure sudoers.

    Configuration is typically automated by your Linux sysadmin. To configure manually if you want to ensure correctness before full configuration, run the following.

    ```
    # visudo -f /etc/sudoers.d/01_servicenow
    User_Alias ACC_USERS = servicenow
    Cmnd_Alias ACC_CMD = /usr/sbin/dmidecode -s baseboard-serial-number,/usr/sbin/dmidecode -s chassis-serial-number,/usr/sbin/dmidecode -s system-serial-number,/usr/sbin/dmidecode -s system-uuid,/usr/sbin/ss -tanp
    ACC_USERS ALL = (root) NOPASSWD:ACC_CMD
    Defaults:ACC_USERS !requiretty
    ```

8.  Configure the agent to run as a service.

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


**Parent Topic:**[Installing MID-less Agent Client Collector](../concept/acc-itom-cloud-services.md)


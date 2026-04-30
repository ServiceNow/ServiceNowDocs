---
title: Install the Edge Encryption proxy server \(command line installer\)
description: Install an Edge Encryption proxy on a 64-bit Windows or Linux computer.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Install the Edge Encryption proxy server \(command line installer\)

Install an Edge Encryption proxy on a 64-bit Windows or Linux computer.

## Before you begin

Role required: admin

Java version 11.0.6 or later in the 11.x version series is required to run the installer.

## About this task

Install the Edge Encryption proxy server on a machine in your network using the appropriate command for your target machine. If installing the Edge Encryption proxy server on a Windows machine, you must additionally install the proxy server as a Windows service.

When you upgrade the Edge Encryption proxy server, the system backs up the old proxy in the `backup.dist-upgrade-<timestamp>` directory under the current installation directory. The backup directory is generated during the upgrade process and stores the old proxy information.

When you run an upgrade via the command line, a dist-upgrade.log may be generated in the directory where the command runs. The dist-upgrade.log contains logs for the upgrade process.

In case of a failed upgrade, the system creates a `failed-backup.dist-upgrade-<timestamp>` directory. In addition, `logs/wrapper.log` in the original proxy directory may also contain failure information.

## Procedure

1.  Create the installation directory.

2.  Download the Edge Encryption proxy archive file to the installation directory.

3.  Open the terminal and change to the installation directory.

    **Note:** If installing on a Windows machine, you must start the Windows Command Prompt with administrator privileges.

4.  Run this command for the target machine and change the variables according to your configuration: `java -jar edgeencryption-<version>-all.jar -m install –n <proxy_name> --instancehost <host> -p <port> --protocol https –s <install_path>`

<table id="table_qc1_krk_kdb"><thead><tr><th>

Option

</th><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

none

</td><td>

version

</td><td>

Version number of the Edge Encryption proxy being used to perform the current operation.

</td></tr><tr><td>

-m

</td><td>

mode

</td><td>

Runtime mode. Options are "install" for a new Edge proxy server or “dist-upgrade” to upgrade an existing Edge proxy server.

</td></tr><tr><td>

-n

</td><td>

proxy\_name

</td><td>

Name of the installed Edge Encryption proxy server. Use a unique proxy\_name to be able to identify specific proxy instances.

</td></tr><tr><td>

--instancehost

</td><td>

host

</td><td>

The host name of your ServiceNow instance \(for example, `mycompany.service-now.com`\).

</td></tr><tr><td>

-p

</td><td>

port

</td><td>

Port your ServiceNow instance listens on. Typically secure HTTPS connections listen on port **443** and HTTP connections listen on port **80**.

</td></tr><tr><td>

--protocol

</td><td>

protocol

</td><td>

Protocol the installed Edge proxy uses when connecting to the backend ServiceNow host. This is typically **HTTPS** \(preferred for secure TLS connections\) or **HTTP** \(connections without TLS\) depending on which protocol the host instance supports.

</td></tr><tr><td>

-s

</td><td>

install\_path

</td><td>

Path to the directory or folder where the new Edge proxy is installed \(the destination directory\). If the directory does not already exist, this command will create it. If it does exist it must not contain an existing installation.

 If this option is skipped, the default folder name is derived from the proxy\_name and port \(for example, `EdgeProxy_443`\), in the current directory.

</td></tr></tbody>
</table>    **Note:** Do not copy and paste commands from the browser. Occasionally, copy/paste operations cause unexpected characters to be pasted to the target machine and results in the command being executed incorrectly. It is best to type out the command by hand using documentation as a reference.

    To see the help screen, execute this command with the `–help` option: `java -jar edgeencryption-<version>-all.jar --help`

5.  If installing on a Windows machine, install the Edge Encryption proxy as a Windows service.

    1.  Change the name of the service by opening the `conf/wrapper.conf` file on the new proxy and setting the properties in the following table.

        |Property|Description|
        |--------|-----------|
        |wrapper.ntservice.name|Unique name of the Edge Encryption proxy service.|
        |wrapper.ntservice.displayname|Edge Encryption proxy service display name.|
        |wrapper.ntservice.description \(Optional\)|Proxy server description.|

        If this step is not performed, the Edge Encryption proxy service is installed under the name **Edge Encryption**.

    2.  Save and close the file.

    3.  Open the Windows Command Prompt and `cd` to `ServerName_port/bin`.

    4.  Execute `edgeencryption.bat install`.


## Result

The `ProxyName_port` directory is created in the current directory. The `edgeencryption.properties` file is updated with the host, port, and protocol values from the command line.

**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Next topic:**[Create and configure the RSA key pair for the digital signature](t_SetUpAKeyPair.md)


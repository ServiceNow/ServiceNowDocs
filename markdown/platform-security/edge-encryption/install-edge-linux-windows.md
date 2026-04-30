---
title: Install the Edge Encryption proxy server \(command line installer\)
description: Install an Edge Encryption proxy on a 64-bit Windows or Linux computer.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2024-08-01"
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

4.  Run this command for the target machine and change the variables according to your configuration: `java -jar edgeencryption-<version>-all.jar -m install -n <ProxyName> --instancehost <host> -p <InstancePort> --protocol https`

    |Option|Variable|Description|
    |------|--------|-----------|
    |none|version|Version number of the Edge Encryption proxy being used to perform the current operation.|
    |-m|mode|The operation or mode to run in \(install or dist-upgrade\).|
    |-n|ProxyName|The name of the encryption proxy instance. Use a unique `ProxyName` to be able to identify specific proxy instances.|
    |--instancehost|host|The host name of your ServiceNow instance \(for example, `mycompany.service-now.com`\).|
    |-p|InstancePort|The port of your instance. When the protocol is https, the port is normally 443.|
    |--protocol|protocol|The protocol used to access your ServiceNow instance \(typically https\).|

    **Note:** Do not copy and paste commands from the browser. Occasionally, copy/paste operations cause unexpected characters to be pasted to the target machine and results in the command being executed incorrectly. It is best to type out the command by hand using documentation as a reference.

    To see the help screen, execute this command without arguments: `java -jar edgeencryption-<version>-all.jar`

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


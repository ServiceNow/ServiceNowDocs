---
title: Start the Edge Encryption proxy
description: After an Edge Encryption proxy is installed and configured, you can start the proxy from the command line.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Start the Edge Encryption proxy

After an Edge Encryption proxy is installed and configured, you can start the proxy from the command line.

## Before you begin

Role required: admin

Before starting the encryption proxy, verify the following:

-   The Edge Encryption plugin is activated on the instance.
-   The `edgeencryption.properties` file on this machine has been configured.
-   If using an order preserving encryption type or encryption patterns, the proxy database is running.

**Note:** The first time you set up the `edgeencryption.properties` file or change properties, you may not want to set the password encryption property. After you have verified that everything is working, you can set the password encryption property, shut down the proxy, and then restart the proxy.

## Procedure

1.  Run the proxy server.

<table id="choicetable_mpf_khb_tt"><tbody><tr><td id="d204375e93">

**On a Linux machine**

</td><td>

1.  `cd` to `ServerName_port`
2.  Execute `./startup.sh`


</td></tr><tr><td id="d204375e117">

**On a Windows machine**

</td><td>

Perform the following steps from the command line as admin:1.  `cd` to `ServerName_port/bin`
2.  Execute `edgeencryption.bat start`


</td></tr></tbody>
</table>2.  Check the log on the proxy server to verify that the proxy is running.


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Set the proxy server initial memory limit and upper bound memory limit](increase-memory.md)

**Next topic:**[Obfuscate passwords in the properties file](t_SetUpPasswordEncryption.md)


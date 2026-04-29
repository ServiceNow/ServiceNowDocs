---
title: Manually add an additional proxy
description: After the first Edge Encryption proxy is properly configured and tested, you can set up additional proxies on a Linux or Windows machine. Installing multiple proxies on the same machine is not recommended.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Manually add an additional proxy

After the first Edge Encryption proxy is properly configured and tested, you can set up additional proxies on a Linux or Windows machine. Installing multiple proxies on the same machine is not recommended.

## Before you begin

Role required: admin

## About this task

Add additional proxy servers on additional machines to ensure an optimal environment. See [Sizing your Edge Encryption environment](../concept/edge-environment-size.md) to determine the number of additional proxies needed.

**Note:** Make sure that all proxies have the same encryption keys and the same RSA key pair used to digitally sign encryption configuration and encryption rules. If a proxy database was set up as part of the installation, all proxies must use the same proxy database.

## Procedure

1.  Install the proxy using the appropriate command.

    For more information, see [Install the Edge Encryption proxy server \(interactive installer\)](install-proxy.md).

2.  Copy all the encryption keys and the `edgeencryption.properties` file from the first proxy to the new proxy.

    Encryption keys may be located in the proxy keystore, in the `/keys` directory, or in a SafeNet KeySecure keystore.

3.  Open the `edgeencryption.properties` file on the new proxy.

4.  Change the following properties:

    |Property|Description|
    |--------|-----------|
    |**edgeencryption.proxy.name**|Unique name of the proxy server|
    |**edgeencryption.proxy.host**|The server name, IP address, or fully-qualified domain name of the computer running the proxy.|
    |**edgeencryption.proxy.http.port**|Port on the proxy for HTTP communication. Must be unique across all processes on the machine.|
    |**edgeencryption.proxy.https.port**|Port on the proxy for HTTPS communication. Must be unique across processes on the machine.|

5.  If installing the proxy server on a Windows machine, you must change the name of the service. by opening the `conf/wrapper.conf` file on the new proxy and adding the properties listed in the following table.

    **Note:** You must perform this step before launching the proxy server.

    |Property|Description|
    |--------|-----------|
    |**wrapper.ntservice.name**|Unique name of the Edge Encryption proxy service.|
    |**wrapper.ntservice.displayname**|Edge Encryption proxy service display name.|
    |**wrapper.ntservice.description** \(Optional\)|Proxy server description.|

6.  Save and close the file.

7.  Launch the proxy using the appropriate command.

    For more information, see [Start the Edge Encryption proxy](t_RuntheProxy.md).


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Obfuscate passwords in the properties file](t_SetUpPasswordEncryption.md)

**Next topic:**[Authenticate an Edge Encryption proxy server](authenticate-edge-proxy.md)


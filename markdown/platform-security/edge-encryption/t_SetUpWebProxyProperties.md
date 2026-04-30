---
title: Configure a web proxy
description: If your network uses a web proxy, you can set up the Edge Encryption proxy to use the web proxy.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure a web proxy

If your network uses a web proxy, you can set up the Edge Encryption proxy to use the web proxy.

## Before you begin

Role required: admin

## About this task

If your network does not use a web proxy, leave the [web proxy properties](../reference/edge-encryption-proxy-server-properties.md) in the configuration file commented out.

The Edge Encryption proxy server supports HTTP connection to and basic authentication with the web proxy.

## Procedure

1.  Change to the `<installation directory>/conf/` directory.

2.  Open the `edgeencryption.properties` file.

3.  Configure the [web proxy properties](../reference/edge-encryption-proxy-server-properties.md).

4.  Save and close the `edgeencryption.properties` file.

5.  If the web proxy is using a customer-specific server certificate, add this certificate to the JVM used by the Edge Encryption proxy server to establish trust between the web proxy and the Edge Encryption proxy server.

    1.  Use the `cd` command to navigate to `<Java home directory>/jre/lib/security/cacerts`

    2.  Execute the command: `keytool -keystore cacerts -importcert -alias <chooseAlias> -file <certificateFile>`


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Configure additional properties in the Edge Encryption properties file](set-props.md)

**Next topic:**[Set the proxy server initial memory limit and upper bound memory limit](increase-memory.md)


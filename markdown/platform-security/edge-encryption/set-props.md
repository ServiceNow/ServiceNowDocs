---
title: Configure additional properties in the Edge Encryption properties file
description: After installing the Edge Encryption proxy server in your network and setting up your keystore and keys, configure the additional Edge Encryption properties.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure additional properties in the Edge Encryption properties file

After installing the Edge Encryption proxy server in your network and setting up your keystore and keys, configure the additional Edge Encryption properties.

## Before you begin

Role required: admin

## Procedure

1.  Open the `<installation directory>/conf/edgeencryption.properties` file and configure the following Edge Encryption proxy server properties:

    -   [Target \(instance\) properties](../reference/edge-encryption-proxy-server-properties.md)
    -   [User account properties](../reference/edge-encryption-proxy-server-properties.md)
    -   [Proxy properties](../reference/edge-encryption-proxy-server-properties.md)
    -   If using order preserving encryption types or encryption patterns, configure the [Proxy database properties](../reference/edge-encryption-proxy-server-properties.md)
    -   [Clear text and static IV properties](../reference/edge-encryption-proxy-server-properties.md)
2.  Save and close the file.


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Configure encryption keys on the instance](t_RotateEncryptionKeys.md)

**Next topic:**[Configure a web proxy](t_SetUpWebProxyProperties.md)


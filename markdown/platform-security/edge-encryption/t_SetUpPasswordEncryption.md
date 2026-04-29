---
title: Obfuscate passwords in the properties file
description: Obfuscate passwords in the edgeencryption.properties file to be able to share the properties file without revealing clear text passwords.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Obfuscate passwords in the properties file

Obfuscate passwords in the `edgeencryption.properties` file to be able to share the properties file without revealing clear text passwords.

## Before you begin

Role required: admin

Make sure that the Edge Encryption proxy server is set up and successfully running before you set this property. Before setting this property, [Stop the Edge Encryption proxy](t_StoptheProxy.md).

## About this task

Setting this property may make it difficult to debug connection and access issues during initial startup. Only set this property in production environments after the proxy has been set up and tested successfully.

## Procedure

1.  Change to the `<installation directory>/conf/` directory.

2.  In the `conf` directory, create a text file containing a complex string or phrase that can be used as a passphrase which the proxy uses to obfuscate the passwords in the `edgeencryption.properties` file.

    This passphrase should be a random and complex phrase not related to the passwords themselves.

3.  Open the `edgeencryption.properties` file.

4.  Set the [password encryption property](../reference/edge-encryption-proxy-server-properties.md).

5.  Save and close the `edgeencryption.properties` file.


## What to do next

After setting this property, you can [Start the Edge Encryption proxy](t_RuntheProxy.md).

**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Start the Edge Encryption proxy](t_RuntheProxy.md)

**Next topic:**[Manually add an additional proxy](t_AddAdditionalProxies.md)


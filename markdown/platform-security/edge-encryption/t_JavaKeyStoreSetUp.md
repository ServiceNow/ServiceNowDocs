---
title: Set up a Java KeyStore keystore
description: You can use a Java KeyStore keystore to store encryption keys.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up a keystore and encryption keys, Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Set up a Java KeyStore keystore

You can use a Java KeyStore keystore to store encryption keys.

## Before you begin

Role required: admin

You must use the Java 1.8 version of the keytool utility. A copy of the utility can be found in `<proxy install dir>/java/jre/bin/keytool`.

## About this task

The Edge Encryption proxy ships with the Java JCEKS KeyStore file named `keystore.jceks` in the `keystore` directory. This keystore file contains the ServiceNow public key used to validate encryption rules signed by ServiceNow.

## Procedure

1.  Set up the keystore properties.

    1.  Change to the `<installation directory>/conf/` directory.

    2.  Open the `edgeencryption.properties` file.

    3.  Enter the properties for the [Java KeyStore](../reference/edge-encryption-proxy-server-properties.md).

2.  Save and close the `edgeencryption.properties` file.


## What to do next

After setting up the Java KeyStore, [Create encryption keys using the Java KeyStore keytool](t_CreateEncryptionKeys.md).

-   **[Create encryption keys using the Java KeyStore keytool](t_CreateEncryptionKeys.md)**  
You can use the keytool shipped with the encryption proxy distribution to create AES 128-bit and AES 256-bit encryption keys.

**Parent Topic:**[Set up a keystore and encryption keys](set-up-keystore.md)


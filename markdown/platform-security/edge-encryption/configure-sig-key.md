---
title: Configure the signature key
description: Configure the signature key after installing the proxy server through the Edge Encryption proxy installer.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure the signature key

Configure the signature key after installing the proxy server through the Edge Encryption proxy installer.

## Before you begin

Role required: admin

## About this task

The signature key signs changes to configurations and properties made by the proxy server. The signature key must be an asymmetric RSA key pair in a JCEKS KeyStore.

**Note:** If installing multiple proxies, each proxy must use the same signature key.

## Procedure

1.  On the Signature Key page of the Edge Encryption installer, select the keystore on the host machine to store the signature key.

    -   **Create New Java KeyStore**: Enter the directory location, name, and password for the new keystore.
    -   **Use Existing Keystore**: Enter the keystore file location and password.
2.  Click **Next**.

3.  Select or create a signature key.

    -   **New Key**: Create a signature key for this proxy.
    -   **Use Existing Key**: Use an RSA key-pair from the selected keystore.
    -   **Import Existing Key**: Import an RSA key-pair from a different keystore. Browse to the keystore file, enter the password for the keystore, and select the key alias. Provide a new alias for the key.
4.  Click **Next**.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Previous topic:**[Configure CyberArk properties protection](configure-cyberark-prop-protection.md)

**Next topic:**[Configure the HTTPS certificate](configure-cert.md)


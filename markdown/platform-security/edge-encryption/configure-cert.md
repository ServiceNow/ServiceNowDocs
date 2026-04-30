---
title: Configure the HTTPS certificate
description: To enable clients to connect to the Edge Encryption proxy server using a secure SSL connection, import the HTTPS certificate to the proxy server.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure the HTTPS certificate

To enable clients to connect to the Edge Encryption proxy server using a secure SSL connection, import the HTTPS certificate to the proxy server.

## Before you begin

Role required: admin

## About this task

The Edge Encryption proxy provides the HTTPS certificate to clients trying to connect.

## Procedure

1.  On the HTTPS Certificate page of the Edge Encryption installer, select the keystore to store the certificate.

    -   **Create New Java KeyStore**: Enter the directory location, name, and password for the new keystore.
    -   **Use Existing Keystore**: Enter the keystore file location and password.
2.  Click **Next**.

3.  Select or import a certificate.

    The key alias is the given alias for the certificate.

    -   **Use Existing Certificate**: Use an existing certificate in the selected keystore.
    -   **Import from File or KeyStore**: Import a certificate from a different keystore or a .cer file. Browse to the keystore or .cer file, enter the password, and select the alias. You must provide a new alias for the certificate.
4.  Click **Next**.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Previous topic:**[Configure the signature key](configure-sig-key.md)

**Next topic:**[Configure the AES 128-bit encryption key](configure-128-key.md)


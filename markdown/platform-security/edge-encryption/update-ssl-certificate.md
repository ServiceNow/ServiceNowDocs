---
title: Update SSL certificate
description: When updating an SSL certificate on an Edge proxy server, you must delete the old one.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Update SSL certificate

When updating an SSL certificate on an Edge proxy server, you must delete the old one.

## Before you begin

Role required: admin

## About this task

When updating the SSL certificate on the Edge proxy server, you must also delete the old certificate. If you don't, the old certificate \(in the form of an alias in the KeyStore file\) continues to be used even though the Edge proxy server is configured to use the new certificate.

## Procedure

1.  On the Edge proxy server, list the entries in the Java KeyStore:

    ```
    keytool -list -keystore keystore.jceks -storetype jceks -storepass MY_SUPER_PASSWORD
    ```

2.  Remove the old SSL certificate:

    ```
    keytool -delete -alias MY_OLD_ALIAS -keystore keystore.jceks -storetype jceks -storepass MY_SUPER_PASSWORD
    ```

3.  Add the new SSL certificate into the Java KeyStore.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Previous topic:**[Configure the AES 256-bit encryption key](configure-256-key.md)

**Next topic:**[Configure the Edge Encryption proxy database](configure-proxy-db.md)


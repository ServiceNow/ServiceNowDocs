---
title: Import and configure the certificate for secure SSL connection
description: To use a secure SSL connection, import a server certificate and add it to the Java KeyStore.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Import and configure the certificate for secure SSL connection

To use a secure SSL connection, import a server certificate and add it to the Java KeyStore.

## Before you begin

Role required: admin

You must obtain the server certificate and matching private key before adding it to the Java KeyStore.

## Procedure

1.  Generate a Certificate Signing Request \(CSR\) using the `openssl` command.

    ```
    openssl req -newkey rsa:2048 -keyout PRIVATEKEY.key -out MYCSR.csr
    ```

2.  Send your CSR \(MYCSR.csr in the example above\) to your certificate authority to have it signed.

3.  Create a P12 keystore for import using the `openssl` command.

    ```
    openssl pkcs12 -export -in MYSIGNEDCERT.pem -inkey PRIVATEKEY.key -name shared > MY_SERVER.p12
    ```

4.  Store your certificate and private key into a jceks file.

    ```
    keytool -importkeystore -destkeystore keystore.jceks -deststoretype jceks -srckeystore MY_SERVER.p12 -srcstoretype pkcs12 -alias MYALIAS
    ```

    The alias, shown in the example as `MYALIAS` can be any value. You will use this alias in the `edgeencryption.proxy.https.cert.alias` property in the `edgeencryption.properties` file located in the `<installation directory>/conf/` folder.

5.  Stop and restart the edge proxy.

    **Note:** During a restart, the proxy server is offline for a short time. The amount of time is determined by your environment and how long it takes to stop and restart the proxy service.


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Create and configure the RSA key pair for the digital signature](t_SetUpAKeyPair.md)

**Next topic:**[Set up a keystore and encryption keys](set-up-keystore.md)


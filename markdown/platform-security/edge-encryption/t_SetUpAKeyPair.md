---
title: Create and configure the RSA key pair for the digital signature
description: Create an RSA key pair that the proxy server can use to create the digital signature for signing changes to the encryption properties and configuration.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Create and configure the RSA key pair for the digital signature

Create an RSA key pair that the proxy server can use to create the digital signature for signing changes to the encryption properties and configuration.

## Before you begin

Role required: admin

To generate and validate the digital signature, an RSA key pair must be generated and stored in the JCEKS Java KeyStore and each proxy must be configured to use this key pair. Generate an encryption key pair using the keytool command.

To use the keytool utility with a proxy installed on SElinux \(CentOS\), you must enable loading of shared libraries from the proxy java-installation directory. To do this, run the following command as root.

```
chcon -R -t texrel_shlib_t proxy_install_dir/java/jre /lib
```

You must use the Java 1.8 version of the keytool utility. A copy of the utility can be found in `<proxy install dir>java/jre/bin/keytool`.

## Procedure

1.  Change to the KeyStore directory in the proxy download directory.

2.  Change the default password.

    The default password is **changeme**.

    ```
    keytool -keystore keystore.jceks -storetype jceks -storepasswd -new <newpassword>
    ```

3.  Create an encryption key pair.

    **Note:** Do not enter a password for the key when the keytool utility prompts for one.

    Enter this command on a single line.

    ```
    keytool -genkeypair -alias <key alias> -keyalg rsa -keystore keystore.jceks 
    -storetype jceks -storepass <keystore password> -keysize 2048
    ```

4.  Update the encryption proxy property file \(`edgeencryption.properties`\).

    1.  Change to the `<installation directory>/conf/` directory.

    2.  Open the `edgeencryption.properties` file.

    3.  Enter the properties for the [digital signature](../reference/edge-encryption-proxy-server-properties.md).

        These properties must be the same for all proxies.

5.  Save and close the `edgeencryption.properties` file.


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Install the Edge Encryption proxy server \(command line installer\)](install-edge-linux-windows.md)

**Next topic:**[Import and configure the certificate for secure SSL connection](t_SetUpSecureSSLConnection.md)


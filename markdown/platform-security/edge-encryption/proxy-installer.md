---
title: Install the Edge Encryption proxy server using the interactive installer
description: Install the Edge Encryption proxy server on a Windows or Linux computer using the interactive installer.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Install the Edge Encryption proxy server using the interactive installer

Install the Edge Encryption proxy server on a Windows or Linux computer using the interactive installer.

## Before you begin

**Note:** SafeNet KeySecure keystore files are not supported by the Edge Encryption installer. To use a SafeNet KeySecure keystore, [Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md).

The Edge Encryption plugin must be installed and activated on your instance before you start this procedure. Ensure that Java version 11.0.6 or later is installed on the machine running the Edge Encryption installer.

Role required:

-   security\_admin on your ServiceNow instance
-   local or domain administrator on a Windows host
-   service user with full file system access on a Linux host

## About this task

After installing a new proxy server, you can run the installer again to perform tests to detect issues with an installation or modify current settings. Your options include:

-   **Install New**: Install a new proxy server.
-   **Verify Installation**: Perform tests to detect and fix issues in a previous installation.
-   **Reinstall Existing**: Perform tests to detect and fix issues in a previous installation and view or modify existing settings.

**Note:** If installing the proxy server on a Linux machine on a privileged port \(port 80 or 443\), you must run the installer as a root user with full file system access. To restrict file system access after the proxy server is installed, you can use the SetUID feature in the proxy installer. To enable this feature, start the installer as root or sudo root. When prompted by the installer, provide the username and usergroup of an unprivileged user. The proxy server will install with file system privileges of the given user. You can skip this step to continue the default installation with root privileges.

## Procedure

1.  Use the installer to install multiple proxies for your instance on multiple machines, ensuring that the following criteria apply:

    -   All proxies must have the same encryption keys and the same RSA key pair used to digitally sign encryption configurations and rules.
    -   The encryption key must be the default key configured on the instance.
    -   When a proxy database is set up as part of the installation, all proxies must use the same proxy database.

        You may need a proxy database for equality-preserving encryption, order-preserving encryption, or tokenization. If you do not use any of these features, you do not need a proxy database.


## What to do next

To use NVDA, an Assistive Technology screen reader designed to read accessibility-enabled Java applications built for keyboard users, see [Configure a Windows 64-bit host to use 32-bit NVDA with Java applications](https://www.servicenow.com/docs/access?context=c_SetUpSect508ComplianceFeature&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

After installing the Edge Encryption proxy server, [Set the proxy server initial memory limit and upper bound memory limit](increase-memory.md).

1.  [Install the Edge Encryption proxy server \(interactive installer\)](install-proxy.md)  
Install the Edge Encryption proxy on a Windows or Linux computer.
2.  [Configure CyberArk properties protection](configure-cyberark-prop-protection.md)  
Optionally, configure CyberArk properties protection to securely store Edge Encryption passwords in a centralized and secure digital vault.
3.  [Configure the signature key](configure-sig-key.md)  
Configure the signature key after installing the proxy server through the Edge Encryption proxy installer.
4.  [Configure the HTTPS certificate](configure-cert.md)  
To enable clients to connect to the Edge Encryption proxy server using a secure SSL connection, import the HTTPS certificate to the proxy server.
5.  [Configure the AES 128-bit encryption key](configure-128-key.md)  
After you configure the HTTPS certificate through the Edge Encryption proxy installer, configure the AES 128-bit encryption key to encrypt your data.
6.  [Configure the AES 256-bit encryption key](configure-256-key.md)  
After you configure the AES 128-bit key through the Edge proxy installer, you can optionally configure an AES 256-bit encryption key to encrypt your data.
7.  [Update SSL certificate](update-ssl-certificate.md)  
When updating an SSL certificate on an Edge proxy server, you must delete the old one.
8.  [Configure the Edge Encryption proxy database](configure-proxy-db.md)  
If using order-preserving encryption types or encryption patterns, you can optionally configure the Edge Encryption proxy database properties.
9.  [Launch the Edge Encryption proxy server](launch-proxy.md)  
After an Edge Encryption proxy is installed and configured, you can start the proxy from the installer.
10. [Verify and troubleshoot the Edge Encryption proxy server installation](verify-install.md)  
After your Edge Encryption proxy is installed, you can verify the installation to locate problems or start and stop the proxy.

**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)


---
title: Configure CyberArk properties protection
description: Optionally, configure CyberArk properties protection to securely store Edge Encryption passwords in a centralized and secure digital vault.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure CyberArk properties protection

Optionally, configure CyberArk properties protection to securely store Edge Encryption passwords in a centralized and secure digital vault.

## Before you begin

Role required: admin

## About this task

You must purchase and configure CyberArk AIM \(Application Identity Management\) before you can configure CyberArk connection parameters and protected credentials for a proxy server. As part of the installation of the AIM client, the `JavaPasswordSDK.jar` file is installed in the AIM client installation directory. The CyberArk vault is installed on an independent hardened server, and the AIM clients allow secure access to that server.

**Note:** You must install the CyberArk AIM client on every host computer where an Edge proxy is installed.

In the Edge installer, you must specify the location of the `JavaPasswordSDK.jar` file to set up the CyberArk connection to the Edge proxy. You must also enter other values you defined during the AIM client installation.

Setting up CyberArk password storage is optional. If you do not want to set up CyberArk password storage, click **Skip** through the CyberArk screens.

## Procedure

1.  On the CyberArk Connection page of the Edge Encryption installer, enter the CyberArk connection parameters.

    |Setting|Description|
    |-------|-----------|
    |Path to PasswordSDK.jar|The path to the `JavaPasswordSDK.jar` file installed on the host Windows machine during CyberArk configuration.|
    |App ID|The **App ID** entered during CyberArk configuration.|
    |Safe Name|The **Safe Name** entered during CyberArk configuration.|

2.  Click **Next**.

3.  On the CyberArk Protected Credentials page of the installer, enter the credentials to be protected by CyberArk.

    -   To use a single credential name for all protected passwords, select the **Apply one Credential Name to all Credentials** check box, enter the credential name, and click **Apply**.
    -   Enter the credential name for one or more of the following fields. Credential names are the usernames entered for the SSH keys during CyberArk configuration.
    |Setting|Description|
    |-------|-----------|
    |Edge Encryption User|The CyberArk credential name for an Edge Encryption user.|
    |Signature Key Keystore|The CyberArk credential name for the signature key keystore.|
    |HTTPS Cert Keystore|The CyberArk credential name for the HTTPS certification keystore.|
    |Encryption Key Keystore|The CyberArk credential name for the encryption key keystore.|
    |Database|The CyberArk credential name for the database keystore.|
    |SafeNet HTTPS Cert Keystore|The CyberArk credential name for the SafeNet HTTPS certification keystore.|
    |SafeNet Server|The CyberArk credential name for the SafeNet server.|
    |Forward Proxy|The CyberArk credential name for the forward proxy.|

4.  Click **Next**.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Previous topic:**[Install the Edge Encryption proxy server \(interactive installer\)](install-proxy.md)

**Next topic:**[Configure the signature key](configure-sig-key.md)


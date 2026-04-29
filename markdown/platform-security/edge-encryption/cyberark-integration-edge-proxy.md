---
title: CyberArk integration with the Edge proxy server
description: Use CyberArk to store passwords in a centralized and secure digital vault to secure passwords that were previously stored in clear text and secured by file access, or that were previously encrypted via a second file.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# CyberArk integration with the Edge proxy server

Use CyberArk to store passwords in a centralized and secure digital vault to secure passwords that were previously stored in clear text and secured by file access, or that were previously encrypted via a second file.

CyberArk AIM \(Application Identity Management\) prevents unauthorized access by eliminating hard-coded and visible passwords. AIM stores passwords in a digital vault on an independent hardened server, where the passwords are represented as digital credentials. The AIM clients \(the Edge proxy servers\) use CyberArk digital credentials and access the independent server to retrieve the secured passwords. No passwords are stored on the Edge proxy servers or in the instance.

## CyberArk digital vault credentials

You must purchase and configure CyberArk before you can set up CyberArk integration with the Edge proxy server.

To add a credential to CyberArk \(which is read by the Edge proxy\), set the **Platform Name** of the credential to **Unix via SSH** and make sure you either create a **Custom** credential **Name** or write down the **Auto-generated** credential **Name**. When you configure the Edge proxy to use this credential, the proxy server matches this credential **Name** to the setting in the proxy.



Each credential entry holds a **Password** that is being secured, as well as a credential **Name** used by an application to access that password.

**Note:** CyberArk credentials are not encryption keys.

## Adding CyberArk during an Edge proxy installation

The proxy installer includes a new configuration page for a CyberArk integration. This page is optional if you do not want to include CyberArk when installing your proxy with the proxy installer. You can also manually set up and configure CyberArk integration in the configuration file.

The proxy installer also includes a new page for CyberArk protected credentials. This page allows configurations of different properties using a single credential name or multiple credential names. This page is optional if you do not want to include CyberArk when installing your proxy with the proxy installer.

## CyberArk password protection

Any password field in the Edge proxy installer that has a CyberArk credential configured in the CyberArk vault and specified on the CyberArk Protected Credentials page of the installer is grayed out and contains the message `Protected by CyberArk`.

**Parent Topic:**[Installing Edge Encryption](c_InstallEdgeEncryptionProxy.md)


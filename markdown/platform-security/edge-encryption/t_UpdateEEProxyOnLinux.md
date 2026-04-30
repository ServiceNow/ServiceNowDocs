---
title: Manually upgrade an Edge Encryption proxy server running on Linux
description: Update a proxy running on Linux.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Upgrading Edge Encryption, Edge Encryption, Encryption]
---

# Manually upgrade an Edge Encryption proxy server running on Linux

Update a proxy running on Linux.

## Before you begin

If using AES 256-bit encryption with Java 8 update 141 \(8u141\) or lower, you must install the Java Cryptography Extension \(JCE\) jurisdiction policy files by copying them into the system Java home directory of each Edge Encryption proxy server host. Add these files to the `<Java-home-directory>/jre/lib/security` folder before performing a scheduled or manual upgrade. To install the AES 256-bit encryption policy files, see [Configure the AES 256-bit encryption key](configure-256-key.md).

Role required: security\_admin or local administrator on the host machine

## Procedure

1.  Download the Edge Encryption proxy-update archive file to the installation directory.

    1.  Navigate to **Edge Encryption Configuration** &gt; **Installation &amp; Downloads** &gt; **Downloads**

    2.  Select the **Download the command line installer** link.

    3.  When the download begins, select the your installation directory as the download location.

2.  Change to the installation directory.

3.  Run the following command:

    `java -jar edgeencryption-dist-<version>-linux-x86-64.jar -m dist-upgrade -c <proxy directory>`

    |Option|Description|
    |------|-----------|
    |proxy directory|The directory in the installation directory where the proxy was initially installed. This directory is created by the install.|

    If you want to see the help screen, execute this command without arguments: `java -jar edgeencryption-dist-<version>-linux-x86-64.jar`

    A new proxy directory is created with a current timestamp. A backup of the old proxy directory is maintained as backup.dist-upgrade\_timestamp in the new proxy installation directory. The old proxy shuts down and the new proxy starts up. Any open connections/transactions on the old proxy server are terminated.

4.  Check the proxy log in the new directory and the instance to verify that the new proxy is running.


**Parent Topic:**[Upgrading Edge Encryption](../concept/c_UpdateEdgeEncryptionProxy.md)


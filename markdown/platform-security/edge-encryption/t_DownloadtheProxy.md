---
title: Download the Edge Encryption proxy server
description: Download the Edge Encryption proxy server application from your instance, and then copy the file to each computer that is to run the Edge Encryption proxy server.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Download the Edge Encryption proxy server

Download the Edge Encryption proxy server application from your instance, and then copy the file to each computer that is to run the Edge Encryption proxy server.

## Before you begin

Before starting this procedure, the Edge Encryption plugin must be installed and activated on your instance.

**Note:** The Edge Encryption proxy is officially supported only on Oracle JRE.

Role required: security\_admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Installation &amp; Downloads** &gt; **Downloads**.

2.  To use the interactive installer, click **Download Interactive Installer**.

    If manually installing the proxy server, select the OS version for your proxy server.

    ![Edge Encryption proxy server download options](../images/edge-proxy-downloads.png)

    **Note:** Because the proxy server requires at least 4 GB of memory to run, 32-bit JREs and 32-bit operating systems are no longer supported starting with the Washington DC release.

3.  Copy the installer to each computer that is to run the Edge Encryption proxy server.

    **Note:** If you are manually installing the Edge Encryption proxy server, copy the ZIP file to each computer that is to run the Edge Encryption proxy server.


## What to do next

After downloading the Edge Encryption installer, [Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md). If installing manually, [Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md).

**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)


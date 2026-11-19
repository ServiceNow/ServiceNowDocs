---
title: Download the Edge Encryption proxy server
description: Download the Edge Encryption proxy server application from your instance, and then copy the file to each computer that is to run the Edge Encryption proxy server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/edge-encryption/t\_DownloadtheProxy.html
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
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

    \[Omitted image "edge-proxy-downloads.png"\] Alt text: Edge Encryption proxy server download options

    **Note:** Because the proxy server requires at least 4 GB of memory to run, 32-bit JREs and 32-bit operating systems are no longer supported starting with the Washington DC release.

3.  Copy the installer to each computer that is to run the Edge Encryption proxy server.

    **Note:** If you are manually installing the Edge Encryption proxy server, copy the ZIP file to each computer that is to run the Edge Encryption proxy server.


## What to do next

After downloading the Edge Encryption installer, [Install the Edge Encryption proxy server using the interactive installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/proxy-installer.md). If installing manually, [Install the Edge Encryption proxy server using the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/manual-proxy-install.md).

**Parent Topic:**[Installing Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/c_InstallEdgeEncryptionProxy.md)


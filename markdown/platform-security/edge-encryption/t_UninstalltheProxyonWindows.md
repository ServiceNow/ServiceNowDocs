---
title: Uninstall the Edge Encryption proxy on Windows
description: You can uninstall the Edge Encryption proxy. If you are upgrading the proxy, it is not necessary to shut down and uninstall the current version.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Uninstall the Edge Encryption proxy on Windows

You can uninstall the Edge Encryption proxy. If you are upgrading the proxy, it is not necessary to shut down and uninstall the current version.

## Before you begin

Role required: admin

You must have access to the computer running the Edge Encryption proxy.

Before shutting down the Edge Encryption proxy, ensure that no users are connected to the instance using the proxy.

## Procedure

1.  You may want to save the `edgeencryption.properties` file before deleting the distribution directory.

2.  Execute `edgeencryption.bat stop`

3.  Execute `edgeencryption.bat remove`

4.  Check the log on the proxy server to verify that the proxy server is shutdown.

5.  Delete the files in the distribution folder.


**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)


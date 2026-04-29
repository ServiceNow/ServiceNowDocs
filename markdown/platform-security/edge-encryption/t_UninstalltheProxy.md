---
title: Uninstall the Edge Encryption proxy on Linux
description: You can uninstall the Edge Encryption proxy. If you are upgrading the proxy, it is not necessary to shut down and uninstall the current version.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Uninstall the Edge Encryption proxy on Linux

You can uninstall the Edge Encryption proxy. If you are upgrading the proxy, it is not necessary to shut down and uninstall the current version.

## Before you begin

Role required: admin

You must have access to the computer running the Edge Encryption proxy.

## About this task

Before shutting down the Edge Encryption proxy, ensure that no users are connected to the instance using the proxy.

The encryption proxy running on Linux operates as a single process. You can end this process to accommodate such tasks as redeploying the encryption proxy to another host machine, updating the proxy version, updating the Java version, or changing the unique name of the encryption proxy when deploying the encryption proxy on multiple proxy servers.

## Procedure

1.  You may want to save the `edgeencryption.properties` file before deleting the distribution directory.

2.  Execute the `shutdown.sh` shell script.

3.  Check the log on the proxy server to verify that the proxy server is shut down.

4.  Delete the files in the distribution folder.


**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)


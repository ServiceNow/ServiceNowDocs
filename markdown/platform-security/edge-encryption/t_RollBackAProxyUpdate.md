---
title: Roll back an Edge Encryption proxy server upgrade
description: If a proxy upgrade is unsuccessful, you can go back to the earlier version.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Upgrading Edge Encryption, Edge Encryption, Encryption]
---

# Roll back an Edge Encryption proxy server upgrade

If a proxy upgrade is unsuccessful, you can go back to the earlier version.

## Before you begin

Role required: admin

## About this task

If an upgrade fails when using the scheduled upgrade feature in the Australia release, the proxy server will automatically roll back to the old version. The old proxy server is stored unmodified in a backup directory.

If you would like to roll back a manual upgrade, you can follow these steps.

## Procedure

1.  Shut down the proxy.

2.  Delete the new proxy directory.

3.  Rename the backup directory to the proxy name.

    The backup directory is in the proxy installation directory with the name `<proxy name>_backup`

4.  Start the proxy.

5.  Check the proxy log and the instance to verify that the proxy is online.


**Parent Topic:**[Upgrading Edge Encryption](../concept/c_UpdateEdgeEncryptionProxy.md)


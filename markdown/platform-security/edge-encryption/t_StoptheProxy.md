---
title: Stop the Edge Encryption proxy
description: You can stop an Edge Encryption proxy from the command line.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Stop the Edge Encryption proxy

You can stop an Edge Encryption proxy from the command line.

## Before you begin

Role required: admin

## Procedure

1.  Stop the proxy server.

<table id="choicetable_nfz_zhb_tt"><tbody><tr><td id="d126454e72">

**On a Linux machine**

</td><td>

Execute `./shutdown.sh`

</td></tr><tr><td id="d126454e84">

**On a Windows machine**

</td><td>

Execute `edgeencryption.bat stop`

 To remove the Windows service, execute `edgeencryption.bat remove`

</td></tr></tbody>
</table>2.  Check the log on the proxy server to verify that the proxy has stopped.


**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)


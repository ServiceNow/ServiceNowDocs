---
title: Schedule an Edge Encryption proxy server upgrade
description: Create an upgrade schedule to enable the instance to upgrade an out-of-date proxy server.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Upgrading Edge Encryption, Edge Encryption, Encryption]
---

# Schedule an Edge Encryption proxy server upgrade

Create an upgrade schedule to enable the instance to upgrade an out-of-date proxy server.

## Before you begin

To schedule an upgrade, you must be logged in to your instance through the proxy server.

If using AES 256-bit encryption with Java 8 update 141 \(8u141\) or lower, you must install the Java Cryptography Extension \(JCE\) jurisdiction policy files by copying them into the system Java home directory of each Edge Encryption proxy server host. Add these files to the `<Java-home-directory>/jre/lib/security` folder before performing a scheduled or manual upgrade. To install the AES 256-bit encryption policy files, see [Configure the AES 256-bit encryption key](configure-256-key.md).

Role required: security\_admin

## About this task

Once the upgrade is scheduled, the proxy server automatically upgrades at the scheduled time. During the upgrade, the proxy server is offline for only a short time.

**Note:** Because the proxy server restarts during the upgrade, it is offline for a short time. The amount of time is determined by your environment and how long it takes to stop and restart the proxy service.

During the scheduled upgrade, a new proxy directory is created and your configuration files are copied to the new directory. New properties are written to your existing properties file. The following files or directories in your old proxy directory are copied to the new proxy directory.

-   `/conf` directory
-   `/keys` directory
-   `/keystore` directory
-   `java/jre/lib/security/cacerts` file

As a result, your keys, keystores, settings, and certificates are preserved.

**Note:** Only the above files are copied to the new proxy directory. Any other customized files in the proxy server directory will not be preserved during a scheduled upgrade. The upgrade log file can be found in the original proxy directory in the following folder: `<original-proxy-directory>/tmp/upgrade-wrapper/bin`.

If multiple proxy servers are out-of-date, you must schedule an upgrade for each proxy server individually.

**Note:** Avoid hosting multiple proxy servers on the same machine. However, if your environment includes this configuration, do not schedule upgrades to multiple proxies on the same machine at the same time.

## Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Proxies** &gt; **Upgrade Schedules**.

2.  Click **New**.

3.  Complete the form.

<table id="table_gqp_d52_3z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Proxy server

</td><td>

Proxy server being upgraded.

</td></tr><tr><td>

Target version

</td><td>

Version to which you are upgrading your proxy server. This value is read-only and set to the most up-to-date proxy version available for your instance.

</td></tr><tr><td>

Scheduled Start Time

</td><td>

Date and time on which to start the upgrade.

</td></tr><tr><td>

Active

</td><td>

Whether the scheduled upgrade is active. If this field is not selected, the upgrade will not perform on the scheduled date and time.

</td></tr><tr><td>

Status

</td><td>

The status of the upgrade. This value is read-only. Possible statuses include:-   Pending
-   Running
-   Complete
-   Failed


</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

The typical time for an upgrade is less that 15 minutes. After an upgrade is executed, you can review the upgrade details to learn more about it. If your upgrade failed, review the **Failure Reason** to determine next steps.

|Field|Description|
|-----|-----------|
|From Version|The version that the server was upgraded from.|
|To Version|The version that the server was upgraded to.|
|Actual Start Time|Time that the upgrade began.|
|End Time|Time that the upgrade ended.|
|Failure Reason|Reason that the upgrade failed.|

**Parent Topic:**[Upgrading Edge Encryption](../concept/c_UpdateEdgeEncryptionProxy.md)


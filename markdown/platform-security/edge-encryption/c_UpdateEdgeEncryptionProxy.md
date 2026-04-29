---
title: Upgrading Edge Encryption
description: Both instance upgrades and proxy server upgrades require special consideration in an Edge Encryption environment.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Edge Encryption, Encryption]
---

# Upgrading Edge Encryption

Both instance upgrades and proxy server upgrades require special consideration in an Edge Encryption environment.

## Instance upgrades

Instance upgrades in an Edge Encryption environment require caution to ensure that Edge controls work properly after the instance upgrade.

During an instance upgrade, you should not add, edit, or delete the following:

-   Edge Encryption configurations
-   Edge Encryption rules
-   Edge Encryption tokenization patterns
-   Edge Encryption scheduled jobs
-   Edge Encryption key configurations
-   Edge Encryption scheduled upgrades
-   Edge Encryption denylist IP configurations

Any scheduled job running during the instance upgrade will not complete. To complete the interrupted job, rerun the job once the instance is upgraded. When you reschedule the job, the processing that occurred before the instance upgrade is not lost, and the job continues to process only the data that has not yet been processed.

## Proxy server upgrades

Schedule a proxy upgrade to enable the instance to upgrade the Edge Encryption proxy server, or manually upgrade the proxy server at any time.

**Warning:** For an upgrade on Windows, you may encounter file lock issues and the upgrade may fail. For the upgrade to succeed, you should not have any files open under the installation directory. Also, there should be no existing shell in the installation directory. In particular, if you start the proxy from the command line \(via `bin\edgeencryption.bat install/start`\) while in the installation directory, you should close that shell or move it out of the installation directory afterward. No files under the installation directory should be opened by an editor or by any other application.

## Third party libraries

Third party libraries, such as Gemalto, are lost during instance and proxy server upgrades if they are kept in the same directory. You can perform the following to prevent the loss of third party libraries during upgrades:

1.  Manually add the following property to edgeencryption.properties:

    `edgeencryption.ekm.provider.classname = com.snc.edgeencryption.encryption.CloudEdgeNaeKeyProvider`

2.  Add the **edgeencryption.thirdparty.vendor.library.path** vendor library location property and set it to `/path/to/jars`.

    For example:

    `edgeencryption.thirdparty.vendor.library.path = /app/servicenow/libs`

3.  Copy the SafeNet JARs into that path.

After you install the third party libraries outside of the Edge Encryption installation, they are no longer lost during upgrades.

## Scheduled upgrades

**Important:** During ServiceNow Instance upgrades, also upgrade your proxy server version to align with your Instance version and reduce the chance of compatibility issues.

Schedule an upgrade to allow the instance to upgrade the proxy server at the scheduled time. This functionality is available by default after upgrading. A scheduled upgrade includes these events:

1.  The proxy server checks with the instance to see if there is a new version available for upgrade. New versions generally become available when the instance is upgraded.
2.  The administrator receives a notification upon logging in when a new version of the proxy server is available.
3.  The administrator can [Schedule an Edge Encryption proxy server upgrade](../task/schedule-proxy-upgrade.md) for each proxy server.

    **Note:** Only users with the security\_admin role can create an upgrade schedule through the proxy server.

4.  Once the upgrade is scheduled, the proxy server automatically upgrades at the scheduled time. During the upgrade, the proxy server is offline for only a short time.

    **Note:** Because the proxy server restarts during the upgrade, it is offline for a short time. The amount of time is determined by your environment and how long it takes to stop and restart the proxy service.

5.  During the scheduled upgrade, a new proxy directory is created and your configuration files are copied to the new directory. New properties are written to your existing properties file. The following files or directories in your old proxy directory are copied to the new proxy directory.

    -   `/conf` directory
    -   `/keys` directory
    -   `/keystore` directory
    -   `java/jre/lib/security/cacerts` file
    As a result, your keys, keystores, settings, and certificates are preserved.

    **Note:** Only the above files are copied to the new proxy directory. Any other customized files in the proxy server directory are not preserved during a scheduled upgrade. The upgrade log file can be found in the original proxy directory in the following folder: `<original-proxy-directory>/tmp/upgrade-wrapper/bin`.


## Prerequisites for scheduled upgrades

Before scheduling an upgrade for an Edge Encryption proxy, ensure the following:

1.  The *JAVA\_HOME* environment variable points to a java installation on the machine that is outside the Edge Encryption proxy’s directory structure.
2.  The *JAVA\_HOME* environment variable points to a java installation that is at version 1.8\_u144 or higher.
3.  The **-Djava.io.tmpdir** parameter in the wrapper.conf file of the Edge Encryption proxy points to a directory that is OUTSIDE the Edge Encryption proxy’s directory structure, and the proxy has read/write/execute permissions on the directory. Optionally, you could comment out the parameter entirely so that Java uses its default tmp location.

## Manual upgrades

Instead of creating an upgrade schedule, you can manually upgrade each proxy server through the command line. See [Manually upgrade an Edge Encryption proxy server running on Linux](../task/t_UpdateEEProxyOnLinux.md) or [Manually upgrade an Edge Encryption proxy server running on Windows](../task/t_UpdateEEProxyOnWindows.md).

## Proxy build status

You can easily identify whether a proxy server is out of date by navigating to **Edge Encryption Configuration** &gt; **Proxies** &gt; **All**. The status of your proxy build is indicated in the **Proxy build** column by the following colors:

-   **Green**

    Your proxy server is up-to-date.

-   **Yellow**

    Your proxy server is out-of-date and an upgrade is needed.

-   **Orange**

    Upgrade failed. Your proxy server reverts to the old version to ensure that there is no downtime.


![](../images/proxy-build-status-green.png)

## Troubleshoot a failed scheduled proxy upgrade

When a scheduled proxy upgrade fails, the proxy server reverts to the version you are upgrading from. All original data, keys, and configuration files are preserved. This process may take several minutes. Contact Customer Service and Support to ensure a successful upgrade.

To determine the reason for the failure, you can check the **Failure Reason** in the upgrade schedule. In addition, the installation directory for the failed upgrade is maintained so that log files are available for troubleshooting.

**Note:** Before deleting any extra proxy directories, always confirm which directory is current by reviewing the log files. If the log files have recent activity, the proxy might be connected to your instance.

If a scheduled proxy upgrade fails repeatedly, you can manually upgrade your proxy server. See [Manually upgrade an Edge Encryption proxy server running on Linux](../task/t_UpdateEEProxyOnLinux.md) and [Manually upgrade an Edge Encryption proxy server running on Windows](../task/t_UpdateEEProxyOnWindows.md).

## Java minimum requirements

The host machine installing or running the Edge Encryption proxy server must maintain a supported version of Java. Current supported versions are Java 17.0.3 or later in the 17.x version series.

**Note:** Java 11 is no longer be supported as of the Yokohama release. Upgrade your environment with the Edge Encryption proxy to Java 17 before you attempt to install Yokohama or later versions of the Edge Encryption proxy.

If using AES 256-bit encryption with Java 8 update 141 \(8u141\) or lower, you must install the Java Cryptography Extension \(JCE\) jurisdiction policy files by copying them into the system Java home directory of each Edge Encryption proxy server host. Add these files to the `<Java-home-directory>/jre/lib/security` folder before performing a scheduled or manual upgrade. To install the AES 256-bit encryption policy files, see [Configure the AES 256-bit encryption key](../task/configure-256-key.md).

## Mixed proxy-version environments

Although an environment running old versions of the proxy server with up-to-date versions of the proxy server is not recommended, it is supported if all proxy servers are within the same version family as your instance. For example, if you have an instance on the Australia release, your environment supports proxy servers from any Australia patch or hot fix. However, the following limitations apply.

-   If one proxy server supports functionality that another proxy does not support, you will see inconsistent behavior, depending on which proxy server is used.
-   If a proxy server is out-of-date, it may not include recent security enhancements.

If a proxy server from a previous release is registered with a newer release of the instance, you will receive regular notifications that the proxy server is out-of-date. To ensure an optimal and secure environment, ServiceNow recommends always upgrading your proxy server to the most recent version of the software supported by your instance.

-   **[Schedule an Edge Encryption proxy server upgrade](../task/schedule-proxy-upgrade.md)**  
Create an upgrade schedule to enable the instance to upgrade an out-of-date proxy server.
-   **[Manually upgrade an Edge Encryption proxy server running on Linux](../task/t_UpdateEEProxyOnLinux.md)**  
Update a proxy running on Linux.
-   **[Manually upgrade an Edge Encryption proxy server running on Windows](../task/t_UpdateEEProxyOnWindows.md)**  
Update a proxy running on Windows.
-   **[Roll back an Edge Encryption proxy server upgrade](../task/t_RollBackAProxyUpdate.md)**  
If a proxy upgrade is unsuccessful, you can go back to the earlier version.

**Parent Topic:**[Edge Encryption](../reference/edge-encryption.md)


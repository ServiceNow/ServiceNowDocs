---
title: Download the MID Server files
description: Download the MID Server installer package through the instance and make it available for installation on the host. Allow the local network to access the authorized IP addresses to ensure that you can download the installation package and receive automatic upgrades.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Download the MID Server files

Download the MID Server installer package through the instance and make it available for installation on the host. Allow the local network to access the authorized IP addresses to ensure that you can download the installation package and receive automatic upgrades.

## Before you begin

Role required: admin

<table id="table_ehc_1s4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>## About this task

The IP address of the MID Server download site \(`install.service-now.com`\) can change without notice. To ensure that you can download the MID Server installation package and receive automatic MID Server upgrades, allow local network access to these IP addresses:

-   149.96.5.98
-   149.96.6.98

A maint user can change the MID Server download site URL with the MID Server system property **mid.install\_server.base\_uri**. The MID Server downloads the update files from the new URL instead. Users with closed environments can direct MID Servers to update through hosts in their environment. See [MID Server properties](../reference/r_MIDServerProperties.md#) and [\[KB1546609\] Configure Custom MID server Upgrade URL](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1546609) for more information.

**Note:** Download the MID Server first and then enable Discovery, Orchestration, or any integration that requires the use of the MID Server.

## Procedure

1.  On the ServiceNow instance, navigate to **Mid Server** &gt; **Downloads**.

2.  Select and download the MID Server for the appropriate operating system.

    For the best performance, install the 64-bit MID Server for your operating system.

    **Note:** ServiceNow no longer supports new installations of 32-bit MID Servers or upgrades to version Rome. New MID Server installation are blocked through RPM and MSI installer on the following operating systems:

    -   CentOS 7
    -   Windows server 2008
    -   Windows server 2008 R2
    -   Windows 8
    -   Windows 10
    MID Servers can be manually installed to any operating system with the ZIP file, however Windows 10 is unsupported. Unsupported MID Servers auto-upgrading to Rome create an issue record in MID Server Issues \(ecc\_agent\_issue\). For more information, see [Supported platform changes for MID Server \[KB0863694\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863694).

    ![MID Server downloads](../image/MIDServerDownloadMatrix.png "MID Server downloads")

3.  Save the download file to a temporary file on the local drive.

4.  Move the file into the designated MID Server folder you create for your operating system and run the installer from that location.


## What to do next

You can manually verify the signature of an installation package with the jarsigner tool to ensure its authenticity. For more information about verifying the signature, see the [MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md) section on manual verification.

Install the MID Server on the host computer.

-   [Linux](t_InstallAMIDServerOnLinux.md#)
-   [Windows](../concept/mid-server-install-prereqs.md#)


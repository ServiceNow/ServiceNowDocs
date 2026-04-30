---
title: Synchronize a JAR file to MID Servers
description: You can upload a JAR file to an instance and synchronize it to all MID Servers, or write custom probes that use the synchronized JAR file.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Synchronize a JAR file to MID Servers

You can upload a JAR file to an instance and synchronize it to all MID Servers, or write custom probes that use the synchronized JAR file.

## Before you begin

Role required: admin, agent\_admin

<table id="table_hpn_4t4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>The MID Server JAR File \[ecc\_agent\_jar\] table is domain separated. You can create versions of these policies that only a MID Server from the same domain can use. For instructions, see [Set up domain separation for MID servers](../concept/c_MIDServerDomainSeparation.md#).

**Warning:** Synchronizing a JAR file with this procedure causes all MID Servers connected to the instance to restart automatically.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **JAR Files**.

2.  Click **New**.

3.  Complete the following fields:

    -   **Name:**A unique and descriptive name for identifying the file in the instance.
    -   **Version:** A version number for the file, if one is available.
    -   **Source:** Location of the JAR file for reference purposes. Source information is not used by the system.
    -   **Description:** Short description of the JAR file and its purpose in the instance.
4.  Click the paper clip icon in the banner.

    ![paper clip icon](../image/JARFileSync.png)

5.  In the Attachments dialog box, click **Browse** and select the file you want to attach.

    The platform attaches the JAR file to the record and restarts the MID Servers to synchronize the file. It is not necessary to update the record to attach the file.


**Parent Topic:**[Configuring MID Servers](../concept/c_MIDServerConfiguration.md)


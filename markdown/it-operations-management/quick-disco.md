---
title: Run a Quick Discovery
description: Scan one or more IP addresses to discover devices in your network without creating ongoing schedules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 2
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console for Discovery, Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Run a Quick Discovery

Scan one or more IP addresses to discover devices in your network without creating ongoing schedules.

## Before you begin

Verify the following:

-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Now Assist for Setup](install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](install-now-assist-itom.md).
-   You have at least one MID Server that is validated and in an **UP** state. The MID Server must be able to reach the IP ranges that you want to discover. For more information, see [Validate a MID Server](validate-mid-server.md).
-   You have configured the credentials needed to access devices in your target IP ranges. For more information, see [Create IP credentials](create-ip-credentials.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](access-itom-config-console-disco.md).

Role required: discovery\_admin

## About this task

Use quick discovery to run an on-demand, IP-based discovery without configuring a full Discovery schedule. Quick discovery is useful for verifying that Discovery can reach and identify devices before you set up recurring schedules.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Discovery Setup**.

2.  Select **Quick Discovery**.

3.  In the **Enter IP list** field, enter the IPv4 addresses that you want to discover.

    You can enter IP addresses in the following formats.

    |Format|Example|
    |------|-------|
    |IP network addresses|`10.0.1.0/24`|
    |IP address range|`10.0.2.1-10.0.2.15`|
    |Comma-separated IP addresses|`10.0.3.176,10.0.3.222,2001::100,2600:1bdc::fffe`|

    **Note:** You can combine multiple formats in a single comma-separated entry.

4.  From the **MID selection method** drop-down list, select how to assign a MID Server for the discovery.

    The following MID Server selection methods are available.

    |Option|Description|
    |------|-----------|
    |**Auto-select MID Server**|Discovery automatically selects an appropriate MID Server to run the discovery.|
    |**Specific MID Server**|Select a specific MID Server from the list. Only MID Servers that are validated and in an **Up** state are available.|
    |**Specific MID cluster**|Select a MID Server cluster. Clusters provide failover protection and load balancing between MID Servers.|

5.  Select **Run discovery**.

    Discovery scans the specified IP addresses and identifies devices in your network.

6.  To complete the setup, select **Mark as configured**.


**Related topics**  


[Get started with credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-getting-started.md)


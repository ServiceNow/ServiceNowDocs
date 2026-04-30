---
title: MID Server selection sequence for Discovery schedules
description: The Discovery application follows this sequence to find a MID Server.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Schedule a horizontal discovery, Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# MID Server selection sequence for Discovery schedules

The Discovery application follows this sequence to find a MID Server.

## MID Server auto-selection

Discovery follows this sequence when you select **Auto-Select MID Server** for the **MID Server selection method** on the Discovery Schedule form.

**Note:** MID Server auto-select is not supported with IPv6.

1.  Discovery looks for a MID Server that also has an appropriate IP range configured.
2.  If no MID Servers meet these criteria, it looks for a MID Server that has the **ALL** application that also has an appropriate IP range configured.
3.  If more than one MID Server meet the criteria, Discovery chooses the first MID Server with the status of **Up**. If more than one MID Server is up, it randomly picks one.
4.  If none are up, it uses the default MID Server specified for the Discovery application, assuming it is up.
5.  If no default MID Server is specified, it uses the default MID Server specified for the **ALL** application, assuming it is up.
6.  If no default MID Server is specified, Discovery cycles through the previous steps and looks for MID Servers with the status of **Paused** or **Upgrading**.

    **Note:** When a MID Server is paused or upgrading, it does not actually process commands until it returns to the status of **Up**.


## MID Server clusters

These steps are followed when you select **Specific MID Cluster** for the **MID Server selection method** on the **Discovery** form, and the cluster is a load balancing cluster:

1.  **Discovery** uses the first MID Server in the cluster that it finds with the status of **Up**.
2.  If more than one MID Server is up, it randomly picks one. If it cannot find any MID Servers, it looks for MID Servers in the cluster with the status of **Paused** or **Upgrading**.

These steps are followed when the cluster is a failover cluster:

1.  **Discovery** uses the MID Server with the lowest **Order** value that also has the status of **Up**.
2.  If no MID Servers are found, it looks for MID Servers in the cluster with the status of **Paused** or **Upgrading**, choosing the one with the lowest **Order** value.

**Note:** **Discovery** ignores the default MID Server for it and **ALL** applications when selecting a MID Server from the cluster.

## Port scan \(Shazzam\) phase

During the port scan phase, Discovery collects all the target IP addresses. It splits them equally between MID Servers matching the criteria \(MID Servers are qualified to do the port scan\). The Shazzam batch size, which you configured on the Discovery schedule, determines the number of IP addresses that each Shazzam probe can scan. This phase helps determine how much work each MID Server does during the port scan phase.

For example, you have 16,000 IP addresses to scan among three qualified MID Servers, and you use the default Shazzam batch size of 5000. Two of the MID Servers handle 5000 IP address scans \(one Shazzam probe each\). The other MID Server handles 6000 IP address scans by launching two Shazzam probes.

**Note:**

Shazzam can process IP lists containing up to of 5000 addresses that include both IPv4 and IPv6 types. If your schedule contains an IP list with more than 5000 IPv6 IP addresses, the Discovery gets cancelled. If you are using only IPv6 addresses, you must use a list and not an IP address range. IPv6 address ranges and networks are not supported and will be ignored.

**Related topics**  


[MID Server pause](https://www.servicenow.com/docs/access?context=t_PauseTheMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&section=c_MIDServerPause&ft:locale=en-US)

[MID Server cluster configuration](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=yokohama&pubname=yokohama-servicenow-platform&section=mid-server-clusters&ft:locale=en-US)


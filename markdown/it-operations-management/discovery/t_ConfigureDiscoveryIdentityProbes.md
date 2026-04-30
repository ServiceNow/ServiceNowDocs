---
title: Configure Discovery identity probes
description: Identity probes are multi-probes, which contain one or more simple probes configured to extract specific information from manageable devices. You can create your own identity multi-probe to identify CIs that Discovery does not already identify.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Discovery identifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure Discovery identity probes

Identity probes are multi-probes, which contain one or more simple probes configured to extract specific information from manageable devices. You can create your own identity multi-probe to identify CIs that Discovery does not already identify.

## Before you begin

Role required: discovery\_admin or admin

## About this task

Identity probes return such information as device serial numbers \(there can be several per device\), the computer name, and network identification \(MAC address\). For example, the Linux - Identity multiprobe provided in the system, contains two simple SSH probes configured to return hardware and network information about the device. After the probe has discovered this information, it passes the data to a multisensor configured to process identity information.

**Note:** A multiprobe cannot contain another multiprobe.

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Probes**.

2.  Select a probe from the list whose **Class** is Multiprobe.

3.  Make sure the scope is set to **Global**.

4.  In the **Includes Probes** Related List, click **Edit** to select simple probes to include in this multiprobe.

5.  Click **New** to create a new simple probe.


## Example

![Discovery identity probes](../image/DiscoveryMultiprobeSelect.png "Discovery identity probes")

## What to do next

[Configure Discovery identity sensors](t_ConfigDiscoIdentSens.md) that are part of the identify probes.

**Parent Topic:**[Discovery identifiers](../concept/c_DiscoveryIdentifiers.md)


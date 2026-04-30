---
title: Configure Discovery identity sensors
description: If you customize an identify multi-probe, you can also configure a multi-sensor for it.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Discovery identifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure Discovery identity sensors

If you customize an identify multi-probe, you can also configure a multi-sensor for it.

## Before you begin

Role required: discovery\_admin or admin

## About this task

These multi-sensors pass the data returned by the identity probes to the Discovery identifiers. The identifiers then search the CMDB for matching CIs. When the identity of a device is resolved, the identifiers pass the result state for the device to the multi-sensors, which react accordingly, either by launching exploration probes or stopping Discovery for that device.

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Sensors**.

2.  Select an existing identity multi-sensors from the list.

    **Note:** To avoid confusion, the multi-sensors provided in the instance must have the same names as their matching multi-probes.

    The **Responds to Probes** related list shows the simple probes which pass their data to this multi-sensors. These are the same simple probes that appear in the Includes Probes list in the matching multi-probes record.

3.  Click the **Script** link for each probe in the list to see the script that the multi-sensors runs to process the data from the probe.


## Example

![Linux identity script](../image/DiscoveryMultisensorAndScript.png "Discovery identity sensors")

## What to do next

Run a discovery through the [Discovery Schedule](t_CreateADiscoverySchedule.md) to search for CIs and verify that they are identified correctly in the CMDB.

**Parent Topic:**[Discovery identifiers](../concept/c_DiscoveryIdentifiers.md)


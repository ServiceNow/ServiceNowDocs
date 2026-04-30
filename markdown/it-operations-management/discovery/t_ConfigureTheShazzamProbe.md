---
title: Configure Shazzam probe
description: When you run Discovery, the Shazzam probe finds your active network devices by scanning specified ports on specified IP address ranges. If the list of IP ranges being scanned is large, you can configure the Shazzam payload for JSON encoding to reduce its size.A system property converts Shazzam payloads into JSON strings, which dramatically reduces their size. This setting prevents nodes from running out of memory when a single schedule discovers large numbers of IP ranges.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Port probes, List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure Shazzam probe

When you run Discovery, the Shazzam probe finds your active network devices by scanning specified ports on specified IP address ranges. If the list of IP ranges being scanned is large, you can configure the Shazzam payload for JSON encoding to reduce its size.

## Before you begin

Role required: admin

## About this task

You control the behavior of individual Shazzam probes using basic and advanced parameters.

For instructions on configuring probe parameters, see [Set probe parameters](t_SetProbeParameters.md).

**Note:** The Shazzam payload is controlled by the following [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). These properties do not need to be added to the MID Server. The Shazzam probe will fall back on their default values.

-   The **shazzam.chunk\_size** property controls the maximum number of IP addresses Shazzam can scan in parallel.
-   The **mid.shazzam.regulator.interval\_ms** property sets the interval in which Shazzam can launch packets.
-   The **mid.shazzam.regulator.packets\_per\_interval** property sets the number of packets that Shazzam can launch in that time interval.

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Probes**.

2.  Select **Shazzam**.

3.  Add or edit parameters in the **Probe Parameters** related list.

4.  Configure the Shazzam parameters.

    These parameters are available for fine-tuning the Shazzam probe. These values are defined in the probe record only.

<table id="table_b1y_skz_y1b"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BannerTCP\_waitForConnectMS

</td><td>

Sets the number of milliseconds the BannerTCP scanner waits for a connection and banner.**Default**: 1500

</td></tr><tr><td>

debug

</td><td>

Enables debug logging if set to **true**.**Default**: false

</td></tr><tr><td>

delay\_wbem

</td><td>

Delays classification of systems with a WBEM port open until the final Shazzam sensor job. For a large schedule discovering many WBEM ports, delaying classification until the last sensor job could cause the node to run out of memory. Setting this parameter to **false** allows classification of these systems to occur across all Shazzam sensor jobs.**Default**: true

</td></tr><tr><td>

DNS\_alternativePort

</td><td>

Deprecated

</td></tr><tr><td>

DNS\_waitForResponseMS

</td><td>

Sets the number of milliseconds the DNS scanner waits for a response.**Default**: 1000

</td></tr><tr><td>

GenericTCP\_waitForConnectMS

</td><td>

Sets the number of milliseconds the GenericTCP scanner waits for a connection.**Default**: 1000

</td></tr><tr><td>

HTTP\_waitForConnectMS

</td><td>

Sets the number of milliseconds the HTTP scanner waits for a connection.**Default**: 500

</td></tr><tr><td>

HTTP\_waitForResponseMS

</td><td>

Sets the number of milliseconds the HTTP scanner waits for a response.**Default**: 500

</td></tr><tr><td>

NBT\_alternativePort

</td><td>

Deprecated

</td></tr><tr><td>

NBT\_waitForResponseMS

</td><td>

Sets the number of milliseconds the NBT scanner waits for a response.**Default**: 500

</td></tr><tr><td>

shazzam\_report\_inactive

</td><td>

When **true**, reports devices that are alive but inactive. For example, a device has no ports open but refuses at least one port connection request.**Default**: true

</td></tr><tr><td>

scanner\_log

</td><td>

Enables scanner logging if set to **true**. This logging information appears in the Shazzam probe response.**Default**: false

</td></tr><tr><td>

shazzam\_report\_dead

</td><td>

When **true**, reports devices with dead IP addresses. For example, a device that has all ports closed.**Default**: false

</td></tr><tr><td>

SNMP\_alternativePort

</td><td>

Deprecated

</td></tr><tr><td>

SNMP\_tapIntervalMS

</td><td>

Sets the number of milliseconds the SNMP scanner waits between taps.**Default**: 1000

</td></tr><tr><td>

SNMP\_taps

</td><td>

Sets the number of taps \(requests\) the SNMP scanner attempts.**Default**: 2

</td></tr><tr><td>

SNMP\_waitForResponseMS

</td><td>

Sets the number of milliseconds the SNMP scanner waits for a response after the last tap.**Default**: 1000

</td></tr><tr><td>

TLS\_keepOriginalCertificate

</td><td>

When **true** and Discovery is running, the certificate\_file field in the cmdb\_ci\_certificate is populated with the original certificate. This can increase your payload size.**Default**: false

</td></tr></tbody>
</table>
**Parent Topic:**[Port probes](../reference/r_PortProbes.md)

## Control Shazzam payload size

A system property converts Shazzam payloads into JSON strings, which dramatically reduces their size. This setting prevents nodes from running out of memory when a single schedule discovers large numbers of IP ranges.

### Before you begin

Role required: admin

### About this task

The `glide.discovery.shazzam_ranges_json` property is set to `true` for new instances. This setting encodes the payload as a JSON string. The property is configurable by administrators and is available in the **Discovery Definition** &gt; **Properties** module. The property label is **Use JSON for IP ranges in Shazzam** in the module.

This property is set to `false` in upgraded instances and is not visible by default. Adding the property manually to your upgraded instance enables the feature, but does not add it to the **Discovery Definition** &gt; **Properties** module. To enable JSON encoding and add it to the module, import the update set attached to [KB0687626](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0687626%26sysparm_stack%3D%26sysparm_view%3D).

### Procedure

1.  In the navigation filter, type `sys_properties.list` and press `Enter`.

2.  In the list of system properties, click **New**.

3.  Complete the form, using these field values:

    -   **Name**: glide.discovery.shazzam\_ranges\_json
    -   **Description**: Encodes the Shazzam payload in JSON.
    -   **Value**: true
4.  Click **Submit**.



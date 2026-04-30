---
title: SNMP probe parameters
description: This list of parameters may be passed to the SNMP probes.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [SNMP probes, List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# SNMP probe parameters

This list of parameters may be passed to the SNMP probes.

For instructions on configuring probe parameters, see [Set probe parameters](../task/t_SetProbeParameters.md).

<table id="table_mmh_pny_5p"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

oid\_spec\_list

</td><td>

A list of OID specifications, one per line. Each specification must be in one of the following two forms:

 -   walk \{OID\}: Walks the OID and all its children
-   table \{OID\} \{OID Children\}: Walks all entries in the table, returning only the given children \(for example, "iso.org.dod.internet"\)

 \{OID Children\} refers to a comma-delimited list of child nodes within the entries for the given table. For example, "ifEntry.ifIndex,ifEntry.ifDescr,ifEntry.ifType" are OID children of the table "iso.org.dod.internet.mgmt.mib-2.interfaces.ifTable". As a convenience, the table entry prefix may be left off. \(The preceding children could be specified as "ifIndex,ifDescr,ifType".\)

 Any child may include a filter qualifier in parentheses. For example, the child "entPhysicalContainedIn\(=0\)" specifies returning table entries only if the value of "entPhysicalContainedIn" equals 0. The operators supported in the expression are:

-   `=` : equals
-   `!=` : does not equal
-   `#` : contains

 If more than one child has a filter expression, a match on any one of the children causes that entry to be read.

 Any content including and after a "//" is ignored \(comments\). Any OID that does not start with "1.3.6.1" or "iso.org.dod.internet" automatically prefaces with "1.3.6.1." as a convenience.

</td><td>

required

</td></tr><tr><td>

source

</td><td>

The IP address or host name of the device to query SNMP on.

</td><td>

required

</td></tr><tr><td>

index

</td><td>

The index to apply after the community string, for Cisco-style community string indexing \(for VLAN interrogation\).

</td><td>

0

</td></tr><tr><td>

credential\_id

</td><td>

The sys\_id of a specific credential that is preferred for use above the rest. This parameter is for internal use only and is not supported.

</td><td>

none

</td></tr><tr><td>

credential\_tag

</td><td>

The credential tag that must be used. This parameter is for internal use only and is not supported.

</td><td>

none

</td></tr><tr><td>

timeout

</td><td>

The timeout value \(in milliseconds\) to wait for a response, instead of the default. You can use this parameter to override the **mid.snmp.request.timeout** SNMP MID Server configuration parameter.

 **Note:** When **use\_getbulk** is set to **true**, the timeout value is for an individual GETBULK request.

</td><td>

1500

</td></tr><tr><td>

established\_session\_timeout

</td><td>

The interval \(in milliseconds\) to wait for a response after at least one response has been received. Longer values can be useful for collecting complete and accurate data. You can use this parameter to override the **mid.snmp.session.timeout** SNMP MID Server configuration parameter.

</td><td>

500

</td></tr><tr><td>

debug

</td><td>

Enables debug logging. Set to true for debug mode.

</td><td>

false

</td></tr><tr><td>

request\_interval

</td><td>

The interval \(in milliseconds\) between successive requests for an OID when a response has not been received, until the timeout \(or established\_session\_timeout\) value is reached. If this value is set to at least as long as the timeout \(or established\_session\_timeout\) value, then only a single request is sent for any particular OID. If you change the timeout \(or established\_session\_timeout\) value, adjust the request\_interval at the same time to avoid sending too many or too few requests for the same OID, as appropriate for a given environment.

</td><td>

400

</td></tr><tr><td>

request\_delay

</td><td>

The interval \(in milliseconds\) between the receipt of a response and the transmission of the next request. The default is 0 \(no delay\). This value may be set to slow the overall rate of an SNMP query.

</td><td>

0

</td></tr><tr><td>

result\_format

</td><td>

Returns JSON formatted payloads for these probes: -   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System
-   SNMP - Routing

This parameter returns data in a more compact format to prevent sensor failure or memory problems on a node when the payload becomes large. Do not change this value or delete this parameter.**Warning:** Use of this parameter with any other probes causes the sensor to fail.

</td><td>

JSON

</td></tr><tr><td>

use\_getbulk

</td><td>

Enables the use of SNMP GETBULK requests to retrieve tabular data from SNMP devices instead of using multiple SNMP GETNEXT requests. For tabular data, GETBULK is more efficient. Regardless of the request type, certain devices may not return any results when they are busy with other tasks. This parameter is used to configure at the probe level. GETBULK can also be set for an individual MID Server or globally for all MID servers. Settings are listed in the order of precedence:

-   SNMP probe parameter
-   [MID Server configuration parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

 The **established\_session\_timeout, request\_interval,** and **request\_delay** parameters are ignored when **use\_getbulk** is set to **true**. Instead, the **retries** parameter is available. The timeout configuration is the same one used by **use\_getscalar**.

 By default, the following probes use GETBULK requests \(the parameter value is **true**\).

-   SNMP - Switch - Vlan
-   SNMP - Switch - BridgePortTable
-   SNMP - Switch - ForwardingTable
-   SNMP - Switch - SpanningTreeTable
-   SNMP - Network - ArpTable
-   SNMP - Layer 2 Protocol Caches
-   SNMP - F5 BIG IP - System \(only for Service Mapping customers\)

 **Note:** These probes have a **timeout** value of 5000.

</td><td>

false

</td></tr><tr><td>

use\_getscalar

</td><td>

Enables the use of simplified retrieval and handling of scalar values from SNMP devices. The **established\_session\_timeout, request\_interval**, and **request\_delay** parameters are ignored when **use\_getscalar** is set to **true**. Instead, the **retries** and **timeout** parameters are available. The timeout configuration is the same one used by **use\_getbulk**.

</td><td>

false

</td></tr><tr><td>

retries

</td><td>

The number of additional attempts Discovery makes to complete an individual GETBULK request \(see **use\_getbulk**\) or a GETNEXT request when the **use\_getscalar** parameter is set to **true**.

</td><td>

2

</td></tr></tbody>
</table>**Parent Topic:**[SNMP probes](../concept/c_SNMPProbe.md)


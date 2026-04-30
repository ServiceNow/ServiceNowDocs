---
title: Network port default check
description: Agent Client Collector provides the following default check for Network port monitoring. The check is available for both Windows and Linux.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-10-09"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Network port default check

Agent Client Collector provides the following default check for Network port monitoring. The check is available for both Windows and Linux.

<table id="table_nlr_j1s_zcc"><thead><tr><th>

Type

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Event

</td><td>

Generates an event for all ports of the specified host address, indicating whether each port is available or in use.

 A CRITICAL event is generated for ports that are either not in use or down. An OK event is generated only if all the specified ports are in use and operational.

 The required parameters are: host, ports.

</td><td>

`check-ports.rb -H localhost -p 22,25,8100-8131,3030 -P tcp -t 5`

-   -h host - Includes all of the hosts, separated by commas, where the specified ports are located. Required field.
-   -p ports - Includes all of the ports, separated by commas, that require monitoring. Required field.
-   -t timeout - Time, in seconds, that the system waits for a connection to be successfully established before aborting the attempt and generating a timeout error. Optional field.
-   -P protocol - Specifies the communication protocol \(such as TCP or UDP\) which is assigned to handle data transmission through a particular network port that is specified in the given parameter. Optional field.

</td><td>

CheckPort CRITICAL: Connection refused by:

 Host: localhost and its ports are: 8100, 8101, 8102, 8103, 8104, 8105, 8106, 8107, 8108, 8109, 8110, 8111, 8112, 8113, 8114, 8115, 8116, 8117, 8118, 8119, 8120, 8121, 8122, 8123, 8124, 8125, 8126, 8127, 8128, 8129, 8130, 8131, 3030.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)


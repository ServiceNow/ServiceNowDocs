---
title: MID Server Configuration Parameter settings and priority
description: The MID Server's settings reside in multiple tables and the MID Server prioritizes them in a set order. MIDConfigParameter must be defined with the correct type-style builders.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server Configuration Parameter settings and priority

The MID Server's settings reside in multiple tables and the MID Server prioritizes them in a set order. MIDConfigParameter must be defined with the correct type-style builders.

## MID Server settings priority

MID Server settings can reside in both the Configuration Parameter table and Properties tables. MID Servers prioritize the settings in the following order:

1.  ​MID Configuration Parameter
2.  MID Property \(specific MID\)
3.  MID Property \(global\)

## Invalid Record Prevention

Avoid creating duplicate records in the MID Property table because they can invalid records. Duplicate properties have the same name and are assigned to the same MID Server.

Similarly, avoid creating global configuration parameters because they are unsupported. Global configuration parameters are configuration parameters with no assigned MID Server. If a setting should be applied to all MID Servers, then use a global MID Property.

**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](r_MIDServerSystemRequirements.md)

[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

[MID Server dashboard](../concept/c_MIDServerDashboard.md)

[MID Server properties](r_MIDServerProperties.md#)

[MID Server parameters](mid-server-parameters.md#)

[MID Server File Cleaner](../concept/mid_file_cleaner.md)

[MID Server protected records and reserved characters](mid-server-reserved-characters.md)

[MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)


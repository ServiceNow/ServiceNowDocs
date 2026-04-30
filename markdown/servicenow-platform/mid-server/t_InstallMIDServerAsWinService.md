---
title: Manually start, stop, and restart a MID Server
description: If you did not start the MID Server at the end of the installation procedure, you can manually start the MID Server.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Manually start, stop, and restart a MID Server

If you did not start the MID Server at the end of the installation procedure, you can manually start the MID Server.

## Before you begin

Role required: MID Server Service account user or a Windows Admin account

This procedure is only for users who install the MID Server using the ZIP file. The Windows MID Server installer completes the installation automatically.

## Procedure

1.  Open the agent directory in the directory you created for the MID Server installation files.

    For example, the path might be `C:\ServiceNow\MID Server1\agent`.

2.  Start the MID Server by executing the `start.bat` file.

3.  To stop the MID Server, execute the `stop.bat` file.

4.  To restart a stopped MID Server, either:

    -   If the MID Server is stopped, execute the `start.bat` file.
    -   If the MID Server is running, execute the `restart.bat` file.

**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](../reference/r_MIDServerSystemRequirements.md)

[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)

[MID Server dashboard](../concept/c_MIDServerDashboard.md)

[MID Server properties](../reference/r_MIDServerProperties.md#)

[MID Server parameters](../reference/mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](../reference/mid-config-param-priority.md)

[MID Server File Cleaner](../concept/mid_file_cleaner.md)

[MID Server protected records and reserved characters](../reference/mid-server-reserved-characters.md)

[MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](../reference/r_MIDSystemMethods.md)

[MID Server heartbeat](../reference/r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](t_PauseTheMIDServer.md#)


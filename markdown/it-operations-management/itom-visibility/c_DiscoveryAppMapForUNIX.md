---
title: Application Mapping for UNIX discovery
description: To perform the mapping that establishes application relationships, Discovery must be able to detect TCP connections.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Application Mapping for UNIX discovery

To perform the mapping that establishes application relationships, Discovery must be able to detect TCP connections.

The best way to accomplish this is to run the [lsof](http://people.freebsd.org/%7Eabe/) command on target machines. For AIX machines, Discovery is configured to use the active connection probe for AIX targets. However, the user that executes the shell script on AIX machines might require additional privileges to execute commands, such as kdb, employed in the script.

On Linux machines, Discovery uses the `lsof` command \(installed by default on Linux\) to detect TCP connections. The Linux classification probe triggers the Linux - Active Connections probe, which uses `lsof` to discover application relationships and does not produce any pauses. The `lsof` command is the recommended method of returning active TCP connections and can be installed on Solaris and AIX target machines to eliminate any issues produced by the shell script.

**Note:** Discovery of active connections on HP-UX is not supported.

-   **[Using the lsof Command](../task/t_UsingTheLsofCommand.md)**  
Use the ls of command to return active TCP connections and can be installed on Solaris and AIX target machines.

**Parent Topic:**[Software discovery](c_Software.md)


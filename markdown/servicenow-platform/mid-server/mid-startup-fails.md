---
title: MID Server fails to start
description: When a newly installed MID Server fails to start or shuts down prematurely, improper configuration could be to blame.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Resolving MID Server issues, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server fails to start

When a newly installed MID Server fails to start or shuts down prematurely, improper configuration could be to blame.

## Duplicate MID Server names

When the MID Server service starts, it verifies that it is the only active \(not down\) MID Server with that name. If the MID Server discovers another active MID Server with the same name, the starting MID Server waits 5 minutes and sends another query. The MID Server repeats this query 12 times and logs each attempt in the agent log. If the IP address or home directory of an existing MID Server is changed, then that MID Server is invalidated. If the MID Server still detects a duplicate after this cycle, it creates a record in the [MID Server Issue \[ecc\_agent\_issue\]](../concept/mid-server-active-issues.md) table and shuts down.

**Note:** The record in the MID Server Issue \[ecc\_agent\_issue\] table cannot be resolved automatically by the instance. Close this record manually for accounting purposes. Either mark the issue **Resolved** or delete it.

## Upgraded MID Servers running multiple services

Beginning with the New York release, a batch file in the MID Server installer package ensures that only one Windows MID Server service is configured for an executable path \(MID Server installation folder\). Previous versions have not checked for this configuration. Upgraded MID Servers that run multiple services with the same executable path are prevented from starting. If you experience this issue, follow this procedure to reconfigure the MID Server to use only one service:

1.  Delete the unwanted Windows service by running **sc.exe delete &lt;service name&gt;** from the command line.
2.  Open the `wrapper-override.conf` file in the MID Server installation folder.
3.  Change the **wrapper.name** and **wrapper.displayname** parameters to the service name that you want to keep.
4.  Restart the MID Server.

**Parent Topic:**[Resolving MID Server issues](r_MIDServerTroubleshooting.md)


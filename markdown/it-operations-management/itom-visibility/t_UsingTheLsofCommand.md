---
title: Using the lsof Command
description: Use the ls of command to return active TCP connections and can be installed on Solaris and AIX target machines.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application Mapping for UNIX, Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Using the lsof Command

Use the ls of command to return active TCP connections and can be installed on Solaris and AIX target machines.

## Before you begin

Role required: admin

## Procedure

1.  Install `lsof` on the Solaris and AIX machines on which you want to gather application relationship data.

2.  In the instance, navigate to **Discovery Definition** &gt; **CI Classification** &gt; **UNIX**.

3.  Select **Solaris** from the list.

4.  In the UNIX Classification form for Solaris, select the **Triggers probes** related list, and then click **Edit**.

5.  Move **Linux - Active Connections** from the Collections list to the Triggers probe List.

    This probe is configured to use `lsof`.

    ![Solaris Active Connections lsof](../image/SolarisActiveConnectionsLsof.png "Solaris Active Connections lsof")

6.  Click **Save**.

7.  Repeat this procedure for the AIX classification probe.


**Parent Topic:**[Application Mapping for UNIX discovery](../concept/c_DiscoveryAppMapForUNIX.md)


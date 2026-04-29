---
title: Reclassify a Windows Workstation machine as a server
description: By default, Discovery automatically classifies computers using certain Windows operating systems as workstations. However, you might want specific computers in your network that are acting as servers to be classified by their function and not their operating system.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Reclassify a Windows Workstation machine as a server

By default, Discovery automatically classifies computers using certain Windows operating systems as workstations. However, you might want specific computers in your network that are acting as servers to be classified by their function and not their operating system.

## Before you begin

Role required: none

## About this task

Use the following variables, preceded by **cidata**, to construct a reclassification condition. For example, to reclassify based on a machine's IP address, use **cidata.ip\_address**.

-   name
-   dsn\_domain
-   os\_domain
-   ip\_address
-   serial\_number

The following procedure reclassifies any Windows workstation operating system \(Windows Vista, XP, or Windows 7\) that is acting as a server.

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **Windows**.

2.  Create a new classification record, such as Windows XP Server.

3.  Select Windows Server `[cmdb_ci_win_server]` as the table.

4.  Right-click in the header bar and select **Save** from the context menu.

    The **Classification Criteria** and **Triggers Probes** Related Lists appear.

5.  Configure the following **Classification Criteria**:

    ![classification criteria](../image/ExampleDiscoveryClassificationCriteria.png)

<table id="simpletable_af1_1v2_q4"><tbody><tr><td>

**Name**

</td><td>

Select a variable to use as the classification criteria from the list above. For example, to reclassify a machine by name, enter `cidata.name`. This works for servers that have a uniform naming convention, such as SRV001, SRV002, etc., regardless of operating system.

</td></tr><tr><td>

**Operator**

</td><td>

Select an operator for the classification condition. In networks containing servers named with a specific convention, you might select **starts with** or **contains**.

</td></tr><tr><td>

**Value**

</td><td>

Enter the value for the condition. In our example of a network with a server naming convention, this value would be the root of that convention, such as **SRV** This condition will classify all computers as servers if their machine name is SRVXXX.

</td></tr></tbody>
</table>6.  Select the **Triggers Probe** related list and add the appropriate probes.

    1.  Copy the list of probes from another Windows server classification, including the Condition scripts.

    2.  Ensure that the **Windows - Identity** probe has a phase of **Identification** \(the default is **Exploration**\).

        The completed form looks like this:

        ![Windows classification](../image/DiscoveryClassificationFormTriggersProbe.png)


## What to do next

Run a discovery from the [Discovery schedule](t_CreateADiscoverySchedule.md#) to find Windows machines on your network, and then check the cmdb\_ci\_win\_server table and related tables to see how data is populated in the CMDB.


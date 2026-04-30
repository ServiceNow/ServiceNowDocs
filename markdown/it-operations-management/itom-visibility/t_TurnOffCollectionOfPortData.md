---
title: Turn off collection of port data for SNMP network devices
description: In some environments you may not want to collect the port data for SNMP network devices.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Network switch and router, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Turn off collection of port data for SNMP network devices

In some environments you may not want to collect the port data for SNMP network devices.

## Before you begin

Role required: admin

## About this task

If the network devices contain an extremely large number of ports and each individual port's information is not critical to the overall management of the devices, you may not want to collect the port data for SNMP network devices. This would affect records from being created in the Switchports table \(dscy\_switchport\). This process only impacts probe discovery.

## Procedure

1.  Navigate to **Discovery Definition** &gt; **Probes**.

2.  Go to the **SNMP - Switching** probe.

3.  In the **SNMP Fields** tab, find the field named **ports**, double-click the value in the **Active** column, and change the value to **false**.

    The collection and processing of ports information for switches is then disabled. The **ports** field for the switch CI should have the correct ports count even though the related list **switchports** is empty.

4.  Click the check mark to save the change.


**Parent Topic:**[Network switch and router discovery](../reference/r_DataCollDiscoNWRouteAndSwitch.md)


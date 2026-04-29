---
title: Collect operational values for datacenter
description: Record and update operational values manually for datacenters performance tracking in the Telecommunications Network Inventory application. You can use this data for further analysis and reporting.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Capacity management, Configure, Telecommunications Network Inventory]
---

# Collect operational values for datacenter

Record and update operational values manually for datacenters performance tracking in the Telecommunications Network Inventory application. You can use this data for further analysis and reporting.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.dc\_ops\_agent

## About this task

Enter the operational data for power and temperature manually and store it in the ClothoDB. You can use this data to display the operational details in a floor map. You can enter data for your datacenter, cabinet, rack, and cage.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.k

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Racks**.

3.  Select the rack that you want to update operational data.

4.  Select the more options icon \(![More Options Icon.](../../tmt-order-mgt/image/more-options.png)\) and then select **Collect Operational Data**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Timestamp|Select a data and time for the data to be collected.|
    |Real Power \(kW\)|Active power of your network asset.|
    |Contractual Power \(kVA\)|Maximum apparent power of your network asset.|
    |Apparent Power \(kVA\)|Apparent Power of your network asset.|
    |Temperature \(C\)|Temperature of your network asset.|

6.  Select Submit.


## Result

The instance stores the operational data in the clothoDB.

**Parent Topic:**[Configuring capacity management](../concept/configuring-capacity-management.md)


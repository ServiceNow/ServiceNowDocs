---
title: Manage high number of concurrent bookings
description: Manage multiple parallel queues to help process mass booking appointments run in a parallel mode. You can distribute the mass booking event processors to different nodes rather than keeping the load on a single node.
locale: en-US
release: zurich
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Manage high number of concurrent bookings

Manage multiple parallel queues to help process mass booking appointments run in a parallel mode. You can distribute the mass booking event processors to different nodes rather than keeping the load on a single node.

## Before you begin

Role required: sn\_vaccine\_sm.admin

## About this task

The **sn\_vaccine\_sm.mass\_booking\_parallelism** property helps you implement the appointment booking flow in a parallel mode. With parallel processing, the job creates separate events for each vaccination center. It helps dispatch the events into the available parallel queues evenly. There are a total of eight mass booking event processors.

**Note:** A maximum of eight queues can be used for mass booking. Even if a user with the admin role sets the property to a value greater than **8**, only eight queues are created. However, the default value is set to **4**.

To avoid performance-related issues, configuration changes are required to pin to a specific node. As a user with the admin role, you can choose which thread to point to a specific node so that the load is distributed evenly across all the nodes. For example, if you’re using a multi-node instance, you can change the configuration to pin to a specific node by using the system ID field to select the specific node where you want your mass booking event processor to hit. This configuration change can improve the system performance.

## Procedure

1.  In the navigation filter, enter `sys_trigger.list`.

2.  In the **Search** field, enter `*mass booking event processor`.

    In the Schedule table, you can see eight mass booking event processor records.

3.  If you have a multi-node instance, locate the mass booking event processor record and choose a node from the **System ID** column field.

4.  Double-click the empty area of the **System ID** field.

    1.  Choose a node from the list of available nodes.

    2.  Save the record by clicking the green checkmark icon \(![Green checkmark icon.](../image/green-checkmark-icon.png)‎\).

    The mass booking event processor record is assigned to a specific node.

5.  To assign different mass booking event processor records to specific nodes, repeat step 3 and step 4, as needed.


**Parent Topic:**[Configuring Vaccine Administration Management](vaccine-mgmt-config.md)


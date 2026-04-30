---
title: Modify the Design and Assign function layout
description: Modify the Design and Assign function layout in the Telecommunications Network Inventory application by configuring the endpoint. You can create the layout according to your network service requirement
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Design and Assign function for your network services, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Modify the Design and Assign function layout

Modify the Design and Assign function layout in the Telecommunications Network Inventory application by configuring the endpoint. You can create the layout according to your network service requirement

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

By default, the Design and assign function layout shows three sections such as activity picker, activity viewer, and network diagram. Currently the network diagram shows the circuit map for logical connection. You can customize the network diagram according to your requirement by configuring the `sn_ni_ws.TNIDesignAssignConfiguration` endpoint. You can also remove the network diagram from the layout by deleting the associated script.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Open the **sn\_ni\_ws.TNIDesignAssignConfiguration** record.

3.  Edit the script according to your requirement.

4.  Select **Update**.


**Parent Topic:**[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)


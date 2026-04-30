---
title: Configure Telecommunications Network Inventory attributes
description: Configure the core equipment table to enable the collection of the common Telecommunications Network Inventory attributes appear in the CI record. You use these attributes to create a Telecommunications Network Inventory CI record.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Configure Telecommunications Network Inventory attributes

Configure the core equipment table to enable the collection of the common Telecommunications Network Inventory attributes appear in the CI record. You use these attributes to create a Telecommunications Network Inventory CI record.

## Before you begin

Role required: admin

## About this task

You update the Equipment generic classes in the core equipment table to display the **Set Inventory Attributes** button in the corresponding CI record \(sub classes\). Except for the Interface card table \(cmdb\_ci\_interface\_card\), all tables that are subclasses of the equipment generic classes are considered as Equipment.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Select the **sn\_ni\_core.equipment\_tables** table.

3.  In the **Value** field, enter the equipment generic classes using a comma as separator.

    You can add the following generic classes:

    -   Computer \(cmdb\_ci\_computer\)
    -   Network Gear \(cmdb\_ci\_netgear\)
    -   Virtual Machine Object \(cmdb\_ci\_vm\_object\)
    -   Kubernetes Component \(cmdb\_ci\_kubernetes\_component\)
    -   Service Instance \(cmdb\_ci\_service\_auto\)

**Parent Topic:**[Configuring Telecommunications Network Inventory](../concept/configuring-telecom-network-inventory.md)


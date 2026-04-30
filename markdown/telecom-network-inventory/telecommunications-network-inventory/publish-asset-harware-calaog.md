---
title: Publish an asset to the hardware catalog
description: Publish an asset to the hardware catalog so that you can procure the asset by using the Telecommunications Network Inventory application integration with the Hardware Asset Management application.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Publish an asset to the hardware catalog

Publish an asset to the hardware catalog so that you can procure the asset by using the Telecommunications Network Inventory application integration with the Hardware Asset Management application.

## Before you begin

Before you can publish an asset to the hardware catalog, make sure that an inventory model record has already been created for that asset. If there's no record, you can create an inventory model record. To learn more, see [Creating your inventory models](../concept/creating-your-inventory-models.md).

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

You can publish an asset to the hardware catalog to make it available as a catalog item. You can procure the asset by creating a service request. To learn more about how to create a service request, see [Create a service request to procure assets](create-service-request-procure-assets.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Equipment Models**.

    To publish an interface card, select **Interface Card Models**.

3.  From the list of records, select the inventory model record that you want.

4.  Select **Publish to Hardware Catalog**.

    If the inventory model is already added to the hardware catalog, the **Publish to Hardware Catalog** button doesn’t appear.

5.  In the **Category** field, select the hardware asset.

6.  Select **OK**.


## Result

A catalog item is created for your asset.

**Parent Topic:**[Reviewing and updating your network inventory with the Network Inventory Workspace](../concept/tni-workspace.md)

**Related topics**  


[Telecommunications Network Inventory integration with Hardware Asset Management](../concept/integration-with-hardware-asset-management.md)


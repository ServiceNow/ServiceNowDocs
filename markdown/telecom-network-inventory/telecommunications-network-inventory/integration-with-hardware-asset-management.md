---
title: Telecommunications Network Inventory integration with Hardware Asset Management
description: By integrating the Telecommunications Network Inventory application with the Hardware Asset Management \(HAM\) application, you can use an inventory template to create a service request. You can also associate the assets that are available in a stock room to instantiate the equipment.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Telecommunications Network Inventory with other applications, Telecommunications Network Inventory]
---

# Telecommunications Network Inventory integration with Hardware Asset Management

By integrating the Telecommunications Network Inventory application with the Hardware Asset Management \(HAM\) application, you can use an inventory template to create a service request. You can also associate the assets that are available in a stock room to instantiate the equipment.

## HAM integration overview

With this integration, you can enable the Telecommunications Network Inventory application to create the bill of materials for your assets by using a record producer. Then, you can create a service request to get those assets. To learn more about record producers, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Before creating the service request, you must publish the asset to the hardware catalog by adding it to the Catalog Definition table. To learn more, see [Publish an asset to the hardware catalog](../task/publish-asset-harware-calaog.md).

The Hardware Asset Management fulfills the service request and executes the workflow to procure the assets in the Hardware Asset Management Workspace. To learn more about the Hardware Asset Management workflow, see [Procurement](https://www.servicenow.com/docs/access?context=c_Procurement&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).

After the assets are acquired or available in a stockroom, the procurement managers can use the ServiceNow® Procurement application to create the configuration items \(CIs\) for these assets. You can use these CIs for equipment instantiation by tagging them.

When you instantiate equipment at a network site with an inventory template, the system picks the assets that match with the interface card models if they’re in the same network site location. Otherwise, the application creates a CI for the interface card. The system makes a relationship with the other assets that are available in a stockroom. These relationships are made only if the related assets are available in a stockroom.

## Hardware Asset Management integration workflow

This integration enables you to do the following tasks:

1.  Create a service request for the bill of materials. To learn more, see [Create a service request to procure assets](../task/create-service-request-procure-assets.md).
2.  Associate the assets from an available stock room. You can associate the asset when you create equipment by using the change model. To learn more, see [Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md).

-   **[Create a service request to procure assets](../task/create-service-request-procure-assets.md)**  
Create a bill of materials for assets by using a record producer, and then create a service request to procure those assets. You can do both these actions by using the Telecommunications Network Inventory application integrations with the Hardware Asset Management application.

**Parent Topic:**[Integrating Telecommunications Network Inventory with other applications](integrating-telecommunications-network-inventory--applications.md)

**Related topics**  


[Telecommunications Network Inventory and Order Management for Telecommunications and Media](telecomm-network-inventor-order-management.md)


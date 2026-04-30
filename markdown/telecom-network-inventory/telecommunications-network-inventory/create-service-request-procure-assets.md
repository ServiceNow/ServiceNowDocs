---
title: Create a service request to procure assets
description: Create a bill of materials for assets by using a record producer, and then create a service request to procure those assets. You can do both these actions by using the Telecommunications Network Inventory application integrations with the Hardware Asset Management application.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Telecommunications Network Inventory integration with Hardware Asset Management, Integrating Telecommunications Network Inventory with other applications, Telecommunications Network Inventory]
---

# Create a service request to procure assets

Create a bill of materials for assets by using a record producer, and then create a service request to procure those assets. You can do both these actions by using the Telecommunications Network Inventory application integrations with the Hardware Asset Management application.

## Before you begin

Make sure to add the asset that you want to procure in the hardware catalog. To learn more, see [Publish an asset to the hardware catalog](publish-asset-harware-calaog.md).

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

To procure the assets, you can create a service request for a bill of materials by using the Material Request using Inventory Template record producer. To learn more about record producers, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Procurement** &gt; **Requests**.

3.  Select **New**.

4.  In the Material Request using Inventory Template record producer, fill in the fields.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inventory Template

</td><td>

Inventory template that includes the assets that you want to procure. When you select the template, the related assets list is displayed in the Material Count section.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of the assets. Enter the required quantity of each asset in the **Quantity** field.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

A service request is created to procure the assets.

**Parent Topic:**[Telecommunications Network Inventory integration with Hardware Asset Management](../concept/integration-with-hardware-asset-management.md)


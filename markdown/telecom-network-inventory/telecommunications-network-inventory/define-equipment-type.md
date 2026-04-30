---
title: Create a telecommunications equipment instance
description: DOC1064599 All Equipment window.Create a telecommunications equipment instance in your network. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Manually creating and reviewing your network asset instances, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a telecommunications equipment instance

Create a telecommunications equipment instance in your network. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

You can create the equipment instances that have the inventory category set as Equipment. When you create an equipment record, it creates a configuration item \(CI\) record in the corresponding equipment table. To learn more about the equipment extended classes, see [Data model for Telecommunications Network Inventory](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **All Equipment**.

    You can create the following equipment types by selecting the options from the List menu.

<table id="choicetable_mds_dxq_qxb"><thead><tr><th align="left" id="d66093e109">

Option

</th><th align="left" id="d66093e112">

Description

</th></tr></thead><tbody><tr><td id="d66093e118">

**IP Routers, IP Switches, IP Firewalls, IP Load Balancers, Servers, or Virtual Machines**

</td><td>

Creates a record that you’ve selected. To learn more about the fields in the form, see [Router, Switch, Firewall, Virtual Machine, Load Balancer, and Server forms](../reference/router-form.md).

</td></tr><tr><td id="d66093e140">

**Kubernetes Clusters**

</td><td>

Creates a Kubernetes cluster instance. To learn more about the fields in the form, see [Kubernetes discovery using patterns](https://www.servicenow.com/docs/access?context=kubernetes-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

</td></tr><tr><td id="d66093e159">

**Kubernetes Pods**

</td><td>

Creates a Kubernetes pod machine instance. To learn more about the fields in the form, see [Kubernetes discovery using patterns](https://www.servicenow.com/docs/access?context=kubernetes-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

</td></tr></tbody>
</table>3.  Select **New** and then select the equipment type from the list.

    To learn more about the equipment extended classes, see [Equipment extension classes](../reference/equipment-extension-classes.md).

4.  In the Equipment form, fill in the fields.

    To learn more about the fields in the Equipment form, see [829eed273b1cf4dc4ebba88cd8857e4eb0c15cd6.dita](define-tni-equipment.md).

5.  Create the Telecommunications Network Inventory attributes for the Telco Equipment form by selecting **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see the [TNI CI Attributes form](../reference/ci-attribue-form.md).

7.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Telco Equipment form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn’t appear when you reopen the CI record.

8.  To view the Dependency views map, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the specific network asset and the relationships between the CIs.

9.  Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Using an attribute pack for a CI record](../concept/using-pack-table-ci-record.md).

10. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).

11. Select **Submit**.

    The inventory record is created for the equipment type that you’ve selected.


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

-   **[Review and update the telecommunications equipment details](define-tni-equipment.md)**  
Review and update a network asset instance for your telecommunications equipment. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.

**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Modeling your Telecommunications Network Inventory workflow](../concept/telecommunications-network-inventory-workflow.md)


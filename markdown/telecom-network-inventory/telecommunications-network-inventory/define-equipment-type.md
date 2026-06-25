---
title: Create a telecommunications equipment instance
description: DOC1064599 All Equipment window.Create a telecommunications equipment instance in your network. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/define-equipment-type.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create a telecommunications equipment instance

Create a telecommunications equipment instance in your network. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

You can create the equipment instances that have the inventory category set as Equipment. When you create an equipment record, it creates a configuration item \(CI\) record in the corresponding equipment table. To learn more about the equipment extended classes, see [Data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon.\), and then go to **Inventory** &gt; **All Equipment**.

    You can create the following equipment types by selecting the options from the List menu.

<table id="choicetable_mds_dxq_qxb"><thead><tr><th align="left" id="d72897e108">

Option

</th><th align="left" id="d72897e111">

Description

</th></tr></thead><tbody><tr><td id="d72897e117">

**IP Routers, IP Switches, IP Firewalls, IP Load Balancers, Servers, or Virtual Machines**

</td><td>

Creates a record that you’ve selected. To learn more about the fields in the form, see [Router, Switch, Firewall, Virtual Machine, Load Balancer, and Server forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/router-form.md).

</td></tr><tr><td id="d72897e139">

**Kubernetes Clusters**

</td><td>

Creates a Kubernetes cluster instance. To learn more about the fields in the form, see [Kubernetes discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/kubernetes-discovery.md).

</td></tr><tr><td id="d72897e155">

**Kubernetes Pods**

</td><td>

Creates a Kubernetes pod machine instance. To learn more about the fields in the form, see [Kubernetes discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/kubernetes-discovery.md).

</td></tr></tbody>
</table>3.  Select **New** and then select the equipment type from the list.

    To learn more about the equipment extended classes, see [Equipment extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/equipment-extension-classes.md).

4.  In the Equipment form, fill in the fields.

    To learn more about the fields in the Equipment form, see [ee9363b19ca20d3f5503d82662539f1c1d1d3c8f.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-equipment.md).

5.  Create the Telecommunications Network Inventory attributes for the Telco Equipment form by selecting **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see the [TNI CI Attributes form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ci-attribue-form.md).

7.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Telco Equipment form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn’t appear when you reopen the CI record.

8.  To view the Dependency views map, select the more options icon \(\[Omitted image "options-icon.png"\] Alt text: More Options icon.\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the specific network asset and the relationships between the CIs.

9.  Select the more options icon \(\[Omitted image "options-icon.png"\] Alt text: More Options icon.\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Attribute pack for CI records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/using-pack-table-ci-record.md).

10. Select the more options icon \(\[Omitted image "options-icon.png"\] Alt text: More Options icon.\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/decommision-an-inventory-record.md).

11. Select **Submit**.

    The inventory record is created for the equipment type that you’ve selected.


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/delete-inventory-record.md).

-   **[Review and update the telecommunications equipment details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-equipment.md)**  
Review and update a network asset instance for your telecommunications equipment. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.

**Parent Topic:**[Manually creating and reviewing your network asset instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-telecommunications-network-inventory.md)

**Related topics**  


[Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md)


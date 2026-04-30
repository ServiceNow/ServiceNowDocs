---
title: Define the card details
description: Review, update, or create a network asset instance for a card that you use in your telecommunications equipment. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manually create and review your network asset instances, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Define the card details

Review, update, or create a network asset instance for a card that you use in your telecommunications equipment. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

The equipment ports can be physical or logical \(virtual\). The network interface data includes the port availability, bandwidths, slots, software version, MAC address, firmware manufacturer, and version. When you create a card record, it creates a corresponding configuration item \(CI\) record in the Card \[cmdb\_ci\_ni\_interface\_card\] table. To learn more, see [Data model](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Cards**.

3.  Select **New**.

4.  On the **Details** tab, in the Card section, fill in the general information for the card.

    [Card form](../reference/tni-interface-card-form.md) describes fields that are unique to the Card form.

    To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](../reference/commonly-used-tni-identification-fields.md).

5.  On the **Details** tab, in the Configuration section, fill in the configuration information for the card.

    The following table lists the fields that are unique to the Configuration section.

    To learn about the remaining configuration fields that are common to most of the Inventory menu forms, see [Commonly used network asset instance configuration fields](../reference/commonly-used-tni-configuration-fields.md).

<table id="table_zxs_tmt_gtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software Version

</td><td>

Version of the firmware that is used in this network asset.

</td></tr><tr><td>

MAC Address

</td><td>

Assigned Media Access Control \(MAC\) address for the network asset. It’s the network address that is used in communications within a network segment.

</td></tr><tr><td>

Firmware manufacturer

</td><td>

Manufacturer of the firmware.

</td></tr><tr><td>

Firmware version

</td><td>

Version of the firmware that is used in this network asset.

</td></tr></tbody>
</table>6.  To create the Telecommunications Network Inventory attributes for the Card form, click **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you click **Save** without clicking **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Click **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Card form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn't appear when you reopen the CI record.

9.  To add the attachments, such as graphics or documents, click the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

11. To view the Dependency views map, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the specific network asset and the relationships between the CIs.

12. To view the visual representation of the selected record, select **Open Map** button.

    **Note:** Install CMDB Workspace 3.5.0 or greater version to get this button in your instance. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0) or Service Graph Workspace .

13. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Attribute pack for CI records](../concept/using-pack-table-ci-record.md).

14. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).

15. To view the associated network inventories, select the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Manually create and review your network asset instances](../concept/creating-telecommunications-network-inventory.md)


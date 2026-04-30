---
title: Define the logical connection details
description: Review, update, or create a network asset instance for a logical or virtual port connection on your network interface cards. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Manually creating and reviewing your network asset instances, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Define the logical connection details

Review, update, or create a network asset instance for a logical or virtual port connection on your network interface cards. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

A logical connection typically represents the multiple physical connections on an interface card. The logical connection data includes the link types, bandwidths, port, and site.

When you create a logical connection record, it creates a corresponding configuration item \(CI\) record in the Logical Connection \[cmdb\_ci\_ni\_logical\_path\] table. To learn more, see [Data model for Telecommunications Network Inventory](../concept/uses-for-network-inventory-data.md).

The **Overview** tab in the logical connection record displays a consolidated detail of the logical connection, its connection elements, and A and Z ends. You can customize the connection elements table by creating a custom implementation for the extension point `sn_ni_adv.TNIConnectionOverview`. Also, you can decide the number of rows in this table by setting the system property `sn_ni_adv.clr_max_rows`. The default value for this property is 500.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then select **Inventory** &gt; **Logical Connections**.

    **Note:** You can also access the logical connection list by selecting the **Logical connection** count in the Network entities. Logical connection count is under the categories widget of the Network Inventory Workspace landing page. To learn more, see [Reviewing and updating your network inventory with the Network Inventory Workspace](../concept/tni-workspace.md).

3.  Select **New**.

4.  On the **Details** tab, in the Logical Connection section, fill in the general information for the logical connection.

    To learn more about the fields that are unique to the Logical Connection form, see [Logical Connection form](../reference/tni-logical-connection-forms.md#).

    To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](../reference/commonly-used-tni-identification-fields.md).

5.  On the **Details** tab, in the Configuration section, fill in the configuration information for the logical connection.

    To learn more about the fields that are unique to the Configuration section, see [Logical Connection form - Configuration](../reference/tni-logical-connection-forms.md#).

    To learn about the remaining configuration fields that are common to most of the Inventory menu forms, see [Commonly used network asset instance configuration fields](../reference/commonly-used-tni-configuration-fields.md).

6.  To create the Telecommunications Network Inventory attributes for the Logical Connection form, select **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates the TNI CI Attributes record in the CI table as well as the Telecommunications Network Inventory CI Attributes tables and makes a relationship with the CI record.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record. In the network inventory workspace, the **Set Inventory Attributes** is visible only for the Telecommunications Network Inventory roles.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Logical Connection form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn't appear when you reopen the CI record.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

11. To view the visual representation of the selected record, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Open Map**.

    **Note:** Install CMDB Workspace 3.5.0 or greater version to get this button in your instance. To learn more, see [CMDB Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280/3.5.0).

12. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Using an attribute pack for a CI record](../concept/using-pack-table-ci-record.md).

13. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).

14. To view the associated network inventories, select the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Modeling your Telecommunications Network Inventory workflow](../concept/telecommunications-network-inventory-workflow.md)


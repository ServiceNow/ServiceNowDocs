---
title: Define the datacenter details
description: Define your datacenter record in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each datacenter, including the network centers, buildings, floors, and rooms where your network assets are located.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Define the datacenter details

Define your datacenter record in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each datacenter, including the network centers, buildings, floors, and rooms where your network assets are located.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

Your datacenter is a secure facility that houses critical IT and network infrastructure needed to support the telecommunications network. Datacenter records enable you to view all network assets at a specific location. A datacenter has details about the location, building, floor, and all network assets placed at that location.

When you create a datacenter record, it creates a corresponding configuration item \(CI\) record in the data center \[cmdb\_ci\_datacenter\] table. Datacenter is a subcategory of a network site.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon..](../image/ni-workspace-list-icon.png)\) and then go to **Sites** &gt; **Data Centers**.

    You can view the datacenters that you manage by going to **Sites** &gt; **My Sites**.

3.  Select **New**.

4.  On the **Details** tab, fill in the fields.

    To learn more about the fields that are unique to the Data Center form, see [Network site form](../reference/tni-network-site-form.md).

    To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](../reference/commonly-used-tni-identification-fields.md).

5.  On the **Details** tab, in the Site Details section, fill in the site detail information.

    The following table lists the fields that are unique to the Site Details section.

    To learn about the remaining configuration fields that are common to most of the Inventory menu forms, see [Commonly used network asset instance configuration fields](../reference/commonly-used-tni-configuration-fields.md).

<table id="table_f3c_dmd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Serving wire center

</td><td>

Common Location Identifier Code \(CLLI\) code that represents the telephony company central office that is serving this network site with telephone service.

</td></tr><tr><td>

LATA

</td><td>

Assigned Local Access and Transport Area \(LATA\) code for the network asset. It represents the geographical area in the United States in which the network site is located.

</td></tr><tr><td>

Data center code

</td><td>

Identifier for this datacenter.

</td></tr><tr><td>

Altitude

</td><td>

Altitude of the network site that you select as feet or meters in the **Altitude units** field. The altitude measurement enables your enterprise to comply with Federal Aviation Administration \(FAA\) regulations.

</td></tr><tr><td>

Altitude units

</td><td>

Unit of measurement in which you’re expressing the altitude of the network site in the **Altitude** field. Select one of the following options:

-   **Feet**

Altitude of the network site that is measured in feet. This is the default value.

-   **Meters**

Altitude of the network site that is measured in meters.

</td></tr></tbody>
</table>6.  To create the Telecommunications Network Inventory attributes for the Network Site form, select **Set Inventory Attributes**.

    When you select the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you select **Save** without selecting **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Select **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Network Site form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn't appear when you reopen the CI record.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\).

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

11. View the visual representation of the selected record by selecting **Open Map**.

12. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Attribute pack for CI records](../concept/using-pack-table-ci-record.md).

13. To view the Dependency views map, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the specific network asset and the relationships between the CIs.

14. To view the associated network inventories, select the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.

15. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)


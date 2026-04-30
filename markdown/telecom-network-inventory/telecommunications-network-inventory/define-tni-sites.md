---
title: Define the network site details
description: Review, update, or create your network site records in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each network site, including the network centers, buildings, floors, and rooms where your equipment is located.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Manually creating and reviewing your network asset instances, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Define the network site details

Review, update, or create your network site records in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each network site, including the network centers, buildings, floors, and rooms where your equipment is located.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

Your network sites are those physical locations where you keep your network equipment. Network site records enable you to view all your equipment at a specific location. You can filter the locations by their assigned type, role, and function categories. To learn more, see [Viewing your network inventory configuration items with CMDB Workspace](../concept/viewing-network-inventory-using-cmdb-workspace.md).

When you create a network site record, it creates a corresponding configuration item \(CI\) record in the Network Site \[cmdb\_ci\_ni\_site\] table. To learn more, see [Data model for Telecommunications Network Inventory](../concept/uses-for-network-inventory-data.md).

The Telecommunications Network Inventory application stores the physical network connections, the logical network connections, and the resources that contain the overall network and the services provisioned on the network. The TNI data model adheres to a hierarchical structure. The foundation is the Network Site \(referred to here as a network site\).

The Network Site class represents the physical locations on the network where the equipment and resources are stored and maintained, and where the network connections originate and terminate. The network site has a reference to a physical location and derives the key attributes like the address, latitude, and longitude from it.

Although the network sites and locations are similar, their differences are important within the context of the TNI data model. A network site is a configuration item \(CI\) in TNI. It has an operational status, which is derived from the equipment and connections within the network site. As a CI, a network site can also be mapped as an inherent aspect of your service topology. The network site and location complement one another, which provides more value to your organization.

You can relate your physical locations to your network sites in TNI so that you can visualize these network sites on a map. Your organization can maximize the value of the network site and all the underlying inventory components that reside at the site. With the TNI data model, you can identify incidents, correlate events, and analyze the root cause of your network faults or outages.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Click the list icon \(![List icon..](../image/ni-workspace-list-icon.png)\) and then go to **Network Sites** &gt; **All Sites**.

    You can view the sites that you manage by going to **Network Sites** &gt; **My Sites**.

    **Note:** You can also access the Total Sites list by clicking the **Total sites** or **In maintenance sites** counts in the Network sites overview widget in the Network Inventory Workspace landing page. To learn more, see [Reviewing and updating your network inventory with the Network Inventory Workspace](../concept/tni-workspace.md).

3.  Click **New**.

4.  On the **Details** tab, in the Network Site section, fill in the fields.

    To learn more about the fields that are unique to the Network Site form, see [Network site form](../reference/tni-network-site-form.md).

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
</table>6.  To create the Telecommunications Network Inventory attributes for the Network Site form, click **Set Inventory Attributes**.

    When you click the **Set Inventory Attributes** button, it creates a reference in the CI table.

    **Note:**

    If you click **Save** without clicking **Set Inventory Attributes**, it creates a CI record but not a Telecommunications Network Inventory CI record.

7.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the Telecommunications Network Inventory attribute fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

8.  Click **Save**.

    The Telecommunications Network Inventory attribute fields are displayed on the Network Site form after you save the TNI CI Attributes form. The **Set Inventory Attributes** doesn't appear when you reopen the CI record.

9.  To add the attachments, such as graphics or documents, click the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Click **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

11. View the visual representation of the selected record by selecting **Open Map**.

12. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Add Packs** to capture the attributes for a configuration item \(CI\) record.

    To learn more, see [Using an attribute pack for a CI record](../concept/using-pack-table-ci-record.md).

13. To view the Dependency views map, select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Dependency View**.

    The Dependency Views map graphically displays the CIs that support the specific network asset and the relationships between the CIs.

14. To view the associated network inventories, click the brick icon \(![Brick icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the associated network inventories grouped by the individual network asset instances.

15. Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission** to decommission a CI record.

    To learn more, see [Decommission an inventory record](decommision-an-inventory-record.md).


## What to do next

-   If you want to establish relationships with the other network assets, enter the details in the related tabs. To learn more, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

-   To delete an inventory record, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

**Related topics**  


[Modeling your Telecommunications Network Inventory workflow](../concept/telecommunications-network-inventory-workflow.md)


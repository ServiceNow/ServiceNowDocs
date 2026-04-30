---
title: Network site form
description: The Network Site form enables you to define a network site where you house network equipment.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Network site form

The Network Site form enables you to define a network site where you house network equipment.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the network site where the equipment resides. The ServiceNow AI Platform uses this name to identify your network inventory. For example, `TROY IXC POP`.

</td></tr><tr><td>

NPANXX

</td><td>

Assigned NPA-NXX code for this network site:

-   This code is a combination of area codes \(NPAs\) and local exchanges \(NXXs\).
-   The combined code can contain the last four digits of up to 10,000 telephone numbers that are within a specific region. This region is associated with the central office for the assigned code.
-   For example, 858-335 is the NPA-NXX for the phone number 858-335-9500.

</td></tr><tr><td>

Location

</td><td>

Geographic location of the network site. Select the search icon \(![Search icon.](../image/search.png)\) and select a location from the Location hierarchy. To learn more about the Location hierarchy, see [6bb2f4f6af15321944e8adcad70bcb7dbc2d8557.dita](../task/define-tni-locations.md).

</td></tr><tr><td>

County

</td><td>

Name of the county in which the network site is located.

</td></tr><tr><td>

Region

</td><td>

Name of the geographic region in which the network site is located.

</td></tr><tr><td>

POTS number

</td><td>

Plain Old Telephone Service number \(POTS\) that is associated with this network site.

</td></tr></tbody>
</table>**Note:** To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](commonly-used-tni-identification-fields.md).

**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[ca1a77be2c4d9d7714f11ba6f1f20b14e07bb48f.dita](../task/define-tni-sites.md)


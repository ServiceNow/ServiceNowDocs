---
title: Equipment Holder form
description: The Equipment Holder form enables you to create, review, and modify the network asset details for an equipment holder.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Equipment Holder form

The Equipment Holder form enables you to create, review, and modify the network asset details for an equipment holder.

<table id="table_m2n_5nj_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Physical orientation of the slots in this network asset:

-   **--None--**

No specific physical slot orientation.

-   **Horizontal**

Horizontal slot orientation.

-   **Vertical**

Vertical slot orientation.


</td></tr><tr><td>

Serial number

</td><td>

Total number of equipment holder units, both occupied and available, in this network asset.

</td></tr><tr><td>

Asset

</td><td>

Number of equipment holder units that are in use in this network asset.

</td></tr><tr><td>

Support group

</td><td>

Number of equipment holder units that are available for use in this network asset.

</td></tr><tr><td>

Life Cycle Stage

</td><td>

Stage of the life cycle that this network asset is in:

-   **Deploy**

Network asset that is deployed in your network.

-   **Design**

Network asset that is being used for design purposes.

-   **End of life**

Network asset that is at the end of its useful life.

-   **Inventory**

Network asset that is an inventory item in use in the network.

-   **End of life**

Network asset that is missing and can't be located.

-   **Operational**

Network asset that is operational.

-   **Purchase**

Network asset that is in the purchase phase of its life.


</td></tr><tr><td>

Managed by

</td><td>

Name of the person who manages this network asset. Select the search icon \(![Search icon.](../image/search.png)\) and select a user from the listing.

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Status of the network asset as it relates to the life cycle stage that it is in:

-   **In Maintenance**

Network asset that is currently in maintenance.

-   **In Use**

Network asset that is currently in use.

-   **Pending Retirement**

Network asset that is currently in maintenance.


</td></tr><tr><td>

Model ID

</td><td>

Manufacturer's model identification number for this network asset.

</td></tr><tr><td>

Alarmable

</td><td>

Option that designates if an alarm system can be assigned to this network asset.

</td></tr></tbody>
</table><table id="table_f3c_dmd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(![Search icon.](../image/search.png)\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](../task/add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Model number

</td><td>

Manufacturer's model number for this network asset.

</td></tr><tr><td>

Orientation

</td><td>

Physical orientation of the slots in this network asset:

-   **--None--**

No specific physical slot orientation.

-   **Horizontal**

Horizontal slot orientation.

-   **Vertical**

Vertical slot orientation.


</td></tr><tr><td>

Unit position

</td><td>

Unit position of this network asset.

</td></tr><tr><td>

Network Domain

</td><td>

Domain of ownership and responsibility for this network asset or connection. Select one of the following options:-   **Mobility**

Network asset that is associated with the mobility equipment domain.

-   **Telco**

Network asset that is associated with the Telco equipment domain.

-   **Core**

Network asset that is associated with the core equipment domain.


</td></tr><tr><td>

Units occupied

</td><td>

Total number of equipment holder units, both occupied and available, in this network asset.

</td></tr><tr><td>

Units in use

</td><td>

Number of equipment holder units that are in use in this network asset.

</td></tr><tr><td>

Units available

</td><td>

Number of equipment holder units that are available for use in this network asset.

</td></tr><tr><td>

Comments

</td><td>

Free form text that is used to comment on a network asset. For example, `Duty tech is Rahul Dev`.

</td></tr><tr><td>

Allotted Electric Power

</td><td>

Maximum power allotted to the asset.**Note:**

-   To maintain the power capacity of the rack/cabinet, it’s essential to incorporate a minimum value of 10 Watts.
-   By default, the value is converted to Kilowatts \(KW\), in the capacity metric and following is the conversion formula
    -   Watts \(W\) - &lt;power-in-watts&gt; / 1000
    -   Megawatts \(MW\) - 1000 \* &lt;power-in-mega-watts&gt;
    -   Horsepower \(HP\) - 0.746 \* &lt;power-in-horsepower&gt;

</td></tr><tr><td>

Allotted Electric Power unit

</td><td>

Units in which the allotted electric power of the asset is measured. Select any one of the following units.-   Watts \(W\)
-   Kilowatts \(KW\)
-   Megawatts \(MW\)
-   Horsepower \(HP\)

</td></tr><tr><td>

Unit of Measure System

</td><td>

Measurement type based on which the **Max weight capacity unit** is fetched. Select any one of the following measurement types.-   Metric
-   US Imperial

</td></tr><tr><td>

Max weight capacity

</td><td>

Maximum capacity of assets.**Note:** By default, the value is converted to Pounds \(lbs\), in the capacity metric and following is the conversion formula

-   Ounces: &lt;weight-in-ounces&gt; / 16
-   Grams: &lt;weight-in-grams&gt; / 453.59
-   Kilograms: 2.204 \* &lt;weight-in-kilograms&gt;

</td></tr><tr><td>

Max weight capacity unit

</td><td>

Unit in which weight of the asset is measured. Select any one of the following.-   Grams \(g\)

**Note:** This field is only accessible when the Metric system is used for unit of measurement.

-   Kilograms \(kg\)

**Note:** This field is only accessible when the Metric system is used for unit of measurement.

-   Ounces \(oz\)

**Note:** This field is only accessible when the US Imperial system is used for unit of measurement.

-   Pounds \(lbs\)

**Note:** This field is only accessible when the US Imperial system is used for unit of measurement.


</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[050fc5155699cbc109ee8faad362b47d0db60252.dita](../task/define-tni-equipment-holders.md)


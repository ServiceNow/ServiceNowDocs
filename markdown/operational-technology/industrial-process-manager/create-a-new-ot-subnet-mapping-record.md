---
title: Create a new OT subnet mapping record
description: Create a new OT subnet mapping to associate with an equipment model entity.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Automated mapping of OT devices to the Equipment Model, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Create a new OT subnet mapping record

Create a new OT subnet mapping to associate with an equipment model entity.

## Before you begin

Role required: sn\_ot\_amazing\_write or sn\_ot\_amazing\_admin

**Note:** When creating new OT subnet mapping records, by default the new records are inactive. To automatically map records when the OT device mapping flow triggers, OT subnet mapping records must be active.

## Procedure

1.  Navigate to **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Entities**.

2.  Select the site or equipment model entity you want to create a new mapping for.

    **Note:** Subnet mapping also supports Discovery created configuration items \(CIs\) for ISA equipment models.

3.  Select the **Mapped OT Subnets** related list, then select **New**.

4.  On the form, fill in the fields.

5.  <table id="table_y3j_nmx_mtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Zone or VLAN name for the subnet.

</td></tr><tr><td>

Site

</td><td>

From the Lookup, select the ISA site from the list of available sites if not already populated.

</td></tr><tr><td>

Type

</td><td>

Select the subnet type from these options:-   IP Range - a subset of IP addresses in a subnet
-   IP Network - the entire subnet, in CIDR notation


</td></tr><tr><td>

Starting IP Address

</td><td>

Starting IP for the IP Range This field is visible when Type is IP Range.

</td></tr><tr><td>

Ending IP address

</td><td>

Ending IP for the IP Range This field is visible when Type is IP Range.

</td></tr><tr><td>

Source name

</td><td>

Name of the source, such as NetDB or Firewall.

</td></tr><tr><td>

Firewall Name

</td><td>

Name of the firewall managing the zone if applicable.

</td></tr><tr><td>

Description

</td><td>

Description for the subnet mapping.

</td></tr><tr><td>

Active

</td><td>

Select Active to include the subnet in automated mapping when the OT Subnet Mapping scheduled flow executes.

</td></tr><tr><td>

Equipment model entity

</td><td>

From the Lookup, select the equipment model entity from the list of available entities if not already populated.

</td></tr><tr><td>

Subnet

</td><td>

Enter the subnet address \(CIDR format\). This field is visible when Type is IP Network.

</td></tr><tr><td>

Location

</td><td>

Add a location to the subnet record to automatically add or update the location in the mapped OT devices.**Note:** The location is mapped based on the sn\_otsm.subnet\_mapping.location\_auto\_update system property. For more information about system properties used for OT subnet mapping, see [System properties used by the OT subnet mapping feature](../reference/system-properties-used-by-automated-mapping-feature.md).

</td></tr><tr><td>

Interface name

</td><td>

Name for the firewall interface if applicable.

</td></tr><tr><td>

VLAN ID

</td><td>

Specify the VLAN ID if applicable.

</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Automated mapping of OT devices to the Equipment Model](automate-mappings-between-ot-assets-and-equipment-model-entity.md)


---
title: Import model excel template
description: Learn about the fields and structure of the Excel template used to define network element models and their hierarchical relationships for bulk import.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-05-09"
reading_time_minutes: 4
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Import model excel template

Learn about the fields and structure of the Excel template used to define network element models and their hierarchical relationships for bulk import.

## Import model excel template overview

The import model template is a structured Excel file used to define network element models and their hierarchical relationships for bulk import into the application. Each row represents one record that is imported into the target system, and each column maps to a field in the target table. Entity ID uniquely identifies each row and acts as a key within the spreadsheet. It must be unique across all rows and is not mapped to any target table field. Parent entity ID and Root entity ID reference these keys to establish the parent-child hierarchy between components. The referenced Entity ID must already exist in the Entity ID column before it can be used as a parent or root reference. You do not need a separate row for the model relationship — the model and its relationship to the parent component can be defined in a single row. If the model already exists in the system, the record is skipped. If it does not exist, the model is created along with the model relationship. Model class determines the type of model being represented — Network Equipment Model, Network Holder Model, Network Card Model, or Network Interface Model. Model category must be a valid value from the model category table and determines which tables are used for inserting records and which tables are considered during equipment instantiation. The Excel template is created based on the Import model template \[sn\_ni\_adv\_import\_model\_template\] table. An admin can customize the template and update it as required. To download the template with sample data, select Create Excel template on the Import model request form. Only Sheet 1 is considered during import. All other sheets are ignored.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity ID

</td><td>

Unique identifier for each row in the template. Must be unique across all rows. Acts as a key within the spreadsheet to establish parent-child relationships using the Parent entity ID and Root entity ID fields. Not mapped to any target table field.

</td></tr><tr><td>

Model class

</td><td>

The type of network element the row represents. Accepted values are Network equipment model, Network holder model, Network card model, Facility model and Network interface model.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the manufacturer or vendor of the network element.

</td></tr><tr><td>

Model number

</td><td>

The manufacturer's model number for the component.

</td></tr><tr><td>

Relationship type

</td><td>

Defines how the component relates to its parent. Accepted values are Equipment to Slot

Equipment to Network Interface

Slot to Card

Card to Slot

Card to Network Interface

Physical Connection to Logical Connection

Logical Connection to Logical Connection

Physical Connection to Network Interface

Logical Connection to Network Interface

Rack/Cabinet to Rack/Cabinet Slot

Rack/Cabinet Slot to Equipment

Rack/Cabinet Slot to Shelf

Interface to Interface

Logical Connection to Channel

Cable to Strand

Cable to Physical Connection

Multi Chassis to Equipment

Multi Chassis to Rack

</td></tr><tr><td>

Parent entity ID

</td><td>

The Entity ID of the parent component. The referenced ID must already exist in the Entity ID column. Establishes the hierarchical position of this component within the model structure.

</td></tr><tr><td>

Root entity ID

</td><td>

The number of child elements of this type associated with the parent component.

</td></tr><tr><td>

Count

</td><td>

The number of child elements of this type associated with the parent component.

</td></tr><tr><td>

Sequence

</td><td>

The order in which child elements are listed under the parent component.

</td></tr><tr><td>

Model category

</td><td>

The category of the model. Must be a valid value from the model category table. Determines which tables are used for inserting records and which tables are considered during equipment instantiation.

</td></tr><tr><td>

Owner

</td><td>

The owner of the model record.

</td></tr><tr><td>

Height \(U\)

</td><td>

The height of the component in rack units. Applies to rack-mounted equipment and equipment holders.

</td></tr><tr><td>

CLEI code

</td><td>

The Common Language Equipment Identifier assigned by the manufacturer to the component.

</td></tr><tr><td>

Slots occupied

</td><td>

The number of slots the component occupies in its parent holder.

</td></tr><tr><td>

Interface start number

</td><td>

The starting number used when auto-naming network interfaces associated with this component. Links the model to a corresponding catalog item in the application.

</td></tr><tr><td>

Orientation

</td><td>

The mounting orientation of the component. The allowed value is "Vertical" or "Horizontal"

</td></tr><tr><td>

Port bandwidth

</td><td>

The bandwidth capacity of a network interface port.

</td></tr><tr><td>

Slot naming pattern

</td><td>

Controls how the application automatically generates names for child slot elements associated with this component.

</td></tr><tr><td>

Interface naming pattern

</td><td>

Controls how the application automatically generates names for child interface elements associated with this component.

</td></tr><tr><td>

Weight

</td><td>

The physical weight of the component.

</td></tr><tr><td>

Weight unit

</td><td>

The unit of measurement for the Weight field, such as kg or lb.

</td></tr><tr><td>

Rated power

</td><td>

The power consumption rating of the component.

</td></tr><tr><td>

Power unit

</td><td>

The unit of measurement for the Rated power field, such as W or kW.

</td></tr><tr><td>

Max weight capacity

</td><td>

The maximum weight the component can support. Applies to racks, cabinets, and equipment holders. Allowed value is "2 Post" or "4 Post"

</td></tr><tr><td>

Max weight capacity unit

</td><td>

The unit of measurement for the Max weight capacity field.

</td></tr><tr><td>

Post type

</td><td>

The post type of the rack or cabinet holder.

</td></tr><tr><td>

RU naming pattern

</td><td>

Controls how the application automatically generates names for rack unit positions within the component.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Import a model](../task/import-models.md)


---
title: Import model Excel template
description: Learn about the fields and structure of the Excel template used to define network element models and their hierarchical relationships for bulk import.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/import-model-excel-template.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 4
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Import model Excel template

Learn about the fields and structure of the Excel template used to define network element models and their hierarchical relationships for bulk import.

## Import model excel template overview

The import model template is a structured Excel file used to define network element models and their hierarchical relationships for bulk import into the application. Each row represents one record that is imported into the target system, and each column maps to a field in the target table.

You do not need a separate row for the model relationship. The model and its relationship to the parent component can be defined in a single row. If the model already exists in the system, the record is skipped. If it does not exist, the model is created along with the model relationship.

Model class determines the type of model being represented — Network Equipment Model, Network Holder Model, Network Card Model, or Network Interface Model. Model category must be a valid value from the model category table and determines which tables are used for inserting records and which tables are considered during equipment instantiation. The Excel template is created based on the Import model template table \[sn\_ni\_adv\_import\_model\_template\]. An admin can customize the template and update it as required. To download the template with sample data, select **Create Excel template** on the Import model request form. Only Sheet 1 is considered during import. All other sheets are ignored.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity ID

</td><td>

Unique identifier for each row in the template. The ID must be unique across all rows. The ID acts as a key within the spreadsheet to establish parent-child relationships using the Parent entity ID and Root entity ID fields. The ID is not mapped to any target table field.The referenced Entity ID must already exist in the Entity ID column before it can be used as a parent or root reference.

</td></tr><tr><td>

Model class

</td><td>

The type of network element the row represents. Accepted values are:-   Network equipment model
-   Network holder model
-   Network card model
-   Facility model
-   Network interface model

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the manufacturer or vendor of the network element.

</td></tr><tr><td>

Model number

</td><td>

Model number of the manufacturer for the component.

</td></tr><tr><td>

Relationship type

</td><td>

Relationship between the component relates and its parent. Accepted values are:-   Equipment to Slot
-   Equipment to Network Interface
-   Slot to Card
-   Card to Slot
-   Card to Network Interface
-   Physical Connection to Logical Connection
-   Logical Connection to Logical Connection
-   Physical Connection to Network Interface
-   Logical Connection to Network Interface
-   Rack/Cabinet to Rack/Cabinet Slot
-   Rack/Cabinet Slot to Equipment
-   Rack/Cabinet Slot to Shelf
-   Interface to Interface
-   Logical Connection to Channel
-   Cable to Strand
-   Cable to Physical Connection
-   Multi Chassis to Equipment
-   Multi Chassis to Rack

</td></tr><tr><td>

Parent entity ID

</td><td>

Entity ID of the parent component. The referenced ID must already exist in the Entity ID column. This ID establishes the hierarchical position of this component within the model structure.

</td></tr><tr><td>

Root entity ID

</td><td>

Entity ID of the root component in the hierarchy. The referenced ID must already exist in the Entity ID column.

</td></tr><tr><td>

Count

</td><td>

Number of child elements of this type associated with the parent component.

</td></tr><tr><td>

Sequence

</td><td>

Order in which child elements are listed under the parent component.

</td></tr><tr><td>

Model category

</td><td>

Category of the model. The category must be a valid value from the model category table. The value determines which tables are used for inserting records and which tables are considered during equipment instantiation.

</td></tr><tr><td>

Owner

</td><td>

Owner of the model record.

</td></tr><tr><td>

Height \(U\)

</td><td>

Height of the component in rack units. This height applies to rack-mounted equipment and equipment holders.

</td></tr><tr><td>

CLEI code

</td><td>

Common Language Equipment Identifier assigned by the manufacturer to the component.

</td></tr><tr><td>

Slots occupied

</td><td>

Number of slots the component occupies in its parent holder.

</td></tr><tr><td>

Interface start number

</td><td>

Starting number used when auto-naming network interfaces associated with this component. This number links the model to a corresponding catalog item in the application.

</td></tr><tr><td>

Orientation

</td><td>

Mounting orientation of the component. The allowed values are:-   Vertical
-   Horizontal"

</td></tr><tr><td>

Port bandwidth

</td><td>

Bandwidth capacity of a network interface port.

</td></tr><tr><td>

Slot naming pattern

</td><td>

Pattern that controls how the application automatically generates names for child slot elements associated with this component.

</td></tr><tr><td>

Interface naming pattern

</td><td>

Pattern that controls how the application automatically generates names for child interface elements associated with this component.

</td></tr><tr><td>

Weight

</td><td>

Physical weight of the component.

</td></tr><tr><td>

Weight unit

</td><td>

Unit of measurement for the Weight field, such as kg or lb.

</td></tr><tr><td>

Rated power

</td><td>

Power consumption rating of the component.

</td></tr><tr><td>

Power unit

</td><td>

Unit of measurement for the Rated power field, such as W or kW.

</td></tr><tr><td>

Max weight capacity

</td><td>

Maximum weight that the component can support. This applies to racks, cabinets, and equipment holders. Allowed values are:-   2 Post
-   4 Post

</td></tr><tr><td>

Max weight capacity unit

</td><td>

Unit of measurement for the **Max weight capacity** field.

</td></tr><tr><td>

Post type

</td><td>

Post type of the rack or cabinet holder.

</td></tr><tr><td>

RU naming pattern

</td><td>

Naming pattern that controls how the application automatically generates names for rack unit positions within the component.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Import a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-models.md)


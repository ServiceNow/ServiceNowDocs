---
title: Retail Core data model tables
description: Tables configured within the Retail Operations application enable you to determine the data model, tasks, and product offerings for your Retail Operations workflows.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Retail Core data model, Retail Core reference, Retail Core, Retail]
---

# Retail Core data model tables

Tables configured within the Retail Operations application enable you to determine the data model, tasks, and product offerings for your Retail Operations workflows.

## Retail Organization table

The Retail organization \[sn\_retail\_organization\] table stores information about your retail organizations.

This has a one-to-one relationship with the Service Organization \[sn\_customer\_service\_organization\] table.

Service Organization \[sn\_customer\_service\_organization\] has an attribute of Retail Organization.

Retail-specific attributes should be maintained in this table.

<table id="table_y31_2wr_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ownership

</td><td>

The ownership type of this retail organization. Options are:-   Company owned
-   Franchise

</td></tr><tr><td>

Brand

</td><td>

The associated brand of this retail organization.

</td></tr><tr><td>

Service Organization

</td><td>

The associated service organization.

</td></tr><tr><td>

Retail Subtype

</td><td>

The retail subtype. Options are:-   Store
-   Region
-   Division
-   Area
-   District

</td></tr><tr><td>

Flagship

</td><td>

Indicates whether this is considered a flagship retail organization location.

</td></tr></tbody>
</table>## Retail case table

The Retail case \[sn\_retail\_case\] table stores information about your retail case types and provides the basis for retail case creation.

This table extends the Customer Service Management case table. All functionality utilized through the Customer Service Management case remains intact.

This table can be extended to further expand the flow and logic for retail use cases.

|Field|Description|
|-----|-----------|
|Number|Numerical code indicating the case number for this request.|
|Requested by|Internal user associated with this request.|
|Requesting Retail Organization|Retail organization this request is being created for.|
|Supporting Retail Organization|Retail organization responsible for fulfilling this request.|
|Short description|A short description of this request's purpose.|
|Description|A detailed description of this request's purpose.|
|Opened|Date and time at which this request was opened.|
|Priority|Sequence in which this case must be resolved, based on impact and urgency.|
|Assignment Group|The associated assignment group responsible for working on this request.|
|Assigned to|Person primarily responsible for working on this request.|

**Parent Topic:**[Retail Core data model](rahi-retail-data-model.md)


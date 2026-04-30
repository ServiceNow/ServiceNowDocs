---
title: Retail organization data model tables
description: Tables configured within the Retail Operations application enable you to determine the data model, tasks, and product offerings for your Retail Operations workflows.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Retail organization data model, Retail reference, Retail]
---

# Retail organization data model tables

Tables configured within the Retail Operations application enable you to determine the data model, tasks, and product offerings for your Retail Operations workflows.

## Retail organization table

The Retail organization \[sn\_retail\_organization\] table stores information about your retail organizations.

The Retail organization \[sn\_retail\_organization\] table has a one-to-one relationship with the Service Organization \[sn\_customer\_service\_organization\] table.

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

The Retail case \[sn\_retail\_case\] table extends the Customer Service Management case table. All functionality used through the Customer Service Management case remains intact.

The Retail case \[sn\_retail\_case\] table can be extended to expand the flow and logic for retail use cases.

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

**Parent Topic:**[Retail organization data model](rahi-retail-data-model.md)


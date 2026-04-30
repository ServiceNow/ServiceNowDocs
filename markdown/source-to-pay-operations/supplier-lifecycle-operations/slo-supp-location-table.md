---
title: Supplier Location table
description: The Supplier Location \[sn\_slm\_m2m\_location\] table stores important information about the geographical location of a supplier.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Primary data tables for Supplier Lifecycle Operations, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier Location table

The Supplier Location \[sn\_slm\_m2m\_location\] table stores important information about the geographical location of a supplier.

## Supplier Location \[sn\_slm\_m2m\_location\] table

The Supplier Location \[sn\_slm\_m2m\_location\] table contains the following fields.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Supplier

</td><td>

Reference

</td><td>

Name of the supplier.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the supplier location.

</td></tr><tr><td>

Street

</td><td>

String

</td><td>

The street address of the supplier location.

</td></tr><tr><td>

City

</td><td>

String

</td><td>

The city of the supplier location.

</td></tr><tr><td>

State/Province

</td><td>

String

</td><td>

The state of the supplier location.

</td></tr><tr><td>

Zip/Postal Code

</td><td>

String

</td><td>

The zip code of the supplier location.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

The country of the supplier location.

</td></tr><tr><td>

Latitude

</td><td>

Integer

</td><td>

The latitude coordinates of the supplier location.

</td></tr><tr><td>

Longitude

</td><td>

Integer

</td><td>

The longitude coordinates of the supplier location.

</td></tr><tr><td>

Category

</td><td>

List

</td><td>

The category that the supplier location belongs to. The choices are:-   Contracting address
-   Delivery address
-   Facility \(default\)
-   Headquarters
-   Invoice address
-   Service center

</td></tr></tbody>
</table>For more information, see [Supplier Lifecycle Operations data model](slo-data-model.md).

**Parent Topic:**[Primary data tables for Supplier Lifecycle Operations](slo-primary-data-tables.md)


---
title: Supplier Contact table
description: The Supplier Contact \[sn\_slm\_contact\_m2m\_supplier\] table stores information about supplier contacts and suppliers linked to them.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Primary data tables for Supplier Lifecycle Operations, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier Contact table

The Supplier Contact \[sn\_slm\_contact\_m2m\_supplier\] table stores information about supplier contacts and suppliers linked to them.

## Supplier Contact \[sn\_slm\_contact\_m2m\_supplier\] table

**Important:**

The Supplier Contact table is available from the Xanadu December 2024 release onwards.

Previously, the `Organization` field from the `Vendor Contact` table was used to fetch the mapping between the supplier contact and the supplier. From Xanadu December 2024 release onwards, the `Supplier Contact` table is used to fetch this mapping.

The Supplier Contact \[sn\_slm\_contact\_m2m\_supplier\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Supplier contact|Reference|Name of the supplier contact.|
|Supplier|Reference|Name of the supplier.|
|Default supplier|Boolean|Indicates whether the supplier is the default supplier for the supplier contact.|
|Primary contact|Boolean|Indicates whether the supplier contact is the primary contact for the supplier.|

For more information, see [Supplier Lifecycle Operations data model](slo-data-model.md).

**Parent Topic:**[Primary data tables for Supplier Lifecycle Operations](slo-primary-data-tables.md)


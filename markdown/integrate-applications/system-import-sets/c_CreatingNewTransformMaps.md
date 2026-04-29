---
title: Transform maps
description: A transform map is a set of field maps that determine the relationships between fields in an import set and fields in an existing ServiceNow table, such as Incident \[incident\] or User \[sys\_user\].
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Import sets, Imports, Workflow Data Fabric]
---

# Transform maps

A transform map is a set of field maps that determine the relationships between fields in an import set and fields in an existing ServiceNow table, such as Incident \[incident\] or User \[sys\_user\].

After creating a transform map, you can reuse it to map data from another import set to the same table.

The **Transform Maps** module enables an administrator to define destinations for imported data on any tables. Transform mapping can be as simple as a drag and drop operation to specify linking between source fields on an import set table and destination fields on any table. Use transform mapping to map source and destination fields dynamically.

For a video overview of transform maps, see the [Transform Maps](https://youtu.be/iMjSpK3OaUY?si=SzrhUInpF16Xon5) video on the ServiceNow Dev Program YouTube channel.

## Transform considerations

-   **Auto-mapping**

    Double-check that fields the system maps automatically are actually required. For example, encrypted passwords probably should not be mapped.

-   **Mapping reference fields**

    If you are mapping reference field data and the sys\_id does not exist, the sys\_id could potentially appear in the target record as the DisplayValue, and this may be undesirable.

    Field mapping a large number of reference fields incurs additional performance overhead because the system checks that the referenced sys\_id actually exists before performing choice actions at the field level.

    **Note:** You can bypass the performance overhead using transform scripts such as onBefore \(on the assumption that there is no requirement to validate the import of reference fields\). For example, `target.<field_name> = source.<field_name>`.


## Using multiple transform maps

Multiple transform maps can be applied to a single data source.

One import set row is created per transform map, which can cause a large number of temporary records to be generated.

**Note:** If you use multiple transform maps for the same import set, the transform creates multiple entries in the import set table.

## Run multiple transforms off a single import set

Users can select multiple transform maps during data import.

The selected transform maps will be executed on the same import set in the order specified.

## Transform map scripts

Transform Map scripts allow you to customize import operations using a robust programming interface to introduce advanced logic.

A transform map script executes as events occur while an import set is being transformed onto a ServiceNow table. Transform Map scripting is fully integrated into the ServiceNow scripting environment. There are two types of Transform Map scripts:

-   Explicit Transform Map scripts, which explicitly define mapping relationships
-   Transformation Event scripts, which modify the processing of events at different stages of a transformation


---
title: Practitioner specialty table
description: The Practitioner specialty \[sn\_hcls\_practitioner\_specialty\] table stores the association details of a specialty with a practitioner.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Practitioner specialty table

The Practitioner specialty \[sn\_hcls\_practitioner\_specialty\] table stores the association details of a specialty with a practitioner.

## Key features

-   Links the practitioner to multiple care specialties that the practitioner specializes in.
-   Enables supported care specialties models in the Healthcare code set \[sn\_hcls\_code\_set\] table.
-   Provides a reference to the practitioner and the code set of type care specialty.
-   Includes a reference to the practitioner type \(also modeled as a code set\).
-   Enables indicating whether location is the primary specialty for a practitioner.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_rj5_svs_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

True/False

</td><td>

Option to indicate whether the specialty is associated with the practitioner.

</td></tr><tr><td>

Practitioner

</td><td>

Reference

</td><td>

Person added as the practitioner.

</td></tr><tr><td>

Practitioner type

</td><td>

Reference

</td><td>

Type of the practitioner.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Specialty

</td><td>

Reference

</td><td>

Specialty of the practitioner.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)


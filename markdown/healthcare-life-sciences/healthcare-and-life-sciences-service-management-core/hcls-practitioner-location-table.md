---
title: Practitioner location table
description: The Practitioner location \[sn\_hcls\_practitioner\_facility\] table stores the details of the location at which a practitioner provides healthcare services.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Practitioner location table

The Practitioner location \[sn\_hcls\_practitioner\_facility\] table stores the details of the location at which a practitioner provides healthcare services.

## Key features

-   Links the practitioner to a healthcare location.
-   Enables providing a date range for that practitioner and location association.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_unw_q4t_mpb"><thead><tr><th>

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

Option to indicate whether the location is associated with the practitioner.

</td></tr><tr><td>

Effective from

</td><td>

Date

</td><td>

Start date of the period during which the practitioner is authorized to perform in the location.

</td></tr><tr><td>

Effective until

</td><td>

Date

</td><td>

End date of the period during which the practitioner is authorized to perform in the location.

</td></tr><tr><td>

Organization

</td><td>

Reference

</td><td>

Identity of the organization the practitioner represents or acts on behalf of.

</td></tr><tr><td>

Practitioner

</td><td>

Reference

</td><td>

Person added as the practitioner.

</td></tr><tr><td>

Location

</td><td>

Reference

</td><td>

The associated practitioners location name.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)


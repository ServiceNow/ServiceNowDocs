---
title: Practitioner location specialty table
description: The Practitioner location specialty \[sn\_hcls\_pract\_location\_specialty\] table stores the details about types of services that a practitioner can provide for an organization at a specific location.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Healthcare and Life Sciences data model tables, Healthcare and Life Sciences Service Management Core reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Practitioner location specialty table

The Practitioner location specialty \[sn\_hcls\_pract\_location\_specialty\] table stores the details about types of services that a practitioner can provide for an organization at a specific location.

## Key features

-   Links the practitioner location object to a specific care specialty and also the practitioner type.
-   Enables indicating whether location is the primary specialty for a practitioner.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_wss_rlz_mpb"><thead><tr><th>

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

Option to indicate whether the location and specialty mapping is in use.

</td></tr><tr><td>

Practitioner location

</td><td>

Reference

</td><td>

Location at which a practitioner provides a care specialty.

</td></tr><tr><td>

Practitioner type

</td><td>

Reference

</td><td>

Type of the practitioner.

</td></tr><tr><td>

Primary specialty

</td><td>

True/False

</td><td>

Option to indicate whether the specialty is the main specialty care provided at the location by a practitioner.

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


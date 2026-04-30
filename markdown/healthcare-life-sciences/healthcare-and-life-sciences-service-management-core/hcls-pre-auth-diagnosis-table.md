---
title: Pre-authorization diagnosis table
description: The Pre-authorization diagnosis \[sn\_hcls\_pre\_auth\_diagnosis\] table stores diagnosis information pertaining to a pre-authorization for healthcare services.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Pre-authorization diagnosis table

The Pre-authorization diagnosis \[sn\_hcls\_pre\_auth\_diagnosis\] table stores diagnosis information pertaining to a pre-authorization for healthcare services.

## Key features

-   Stores the diagnosis code for use with pre-authorizations.
-   Includes both pre-authorization and diagnosis information.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_ykg_4qj_rvb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pre-authorization request

</td><td>

Reference

</td><td>

Associated pre-authorization request.

</td></tr><tr><td>

Pre-authorization item

</td><td>

Reference

</td><td>

Associated pre-authorization item.

</td></tr><tr><td>

Diagnosis code

</td><td>

Reference

</td><td>

Code used to indicate the diagnosis given by a healthcare practitioner.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)


---
title: Claim diagnosis table
description: The Claim diagnosis table \[sn\_hcls\_claim\_diagnosis\] stores diagnosis information for claims.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Claim diagnosis table

The Claim diagnosis table \[sn\_hcls\_claim\_diagnosis\] stores diagnosis information for claims.

## Key features

-   Stores the diagnosis code for use with claims.
-   Includes both claim and diagnosis information.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_azg_z42_rvb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Claim

</td><td>

Reference

</td><td>

Associated claim submitted on behalf of a patient to a payer organization.

</td></tr><tr><td>

Claim line

</td><td>

Reference

</td><td>

Associated claim line containing details of the items pertaining to the claim header.

</td></tr><tr><td>

Diagnosis code

</td><td>

Reference

</td><td>

Code used to indicate the diagnosis given by a healthcare practitioner.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)


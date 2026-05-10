---
title: Components installed with Workplace Lease Administration
description: Several types of components are installed with activation of the Workplace Lease Administration application, including user roles and tables.
locale: en-US
release: australia
product: Workplace Lease Administration
classification: workplace-lease-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workplace Lease Administration references, Workplace Lease Administration, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Lease Administration

Several types of components are installed with activation of the Workplace Lease Administration application, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles

<table id="table_lqh_3b4_wvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_wsd\_la.manager

</td><td>

Create and edit lease contract records. Updates the spaces that are part of a lease contract.

</td><td>

-   sn\_wsd\_la.user
-   contract\_manager

</td></tr><tr><td>

sn\_wsd\_la.admin

</td><td>

Performs the Lease tracking module setup

</td><td>

-   sn\_wsd\_la.manager
-   sn\_wsd\_central.workspace\_user

</td></tr><tr><td>

sn\_wsd\_la.user

</td><td>

Read all lease contract information. No create or edit access.

</td><td>

-   sn\_wsd\_central.workspace\_user
-   contract\_manager

</td></tr><tr><td>

sn\_wsd\_la.workplace\_central\_user

</td><td>

Enables users to access the Workplace Lease Administration application in Workplace Central.

</td><td>

None

</td></tr></tbody>
</table>## Tables

<table id="table_x31_wb4_wvb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Contract\[sn\_wsd\_la\_workplace\_contract\]

</td><td>

Extends the Application Contract table and stores workplace contracts.

</td></tr><tr><td>

Workplace Contract Service\[sn\_wsd\_la\_workplace\_contract\_service\]

</td><td>

Stores workplace contract services related to the contract.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Lease Administration references](../concept/workplace-lease-references.md)

**Related topics**  


[Workplace contract new record form](workplace-contract-form.md)

[Scripts installed with Workplace Lease Administration](scripts-lease-admin.md)


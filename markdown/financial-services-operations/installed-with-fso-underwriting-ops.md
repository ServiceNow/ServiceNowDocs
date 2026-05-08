---
title: Components installed with Personal Lines Underwriting
description: Several types of components are installed with installation of the Personal Lines Underwriting application \(sn\_ins\_underwrite\), including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Personal Lines Servicing, Property and Casualty Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Personal Lines Underwriting

Several types of components are installed with installation of the Personal Lines Underwriting application \(sn\_ins\_underwrite\), including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

The Personal Lines Underwriting plugin \(sn\_ins\_underwrite\) is automatically installed with the Personal Lines Servicing plugin.

Personal Lines Underwriting manages the underwriting tasks that are used in workflows across Financial Services Operations applications.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Insurance underwriting adminsn\_ins\_underwrite.admin

</td><td>

Application-specific system administrator role that can grant access to all insurance underwriting operations data.Users with this role have read, write, and create access to the Insurance Underwriting Operations tables.

</td><td>

sn\_ins\_underwrite.underwriter

</td></tr><tr><td>

Personal insurance underwriter\[sn\_ins\_underwrite.b2c\_underwriter\]

</td><td>

-   View the overall status of personal underwriting tasks for insurance policy services
-   Work on personal underwriting tasks

</td><td>

-   sn\_bom.b2c\_agent
-   sn\_bom.ins\_policy\_viewer
-   sn\_ins\_policy\_b2c.info\_viewer
-   sn\_ins\_policy\_b2c.homeowner\_policy\_viewer
-   sn\_ins\_policy\_b2c.auto\_policy\_viewer

</td></tr><tr><td>

Insurance underwriting viewersn\_ins\_underwrite.viewer

</td><td>

View underwriting tasks and related data for insurance policy services

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Underwriting Service Task \(Personal\)\[sn\_ins\_underwrite\_b2c\_task\]

</td><td>

Stores all underwriting tasks for personal policy service requests for all Financial Services Operations applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Personal Lines Servicing reference](../concept/ins-policy-ops-reference.md)


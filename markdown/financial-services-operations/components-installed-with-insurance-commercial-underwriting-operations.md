---
title: Components installed with Commercial Lines Underwriting
description: Several types of components are installed with installation of the Commercial Lines Underwriting application \(sn\_ins\_uw\_b2b\), including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Commercial Lines Servicing, Property and Casualty Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Commercial Lines Underwriting

Several types of components are installed with installation of the Commercial Lines Underwriting application \(sn\_ins\_uw\_b2b\), including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

The Commercial Lines Underwriting plugin \(sn\_ins\_uw\_b2b\) is automatically installed with the Commercial Lines Servicing plugin.

Commercial Lines Underwriting manages the underwriting tasks that are used in workflows across Financial Services Operations applications.

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

Commercial insurance underwriter\[sn\_ins\_uw\_b2b.underwriter\]

</td><td>

-   View the overall status of commercial underwriting tasks for insurance policy services
-   Work on commercial underwriting tasks

</td><td>

-   sn\_ins\_policy\_b2b.info\_viewer
-   sn\_bom.b2b\_agent
-   sn\_ins\_policy\_b2b.bop\_viewer
-   sn\_bom.ins\_policy\_viewer

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

</th></tr></thead><tbody><tr><td colspan="2">

Commercial Lines Underwriting

</td></tr><tr><td>

Commercial Underwriting Service Task \[sn\_ins\_uw\_b2b\_task\]

</td><td>

Stores all underwriting tasks for business policy service requests for all Financial Services Operations applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Commercial Lines Servicing reference](../concept/commercial-lines-servicing-reference.md)


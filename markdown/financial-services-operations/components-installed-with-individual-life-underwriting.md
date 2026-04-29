---
title: Components installed with Individual Life Underwriting
description: Several types of components are installed with activation of the Individual Life Underwriting plugin, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Individual Life Servicing, Life Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Individual Life Underwriting

Several types of components are installed with activation of the Individual Life Underwriting plugin, including tables and user roles.

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Individual insurance underwriting admin

 \[sn\_ins\_indiv\_uw.admin\]

</td><td>

Application-specific system administrator role that can grant access to all individual insurance underwriting operations data.Users with this role have read, write, and create access to the Individual Life Underwriting tables.

</td><td>

sn\_ins\_indiv\_uw.underwriter

</td></tr><tr><td>

Individual insurance underwriter\[sn\_ins\_indiv\_uw.underwriter\]

</td><td>

-   View the overall status of individual policy underwriting tasks for insurance policy services
-   Work on individual policy underwriting tasks

</td><td>

-   sn\_ins\_indiv\_life.viewer
-   sn\_ins\_indiv\_life.line\_writer
-   sn\_bom.indiv\_disab\_policy\_viewer
-   sn\_bom,b2b\_agent
-   sn\_bom.b2c\_agent

</td></tr><tr><td>

Individual insurance underwriting viewer\[sn\_ins\_indiv\_uw.viewer\]

</td><td>

View underwriting tasks and related data for individual insurance policy services

</td><td>

 

</td></tr></tbody>
</table>## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Individual Life Underwriting Service Task

 \[sn\_ins\_indiv\_uw\_task\]

</td><td>

Stores all underwriting tasks for individual policy service requests for all applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Individual Life Servicing reference](individual-life-servicing-reference.md)


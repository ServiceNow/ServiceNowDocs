---
title: Components installed with Group Life Underwriting
description: Several types of components are installed with activation of the Group Life and Disability Underwriting plugin, including tables and user roles.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Group Life Servicing reference, Setting up Group Life Servicing, Group Life Servicing, Life Insurance Servicing, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Components installed with Group Life Underwriting

Several types of components are installed with activation of the Group Life and Disability Underwriting plugin, including tables and user roles.

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Group insurance underwriting admin

 \[sn\_ins\_group\_uw.admin\]

</td><td>

Application-specific system administrator role that can grant access to all group insurance underwriting operations data.Users with this role have read, write, and create access to the Group Life Underwriting tables.

</td><td>

sn\_ins\_group\_uw.underwriter

</td></tr><tr><td>

Group insurance underwriter\[sn\_ins\_group\_uw.underwriter\]

</td><td>

-   View the overall status of group policy underwriting tasks for insurance policy services
-   Work on group policy underwriting tasks

</td><td>

-   sn\_ins\_group\_life.info\_viewer
-   sn\_ins\_group\_life.viewer
-   sn\_ins\_group\_life.info\_writer
-   sn\_bom.b2b\_agent

</td></tr><tr><td>

Group insurance underwriting viewer\[sn\_ins\_group\_uw.viewer\]

</td><td>

View underwriting tasks and related data for group insurance policy services

</td><td>

sn\_bom.service\_definition\_read

</td></tr></tbody>
</table>## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group Life Underwriting Service Task

 \[sn\_ins\_group\_uw\_task\]

</td><td>

Stores all underwriting tasks for group policy service requests for all Financial Services Operations applications. This table extends the Financial Task \[sn\_bom\_task\] table.

</td></tr></tbody>
</table>
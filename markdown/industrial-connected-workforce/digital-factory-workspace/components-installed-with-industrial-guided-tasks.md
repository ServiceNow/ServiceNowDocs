---
title: Components installed with Industrial Guided Tasks
description: Several types of components are installed with activation of the plugin, including tables and user roles.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Industrial Guided Tasks, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Components installed with Industrial Guided Tasks

Several types of components are installed with activation of the plugin, including tables and user roles.

## Roles installed

<table id="table_xkb_4fr_pdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Industrial Guided Task Expert

 \[sn\_icw\_igt.expert\]

</td><td>

Expert role for the Industrial Guided Tasks application

</td><td>

sn\_icw\_igt.user

</td></tr><tr><td>

Industrial Guided Task Standard Author

 \[sn\_icw\_igt.standard\_author\]

</td><td>

Can contribute to the Industrial Guided Task standards

</td><td>

-   sn\_icw\_std.standard\_author
-   sn\_smart\_imp\_auto.automation\_creator
-   sn\_smart\_asmt.template\_manager
-   sn\_icw\_igt.expert

</td></tr><tr><td>

Industrial Guided Task User

 \[sn\_icw\_igt.user\]

</td><td>

User role for the Industrial Guided Tasks application

</td><td>

-   sn\_smart\_asmt.assessment\_reader
-   sn\_smart\_asmt.template\_reader
-   sn\_smart\_asmt.actor
-   sn\_icw\_std.user

</td></tr></tbody>
</table>**Note:** Only users with the sn\_icw.application\_admin role can override the IGT standard and task access control lists \(ACLs\).

## Tables installed

-   Industrial Guided Task Standard \[sn\_icw\_igt\_standard\]
-   Industrial Guided Task \[sn\_icw\_igt\_task\]

**Parent Topic:**[Industrial Guided Tasks reference](industrial-guided-tasks-reference.md)


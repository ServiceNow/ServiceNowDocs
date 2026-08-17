---
title: Components installed with Industrial Standards
description: Several types of components are installed with activation of the Industrial Standards application. This includes tables, user roles, and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/components-installed-with-industrial-standards.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Industrial Standards, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Components installed with Industrial Standards

Several types of components are installed with activation of the Industrial Standards application. This includes tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_ac1_ymx_y2c"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Standard Standard Author

 sn\_icw\_std.standard\_author

</td><td>

Can plan and manage standards data

</td><td>

sn\_icw\_std.user

</td></tr><tr><td>

Standard User

 \[sn\_icw\_std.user\]

</td><td>

Can read standards tables

</td><td>

-   oc\_read
-   sn\_icw.user

</td></tr></tbody>
</table>## Tables installed

-   Published Industrial Standard \[sn\_icw\_std\_publ\_standard\]
-   Standard Schedule \[sn\_icw\_std\_schedule\]
-   Standard scheduled plan \[sn\_icw\_std\_scheduled\_plan\]
-   Industrial Standard \[sn\_icw\_std\_standard\]
-   Industrial Standard Applied to Task \[sn\_icw\_std\_standard\_applied\_to\_task\]
-   Industrial Standard Task \[sn\_icw\_std\_task\]

## Roles installed with work set standards

<table id="table_otq_frw_xjc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Work Set Standard Author

 \[sn\_icw\_std.work\_set\_standard\_author\]

</td><td>

Can create, update, and publish work set standards and sub-activities.

</td><td>

sn\_icw\_std.work\_set\_expert

</td></tr><tr><td>

Work Set Expert

 \[sn\_icw\_std.work\_set\_expert\]

</td><td>

Can execute and cancel work set tasks.

</td><td>

sn\_icw\_std.work\_set\_user

</td></tr><tr><td>

Work Set User

 \[sn\_icw\_std.work\_set\_user\]

</td><td>

Can execute work set tasks and the child tasks and actions that they generate.

</td><td>

-   sn\_icw\_std.user
-   sn\_icw\_igt.user

</td></tr></tbody>
</table>## Tables installed with work set standards

-   Work Set Standard \[sn\_icw\_std\_work\_set\_standard\]
-   Work Set Sub-Activity \[sn\_icw\_std\_work\_set\_sub\_activity\]
-   Work Set Task \[sn\_icw\_std\_work\_set\_task\]

**Parent Topic:**[Industrial Standards reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-standards-reference.md)


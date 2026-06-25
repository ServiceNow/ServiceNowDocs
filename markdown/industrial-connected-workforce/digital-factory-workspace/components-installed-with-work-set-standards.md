---
title: Components installed with work set standards
description: Several types of components are installed with the work set standard feature. This includes roles and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/components-installed-with-work-set-standards.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-05-25"
reading_time_minutes: 1
keywords: [components installed, work set roles]
breadcrumb: [Industrial Standards, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Components installed with work set standards

Several types of components are installed with the work set standard feature. This includes roles and tables.

## Roles installed

<table id="table_roles"><thead><tr><th>

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
</table>## Tables installed

-   Work Set Standard \[sn\_icw\_std\_work\_set\_standard\]
-   Work Set Sub-Activity \[sn\_icw\_std\_work\_set\_sub\_activity\]
-   Work Set Task \[sn\_icw\_std\_work\_set\_task\]

**Parent Topic:**[Industrial Standards reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-standards-reference.md)

**Related topics**  


[Work set standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standards.md)

[Work set standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.md)


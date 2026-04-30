---
title: Assign roles to Lead-to-Cash Process Management users
description: Assign roles to your users so that they can access features, capabilities, and data in the Lead-to-Cash Process Management application.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Lead-to-Cash Process Management, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Assign roles to Lead-to-Cash Process Management users

Assign roles to your users so that they can access features, capabilities, and data in the Lead-to-Cash Process Management application.

## Before you begin

Before you can assign roles to your users and groups, make sure you have created and configured required users and groups.

Role required: admin

## About this task

The following table lists the roles business object writers and sales process managers need to access the tables necessary to perform their respective tasks.

<table id="table_e5z_gx5_vfc"><thead><tr><th>

User persona

</th><th>

Job function

</th><th>

Role required

</th><th>

Tables accessed

</th></tr></thead><tbody><tr><td>

Business object writer

</td><td>

Creates business object groups and defines relationships between the business object types.

</td><td>

Business object writer

 \[sn\_bo\_core.business\_object\_writer\]

</td><td>

-   Business Object Type

\[sn\_bo\_core\_obj\_type\]

-   Business Object Relationship

\[sn\_bo\_core\_obj\_rel\]

-   Business Object Group

\[sn\_bo\_core\_obj\_group\]

-   Business Object Group Members

\[sn\_bo\_core\_obj\_group\_members\]


</td></tr><tr><td>

Sales process manager

</td><td>

Creates sales process records, monitors tasks and activities on the hierarchical node map, links and delinks nodes.

</td><td>

Sales process manager

 \[sn\_l2c\_cockpit.sales\_process\_manager\]

</td><td>

-   Sales Process Record

\[sn\_l2c\_cockpit\_sales\_process\_record\]

-   Business Process Record

\[sn\_bo\_core\_process\_record\]

-   Business Process Resource

\[sn\_bo\_core\_process\_resource\]

-   Business Process Task

\[sn\_bo\_core\_process\_task\]


</td></tr></tbody>
</table>You can assign roles to users and groups using either guided setup or through the following user administration features:

-   [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
-   [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

**Related topics**  


[Creating users](https://www.servicenow.com/docs/access?context=ua-creating-users&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Creating groups](https://www.servicenow.com/docs/access?context=ua-creating-groups&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Components installed with Lead-to-Cash Process Management](../reference/components-installed-lead-cash-process-management.md)

[Components installed with Business Object Core](../reference/components-installed-business-object-core.md)

